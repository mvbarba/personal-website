---
title: Police Trainer VR
summary: A modern Virtual Reality arcade shooter, created in Unity.
tags:
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

links: []

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Police Trainer VR is an immersive virtual reality experience based on the classic light gun arcade game Police Trainer 2. In it, you take the role of a police officer going through a futuristic new training procedure. 

For Police Trainer VR, I wanted to keep the fun arcade feel of the original game, while enhancing it with the immersion of VR. I made a system that lets you easily navigate through menus full of minigames and scoreboards using the virtual gun, so there was no interruption between gameplay. Between minigames, a gameplay manager object is used to handle loading the prefabs that make up each part of gameplay.

Here is one of the minigames, where players are challenged to quickly shoot as many targets as possible in a given time.
![GIF of the speed minigame](/img/police/speed.gif)

Here is another minigame, where players must quickly match two targets among many similar looking targets.
![GIF of the visual minigame](/img/police/visual.gif)

In order to make the game as immersive as possible, I wanted to make the actions you do in real life match up with those in the game. When you pull the trigger on the VR controller, the trigger moves 1:1 in VR as well. In addition to this, when the gun fires, haptic feedback is triggered, and directional audio will play using the position of the gun as a source. As an example, if you shot the gun on your left side, the gun would sound much louder in your left ear

![GIF of gun firing](/img/police/gun.gif)
