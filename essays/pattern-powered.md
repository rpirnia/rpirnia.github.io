---
layout: essay
type: essay
title: "Pattern Powered!"
# All dates must be YYYY-MM-DD format!
date: 2025-04-24
published: true
labels:
  - Design Patterns
  - Organization
  - Reusability
---

<img width="600px" text-align="center" class="img-thumbnail" src="../img/dp.png">

*Patterns are about using what you know to make sense of what you don't know*

## Patterns

There are patterns all around us, from the square paneled walls of a room to the purple polka dot shirt you swear you do not recall purchasing. These patterns are repetitive of course. You could even consider them related. Now, let's go beyond patterns you might see in a wall or on a shirt and think about ones you might see on a larger scale. Like the birthday celebration you throw for your sister every year, each one building on the last, trying to top the cake, the playlist, or the theme—learning from what worked (or didn’t) the year before.

Too abstract? I get it. *Let's just jump straight into it.*

## The Problem Design Patterns Solve
A common problem students face in introductory Software Engineering classes is building their first website. Without realizing, we are importing libraries of workable code, finding relevant source code, and even using templates. We know that by importing Container, Col, and Row from React Bootstrap, we'll get a pretty good grid system to present our information. We do not know the ins and outs of how this renders, but we know it works and that we can use it to make something even better. That is what design patterns aim to do—**create more efficient, reusable, and maintainable code**.

## The Pattern of Progress
Using design patterns is like discovering that there’s a method to life’s madness. Imagine trying to bake a cake without a recipe. Sure, maybe you could eyeball the flour and guess at oven temps, but odds are you’d end up with a half-baked blob. Now imagine having not just a recipe, but ten versions from expert bakers, all refined over time to solve specific baking problems—like keeping the cake moist or layering it perfectly. That’s what design patterns are for developers: a shared collection of recipes refined through years of trial, error, and success.

## Our Project: Campus Plate Mate
For ICS 314, a Software Engineering class I’m taking in university, our final project is to bring everything we’ve learned together and build something cool. My team decided to make Campus Plate Mate, a web application that connects students to affordable leftovers and businesses to happy takers.

Campus Plate Mate uses [this template](https://github.com/ics-software-engineering/nextjs-application-template). This template has forms for AddStuff, Edit Stuff, and a Stuff Item Admin, which we used to develop our Add Food and Dashboard pages. Thus, we used the **Template Method Pattern**. Then, there is the points system we are implementing. We plan on using a **Strategy Pattern** to handle what you get points for (e.g., 1 point for logging in, 5 points for redeeming food, etc.). This allows for flexibility. 

Another small but meaningful feature we are working on is a feedback footer, where users can submit comments or suggestions. Each submission is handled individually and stored as a standalone action. This resembles the **Command Pattern**, where each user action is packaged as its own object—something that could later be tracked, analyzed, or responded to.

We didn’t start with a list of design patterns and build around them. But through trial, error, and teamwork, we ended up using them anyway. That’s the power of patterns—they show up when you start building real things. They help you reuse what works, avoid what doesn’t, and make life (and code) just a little more easier.

<p style="text-align: center; font-size: 0.8em;"> Note: This essay was reviewed by ChatGPT for structure and grammar corrections.</p>
