---
title: "3D Engine"
eventname: "A full 3D Rendering Engine written from scratch"
date: 2021-07-30
publishDate: 2021-07-30
author: "Rayyan Shaik"
draft: false
images: []
tags: ["Python3", "Gui", "Featured"]
projects: ["Programming Projects"]
---

### Description
This projects features a 3D Rendering Engine that I have written using Python3 and Pygame (simple 2D graphics drawing library). It allows for
the manipulation of points in 3 dimensional space. It was designed with the future use of creating a simple 3D game, and the code is written so that
it is easy to utilize and understand from a high level perspective.


### Github Repository
The [Github repository can be found here](https://github.com/rayyanshaik2022/3D-Engine)

### What does this project feature?
* Render custom objects by vertices, poly lines (edges), and faces
* Load and view `.obj` 3D files
* Lighting/light source implementation
* Perspective camera view
* Object rotations and translations

### Project Images
-----

#### Rendering 3d object by vertices and lines
{{< figure src="../../images/line-render.gif" alt="line-render.gif" width=600 >}}

#### Rending 3d object by faces (with light source)
{{< figure src="../../images/face-render.gif" alt="face-render.gif" width=600 >}}
---

#### Key Components by File
- **vector3.py | Vector3**
    - `vector3.py` features the `Vector3` class. This is used (as the name implies) to represent a 3 dimensional vector. Nearly every 3 dimensional vertex is represented by an object of this class.
    - A `Vector3` object stores its (x, y, z) values in a numpy array. This allows for faster mathematical operations to be used on the the values.

- **camera.py | Camera**
    - `camera.py` features the `Camera` class. An object of this class represents a perspective camera, and is used to rotate and translate every existing vertex by its own rotation and position. It also converts the 3 dimensional point to a 2 dimensional cartesian plane that can be drawn on screen
    - The bulk of the math is computed within the `orient_vector()` method. It translates a point, then rotates it by the cameras current rotation, applies a projection matrix, perspective matrix, and then an offset matrix. The resulting point remains in (x, y, z) form, where '(x, y)' can be drawn on the screen and 'z' is the depth from the from the front of the camera's viewing angle.

- **environment.py | Environment**
    - `environment.py` features the `Environment` class. An object of this class acts as the "3 dimensional space manager". It is designed to help
    keep track of loaded 3D objects and meshes.
    - Add/remove objects, translate/rotate objects, etc
    - `draw_object()` is a method that calculates the position of points, lines, faces, and lighting and returns the values in an easy to draw format.

- **mesh.py | Mesh & MeshReader**
- `mesh.py` features the `Mesh` class. An object of this class stores a mesh (vertices, lines, faces) from a loaded `.obj` 3D object.
- `mesh.py` features the `MeshReader` class. An object of this class can be used to read the raw data from `.obj` files and store them in a `Mesh` object.

- **main.py | Gui**
- `main.py` features the execution code and the `Gui` class. This class handles the pygame window and drawing mechanics.



#### Learning Resources
- The concept and code for this project was developed 100% by myself.
These are the links to resources that I used to learn about the math behind 3D Engines
- [3D Projection Wikipedia](https://en.wikipedia.org/wiki/3D_projection)
- [Scientific calculations - distance and light intensity - BBC](https://www.bbc.co.uk/bitesize/guides/zs4mk2p/revision/7)
- [Wavefront .obj file Wikipedia](https://en.wikipedia.org/wiki/Wavefront_.obj_file)
- [The Camera Transform - UC Davis Academics](https://www.youtube.com/watch?v=mpTl003EXCY)