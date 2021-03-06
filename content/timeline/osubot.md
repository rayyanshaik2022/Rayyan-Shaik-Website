---
title: "OsuBot"
eventname: "An osu! statistics discord bot"
date: 2021-03-06
publishDate: 2021-03-06
author: "Rayyan Shaik"
draft: false
images: []
tags: ["Python3","Featured"]
projects: ["Programming Projects"]
---

### Description
This is a discord bot designed to provide easily accessible statistics for the game osu! - a rhythm game with a wide player base. This bot can be used on the messaging & gaming platform "discord". 

The bot utilizes a few APIs and intuitive web scraping to easily find and calculate generalized and specific statsitics for osu! players. There are several
osu! discord bots provide these statistics, however, what makes this bot unique are some of its original commands - notably the `o.beatmap (name)` command, which uses web-scraping to find beatmaps (levels playable in the game) by name search, and the `o.practice` command, which analyzes a user's plays and recommends beatmaps to play. As of writing this, the bot has ~200 registered users and is exposed to over 80,000 different discord users*.

*A user does not need to be registered with the bot in order use most of its features.

This discord bot is also hosted 24/7 on a personal server so that it can be accessed at any time by discord users.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Osu-Bot-Public)   

### What were my goals with this project?
* Functional & useful commands
* Full utilization of discord.py library (structure and code)
* Abstraction through cogs
* Multi-user interactions and long-term data storage regarding many users
* Efficient algorithms to allow for several users to access commands at the same time
* Efficient web-scraping algorithms to minimize API calls and server CPU usage

### Challenges with this project

- #### Useful commands
- My previous discord, bot "Velocirator Bot", was created for personal use and primarly included commands that myself and its limited users would use.
A challenge with this discord bot however, is that I intended for it to be widely used, and for that to become a reality I had to make sure that
the bot had useful and practical commands. I also had to make sure not to "reinvent the wheel" and include several unique commands and options.

- #### Efficient Algorithms
- A challenge that comes with the bot being widely accessible, is that it needs to actually be able to support the usage of several users at once. Due to this, I had to had take very careful approaches when designing specific (usually web-scraping and API related) algorithms so that they would not overload websites nor my server. 

- #### Persistant Data
- A key feature of this bot is that it allows users to "register" and save their osu! username to have more convenient access to the bot's commands. To this, data - such as discord IDs and osu! usernames - would have to be saved. For this bot, I chose to represent this data in the `.json` format and utilize it with the `pickle` library.

### Project Images

{{< figure src="../../images/osubot1.png" alt="osubot1.png" width=350 >}}
---
{{< figure src="../../images/osubot2.png" alt="osubot2.png" width=350 >}}
---
{{< figure src="../../images/osubot3.png" alt="osubot3.png" width=350 >}}
---

### Dependencies
* discord.py
* asyncio
* json
* pickle
* collections
* requests
* BeautifulSoup4
* Selenium
