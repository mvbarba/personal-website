---
title: Quaternion Demo
summary: An educational advanced math demo, created in the Unreal Engine.
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
[Link to **playable build**](https://mbarba.itch.io/understanding-quaternions)

[Link to **github repo**](https://github.com/mvbarba/UnderstandingQuaternions)

Understanding Quaternions is a demo designed for indie developers who have used quaternions in their game dev projects, but were not really certain how exactly they worked as a mathematical object. 

A lot of game developers take for granted the convenience of the quaternion, and the mathematical operations that allow us to create guarateed smooth rotaional interpolation using them. 

![Screenshot of the quaternion demo](/img/quaternion/quat1.png)

Instead of developers simply abstracting quaternions into a rotation by converting them using some sort of toEulerAngles function, this demo enables them to have a full understanding of the quaternions, without diving too deep to the point that it is unreasonable for the average developer to understand (because trust me, quaternions can get pretty complicated if you want to understand exactly *how* they work, and not just how they function in game dev applications...)

![A more elaborate example of the rotation operation shown in my demo](/img/quaternion/rotation.PNG)

Besides the great practice I got with 3D math and Quaternion math, this project was also my first big Unreal Engine 4 project that I have ever fully released. I had a great time becoming familiar with the UE4 Blueprint, and interfacing classes and functions that I made in C++ into the Blueprints. It was super efficient to program complicated systems, such as the UI manager, and being able to simply call public function from them in Blueprints, such as opening UI menus. 

![Screenshot of blueprint](/img/quaternion/bp.png)

Above, you can see the main camera controller that I made, using a combination of Blueprint logic, and called public functions written in C++ to access other managers, such as the UI manager. 