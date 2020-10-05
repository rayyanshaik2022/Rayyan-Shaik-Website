---
title: "A* Pathfinding"
description: "Visual representation of the A* Pathfinding Algorithm"
date: 2018-07-04
publishDate: 2018-07-04
author: "Rayyan Shaik"
draft: false
images: []
tags: ["python3", "gui", "algorithm"]
---

### Description
An implementation of the A* Pathfinding Algorithm. The logic behind this algorithm is based on the function ```f(n) = g(n) + h(n)```.
Where the total cost of "moving" is the sum of the cost of the path to the starting node and the cost as calculated by the heuristic function for the cheapest path from the next node to the goal.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/A-Pathfinding)

### What were my goals with this project?
* Practice advanced manipulation of 2d arrays
* Practice GUI efficiency
* Object-Oriented approach
* Implentation of nodes, and stepping through nodes (effectively complex linked lists)

### Project Images

{{< figure src="https://rayyanshaik2022.github.io/Rayyan-Shaik-Website/images/astar1.gif" alt="/images/astar1.gif" width=500 >}}
---


### Dependencies
* Pygame


### A* Pathfinding readme.txt
## Usage:
Number Key 1: Cycles through placing the start location, goal location, and walls   
Number Key 2: Clears all walls   
Space Bar: Runs the pathfinding algorithm   