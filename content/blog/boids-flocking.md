---
title: "Boids Flocking Algorithm"
description: "A visual implementation of the boids flocking algorithm"
date: 2020-04-12
publishDate: 2020-04-12
author: "Rayyan Shaik"
draft: false
images: []
tags: ["python3", "gui", "algorithm"]
---

### Description
My implementation of the boids flocking algorithm in pygame. It uses arrows - representative of birds - as enties that move around and account for each other's positions. Some additional features that I implemented include an "infinite border" - meaning borders transport entities to opposite ends of the map. The entities also spawn with random hues (color), and when several enities converge into a group, their colors average out. When these groups disband, the entities slowly revert to their original color.


### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Boids-Flocking)   

### What were my goals with this project?
* Implementation of the boids flocking algorithm
    * Separation: Steer to avoid contact with other entities
    * Alignment: Steer towards the average direction of nearby entities
    * Cohesion: Steer towards the average position of all entities
* Visually pleasing and easy to understand

### Project Images

{{< figure src="https://rayyanshaik.com/images/boids1.gif" alt="boids1.gif" width=600 >}}
---

### Dependencies
* pygame
