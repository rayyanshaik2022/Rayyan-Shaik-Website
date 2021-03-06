---
title: "Smart Rockets"
eventname: "Guiding rockets via a genetic algorithm"
date: 2020-07-15
publishDate: 2020-07-15
author: "Rayyan Shaik"
draft: false
images: []
tags: ["Python3", "Gui", "Featured"]
projects: ["Programming Projects"]
---

### Description
This program is a demonstration of a genetic algorithm, with the use of "rockets" drawn 
as rectangles. Each "rocket" has its own dna telling them random directions to accelerate towards.
Rockets effectively gain a higher (better) fitness the closer they are to the goal (green circle)
and lose fitness (worse) if they try and go out of bounds or hit a boundary. In the scope of the
genetic algorithm, these fitness scores are used to create the next "generation" of rocket which
favors (not absolute) to combine dna of the top performing rockets. This, in turn, simulates evolution,
with each proceding generation utilizing the top performing "genes" of their predecessors.

This particular genetic algorithm also includes "Elitism". The highest performing rocket from each generation
is also chosen to be a part of the next generation (represented by the light blue rocket). 
This ensures, that there is a "check point" of sorts - preventing complete deviation from 
the goal as a result of mutation and poor performing crossovers.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Smart-Rockets)

### What were my goals with this project?
* Implementation of a genetic algorithm
* Efficient manipulation of a large quantity of objects

### Project Images

{{< figure src="../../images/smart-rockets1.gif" alt="agent-maze1.gif" width=500 >}}
---

### Dependencies
* Pygame


### Smart-Rockets README.md
This is a project designed and inspired from this youtube video:
https://www.youtube.com/watch?v=bGz7mv2vD6g by "The Coding Train"

While it does follow the original structure of the video, my version of the project
offers a translation (from javascript to python), demonstration and understanding of 
geometry (lack of built in drawing/rotation functions), knowledge of OOP programming,
as well as an understanding and implementation of a genetic algorithm.