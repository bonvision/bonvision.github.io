---
title: "OrthographicViewport"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Specifies an orthographic viewport, commonly used for 2D stimulus environments

## Description
OrthographicViewport can follow RenderFrame and (indirectly) precede SphereMapping to construct 2D environments. 

Using OrthographicViewport means that stimuli drawn will have sizes and locations defined in terms of visual angle - in contrast, using NormalisedViewport means that stimuli will have sizes and locations defined in terms of screen proportions.

### Notes


## _Inputs:_ 
* Can take the RenderFrame node as an input
* Path: The bottom boundary of the orthographic environment
* Bottom: The bottom boundary of the orthographic environment
* Left: The left boundary of the orthographic environment
* Right: The right boundary of the orthographic environment
* Top: The top boundary of the orthographic environment

## _Outputs:_
* Can have the DrawStimuli node as an output
* _This can be an end node_
