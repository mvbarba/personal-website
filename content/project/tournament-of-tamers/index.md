---
title: Tounament of Tamers
summary: An exciting new third person MOBA created by Buh! Gaming, where you pilot a dragon into multiplayer combat.
tags:
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

links:
- icon: link
  icon_pack: fas
  name: Official Website
  url: https://buhgaming.com/
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

Tournament of Tamers is a third-person multiplayer online battle arena created by Buh! Gaming in Kirkland, WA. In May 2019 I was hired as a Software Development Intern and have since been invited onto the team as a Part-Time Software Engineer.

In Tournament of Tamers, two teams of dragons face each other in a variety of game modes. Below is a video showing a round of gameplay from the Arena game mode. 

{{< youtube k6KGW5ZYaXk >}}

I have worked on a variety of tasks during my time so far at Buh! Gaming, one of them being the improvement of our navigation system for the AI enemies that attack dragons. The gif below shows an AI beetle minion routing itself around a statue that it might bump into during gameplay.

![GIF of beetle routing around object](/img/tournament/beetle.gif)

```cs
//have we reached our target?
float theDistance = Vector3.Distance(target.position, myTransform.position);
if (theDistance <= selectedArrivalDistance)
{

    // if we are following a path, it's time to select the next node in the path
    // now checks if beetle is being corrected
    if (behaviorState == Constants.BeetleBehaviorStates.FollowingPath)
    {
        //next node in the path
        currentNodeIndex++;

        if (path.nodeInPath.Count > currentNodeIndex)
        {
            GameObject node = path.nodeInPath[currentNodeIndex];
            target = node.transform;
        }
        // we've reached the end of the path
        else
        {
            path = null;
        }
    }
    else
    {
        // if we have reached the target we are chased, hover so we can attack from range.
        return;
    }
}
```
As you can see above, the system for navigating the beetles is abstracted to the point where you can just set the target location, and the beetle movement script will handle navigating around obstacles in its path on every frame update. 

Another task that I worked on was the implementation and improvement of many aspects of the Tournament of Tamers user interface. The gif below shows a player navigating through menus in the game's central hub area, The Nest. In the top left, you can see the player's rank is displayed. I was tasked with creating this ranking system and the UI to accompany it, which can be used to compare player stats, and place players in matches with people of similar skill level.

![GIF of Tournament of Tamer menus](/img/tournament/menu.gif)

Another interesting task that I worked on was the implementation of the Unity Analytics API in order to measure stats such as player retention, and dragon performance used to balance the fairness of gameplay between characters. The image below shows an example of a graph that is automatically generated using this API, which tracks how far players get in the tutorial before quitting. This can be useful for learning which parts of the tutorial needs improvement. 

![Tournament of Tamers analytics graph](/img/tournament/analytics.png)

Some of many other tasks that I have completed Buh! Gaming have included implementing the Steamworks API in order to track player stats on the Steam platform, creating new dragon abilities, and adding new aspects of gameplay such as a "bounty" mechanic that rewards players for taking down powerful enemies.
