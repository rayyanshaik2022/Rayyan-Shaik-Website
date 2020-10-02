---
title: "Agar.io Clone"
description: "A server/client python clone of agar.io"
date: 2020-07-19
publishDate: 2020-07-19
author: "Rayyan Shaik"
draft: false
images: []
tags: ["python3", "sockets", "gui"]
---

### Description
A complete, scalable clone of the popular web game, agar.io. This project was created purely in python, and utilizes the pygame (GUI) and sockets (web connection) libraries. There are 2 main files used to run code. The first is client.py, which runs the game itself. The second is server.py, which can be run on any network and can open a customizable "agar.io" server on any port. This game is playable online, and through local networks.

### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/Agario-Multiplayer/)   

### What were my goals with this project?
* Create a reliable server and client connection with the sockets module
* Create a graphical/GUI game that implemented physics and a dynamic viewport
* Experiment with methods of storing and transfering data

### Agario-Multiplayer readme.txt
## Setup
* Run the server.py file. It will prompt you with how you want the game map to be, and what port to run the server on.
* Next run client.py.   An ip and port (localhost is default) can typed into the text box at the bottom.   
Click on the play button to join the server.

### Dependencies
* pygame
* sockets
