---
{"dg-publish":true,"permalink":"/inbox/zs-testing/","tags":[null]}
---



# ZS Testing
ZS testing, also known as Zero-Scanline Testing, is a technique used in [[Notes/Graphics Processing Unit\|GPUs]] to optimize the rendering of 3D graphics.

The purpose of ZS testing is to reduce the number of pixels that need to be processed during the rendering process. When rendering a 3D scene, the GPU needs to determine which pixels are visible and which are hidden behind other objects in the scene. ZS testing involves checking whether a pixel is hidden by performing a depth test that compares the depth value of the pixel with the depth values of other pixels that have already been processed.

During ZS testing, the GPU maintains a depth buffer that stores the depth values of the pixels that have already been processed. When a new pixel is being processed, its depth value is compared with the value in the depth buffer. If the new pixel is behind another object, it can be skipped and not rendered, saving processing time and resources.

ZS testing is an important optimization technique in modern GPUs because it allows for more efficient rendering of complex 3D scenes. It can also help to reduce power consumption and improve performance by reducing the amount of work that needs to be done by the GPU.
