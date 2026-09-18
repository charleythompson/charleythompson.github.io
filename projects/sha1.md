---
layout: project
type: project
image: img/sha1.png
title: "SHA-1 Implementation"
date: 2025-01-01
published: true
labels:
  - C
  - Algorithms
  - Bitwise Operations
summary: "An implementation of the SHA-1 hashing algorithm in C based on the FIPS 180-1 specification."
---

For this project, I implemented the SHA-1 hashing algorithm in C. Basically, the goal was to take an input message and turn it into a 160-bit message digest. Many of my assignments prior to this involved a lot of user interaction and freedom to take creative liberties, but for this assignment I had to use the FIPS 180-1 specification as a strict guide.

Before SHA-1 could actually calculate the hash, the input had to be prepared. First, my program reads the user input and adds the required padding. Then, it figures out how many 512-bit blocks are needed and converts those bytes into 32-bit words. Next, each of the 512-bit blocks is expanded into a sequence of 80 words that are used during the hashing process.

Once the input was prepared, the program had to repeatedly mix the data using bitwise operations and circular shifts. SHA-1 does this over 80 rounds while constantly updating five 32-bit values until the final hash is produced. Following the specification, I split some of these steps into smaller functions, like circleLeft(), f(), and K(), which made the algorithm easier for me to understand and debug.

In this project, I put a lot of effort into keeping my program accurate and learned a lot about maintaining quality throughout a larger program. I added many debug functions throughout the program so I could manually check things like the input bytes, the number of blocks, the 32-bit words, and the message-length value. That made it much easier to figure out where something had gone wrong, especially because I could very easily compare my values with the FIPS 180-1 specification.

Overall, I think this project made me a lot more confident working with C, bitwise operations, and organizing larger programs. It felt very satisfying to comb through a technical specification and turn it into a real, working program. The project was tough, but it taught me how to take a large, seemingly daunting goal and break it up into smaller pieces that I could individually implement and test.
