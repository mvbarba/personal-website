---
title: ANTIGOLF 
summary: A 2D puzzle game made in Unity, for the Brackey's 2020.1 Game Jam, and selected as one of the 10 winners. 
tags:
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

links:
- icon: award
  icon_pack: fas
  name: Top 10 of 700 Game Jam
  url: 
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
[Link to **playable build**](https://mbarba.itch.io/antigolf)

[Link to **github repo**](https://github.com/mvbarba/antigolf)

ANTIGOLF is a 2D puzzle game made in Unity, created to be played on PC, Mobile, or in browser. The goal of the game is the opposite of golf, you want to NOT get the ball in the hole in a given amount of strokes. The game was initially created for the Brackey's 2020.1 Game Jam, in which it was well received.

![Image of stats for the game jam](/img/antigolf/score1.png)

As seen in the picture above, ANTIGOLF scored in the top 10 overall from over 700 other submission, and in the top 5 in categories such as "fun" and "innovation".

![Promo gif for ANTIGOLF](/img/antigolf/gif1.gif)

Although the game was fairly simple, the high levels of polish applied, especially for a game made in **six days** made it a highly competitive entry. 

![GIF showcasing the menu polish of ANTIGOLF](/img/antigolf/menugif.gif)

Below is a small snippet of code from script that controlled the hole movement, demonstrating some simple vector math skills.  

```cs
// First, check that this hole is of type Homing. Then, make it home onto our target's location.
if (moveType == HoleMoveType.Homing)
    {
    	// Get our direction vector by subtracting the target position from our position, and normalizing it
        Vector2 direction = (Vector2)target.position - rb.position;
        direction.Normalize();

		// Take the z-component of our cross product to find the amount to rotate to
		// This works because it will be 0 when we are facing the target
        float rotateAmount = Vector3.Cross(direction, transform.up).z;

        // Rotate 
        rb.angularVelocity = -rotateAmount * rotateSpeed;

        // Move straight forwards in the direction you are facing
        rb.velocity = transform.up * speed;
    }
```

![Screenshot of ANTIGOLF](/img/antigolf/screenshot1.PNG)
