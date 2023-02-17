---
{"dg-publish":true,"permalink":"/inbox/the-graphics-rendering-pipeline/","tags":[null]}
---



# The Graphics Rendering Pipeline
## What is the rendering pipeline?
- A series of stages that take place in order to render and image to the screen.
- Four stages are programmable via [[Inbox/Shader\|Shaders]].
## General Overview
1. *Build*: Object is built by an artist and represented as a mesh of triangles defining the surface of the object.
2. *Animate*: For each frame of rendering we animate each vertex in the mesh to place object correctly sized and oriented (#TODO : clarification).
3. *Rasterize*: The [[Inbox/Graphics Processing Unit\|GPU]] rasterizes the visible triangles.
4. *Color*: Pixels are colored and written to [[Frame Buffer\|Frame Buffer]].

## Computation Pipleline
1. [[Notes/Central Processing Unit\|CPU]]: The [[Notes/Central Processing Unit\|CPU]] runs the application and the graphics driver, and is responsible for animation, physics, and uploading data into DRAM.
2. Command Processing: The [[Inbox/Graphics Processing Unit\|GPU]]'s command processing stage is responsible for interpreting requests made by the [[Notes/Central Processing Unit\|CPU]] and coordinating the [[Inbox/Graphics Processing Unit\|GPU]]'s data processing stages.
3. Geometry Processing: The geometry processing stage takes the input meshes designed by the content artists, animates each vertex into the correct location in screen-space, generates any additional per-vertex data payload such as per-vertex lighting, and emits a stream of primitives, most commonly triangles, for pixel processing to consume.
4. Pixel Processing: The pixel processing stage consumes this primitive data, [[Inbox/Rasterization\|rasterizes]] it to generate pixel coverage and executes the fragment coloring operations. To run this process, the [[Notes/Central Processing Unit\|CPU]] must upload different types of data resource.