---
title: "Autoclickr"
eventname: "An autoclicker script"
date: 2019-06-28T12:39:56+01:00
publishDate: 2019-06-28T12:39:56+01:00
author: "Rayyan Shaik"
draft: false
images: []
tags: ["Python3", "Threading"]
projects: ["Programming Projects"]
---

### Description
A complete GUI environment designed to test grid/maze solving algorithms. Complete with a GUI environment
builder.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Autoclickr/https://github.com/WPS-Programming/Agent-Maze-Solver)

### What were my goals with this project?
* Create a fast and reliable auto clicker
* Have the script be easy to use and interact with
* Make the driver code relatively simple for easy changes

### Driver code
{{< highlight python >}}
from autoclickr import Autoclickr

mult = int(input("Scale value (threads to be opened): "))

clicker = Autoclickr(True, 0, 'left', 'right',scaled=mult, clickType=0)
clicker.run()
{{< /highlight >}}

### Autoclickr readme.txt
## PARAMETERS
(True, 0, 'left', 'right', 0, 1)

1 - The first parameter indicates whether the clicker is enabled or disabled. It must be defined as enabled (True) to work.  
2 - The second parameter is a time delay (in seconds), between clicks. If this is set to 0, there will be no delay. (Max cps of 10)  
3 - The third parameter takes a key which will be used to enable the clicker (All keys usable in the 'keyboard' library will work)  
4 - The fourth parameter takes a key which will be used to disable the clicker (All keys usable in the 'keyboard' library will work)  
5 - The fifth parameter takes an int which represents the type of click you want (0 = Left Click, 1 = Right Click, All other values will default to 0).  
6 - The sixed parameter refers to 'scalability' or the multiplier. It opens new threads for clicking allowing you to click hyper-fast.