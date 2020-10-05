---
title: "Perlin Noise Map Generator"
description: "An seed-based island/landmass generator"
date: 2020-04-24
publishDate: 2020-04-24
author: "Rayyan Shaik"
draft: false
images: []
tags: ["python3","gui","algorithm","featured"]
---

### Description
A map generating script primarly using the perlin noise equations. This program utilizes a the 2d perlin noise equation to generate topographic values in a 2d list. These values are normalized and assigned a "color output" depending on their value (for example, a low value would mean blue or water, while a high value might be grey for mountains). This program also uses poisson disc sampling to randomly generate trees across the landmasses.
Due to the nature of the calculations, the program is relatively slow (requires ~2-3 seconds to launch); this is partly due to the resolution of the image, and partly due to the constantly generating/updating cloud layer.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Perlin-Map-Generator)   

### What were my goals with this project?
* Create a visually pleasing and effective map generator
* Utilize complex numpy operations to practice list/array manipulation
* Work and implement algorithms and equations such as perlin noise and poisson disc sampling.


### Project Images

{{< figure src="/images/perlinmap2.png" alt="perlinmap2.png" width=500 >}}
---
{{< figure src="https://rayyanshaik2022.github.io/Rayyan-Shaik-Website/images/perlinmap3.png" alt="perlinmap3.png" width=500 >}}
---

### Dependencies
* pygame
* noise
* numpy
* bridson.poisson_disc_samples
