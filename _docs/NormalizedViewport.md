---
title: "NormalisedViewport"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Specifies an orthographic viewport with normalized screen coordinates for rapid prototyping of 2D environments

## Description
If you'd like to present 2D stimuli with parameters (e.g. sizes, locations) in terms of proportions of the screen size, then this can be used instead of OrthographicViewport. 

If so, then the locations of stimuli defined downstream of this node will use the centre of the screen as the origin, and have sizes that refer to the proportion of the short axis of the screen occupied.

I.e. a quad with an extent of 1 will have a side length equal to the length of the short axis of the screen.

### Notes


## _Inputs:_ 
* Can take the RenderFrame node as an input
* Path: The bottom boundary of the orthographic environment

## _Outputs:_
* Can have the DrawStimuli node as an output
* _This can be an end node_
