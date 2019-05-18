---
title: "DrawViewport"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Renders all currently stored draw commands to the specified viewport

## Description
DrawViewport allows you to define how the output of ViewingWindow is drawn onto the window created in CreateWindow. 

For example, if the window created in CreateWindow refers to a mosaic of two monitors, then two DrawViewports would allow you to draw something on one monitor, and something on the other.

### Notes
Best used with _SphereMapping_ transformed coordinate frame

## _Inputs:_ 
* Can take the ViewingWindow node as an input
* Path: The path of the workflow to include
* Height: The height of the viewport rectangle as a fraction of total number of pixels in the window height
* Width: The width of the viewport rectangle as a fraction of total number of pixels in the window width
* X: The x-coordinate of the lower-left corner of the viewport rectangle, as a fraction of total number of pixels in the window width
* Y: The y-coordinate of the lower-left corner of the viewport rectangle, as a fraction of total number of pixels in the window height

## _Outputs:_
* Can have the DrawViewport node as an output
* _This can be an end node_
