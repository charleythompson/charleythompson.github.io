---
layout: project
type: project
image: img/rocket.png
title: "3D Modeling and Animation in Maya"
date: 2026-09-01
published: true
labels:
  - Autodesk Maya
  - 3D Modeling
  - Animation
  - Arnold
summary: "A 3D animation project in Autodesk Maya featuring a rocket launch, a hidden cannon, animated lighting, procedural materials, and a laser-driven destruction sequence."
---

This project was my first time using any kind of 3D modeling or animation software. My professor gave us the rather broad instructions of ‘make an animation where a rocket takes off, has a complication, then crashes’, and he encouraged us students to be creative with it. I wanted to make something ambitious enough to challenge myself, but still realistic enough that I could actually finish it without suffering from burnout. My idea was to have the rocket launch and reveal a hidden cannon in the distance, which then charges up, fires a laser, and blasts the rocket out of the sky. I spent a lot of time thinking about the animation in terms of setup and payoff, especially building towards the climactic moment where the laser pierces the rocket.

<video width="100%" controls>
  <source src="{{ '/img/rocketvid.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Most of the project involved learning how to model and apply materials. One of the biggest challenges for me was making the cannon have a convincing dull concrete texture. I originally used a noise filter for both the color and surface texture, which looked fine in Maya, but in the render it came out looking as though it had no materials applied to it at all. After a lot of frustration and research, I eventually traced the problem to my GPU rendering. I ended up having to completely rebuild the texture using Arnold noise rather than Maya’s default noise. 

The animation had a lot more moving parts than I initially expected. For example, to visually show the cannon charging up, I used four red lights that turned green one by one. The four charging lights start off emitting an identical red light, so I initially had them all share one material. But in order to have them individually turn green, I ended up having to apply four identical materials, one to each light. I also had to tweak some awkward movement on the barrel of the cannon and create rocket debris using precise keyframing. I even ended up creating a duplicate of the rocket that I could tear apart in the final shot.

I really enjoyed the amount of creativity I used in this project, both from an artistic standpoint and a technical standpoint. The animation didn’t fully turn out as I envisioned, and there are many things I would have done differently now. But this project is special to me because of how much it taught me and how much I grew and learned throughout it. It was also a good lesson in grounding the ambitious perfectionist in me and accepting a result that, while not perfect, is good enough.
