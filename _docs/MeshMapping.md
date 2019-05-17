---
title: "MeshMapping"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Renders the current scene to a texture and applies mesh mapping and brightness correction as a post-processing effect.

A BonVision primitive that applies a warping map for displaying scenes on arbitrary screen surfaces. 

## Description
MeshMapping adjusts the scene to compensate for the curvature of the screen surface before being rendered. This function allows for conformal projections of the visual stimulus on any arbitrary surface. It is normally used for demispherical dome screens whose physical properties are known. These information are retrieved from a *.CSV file. In the case of a spherical screen, these are the coordinates of the intersections between meridians and parallels in degrees (first two columns) and pixels units (third and fourth column); the fifth column contains the normalised brightness level for each node. 

### Notes
Normally used with projectors. For info about mesh mapping please see "Bourke, P. (2005), ‘Spherical Mirror: A New Approach to Hemispherical Dome Projection’, Planetarian, December 2, pp. 6–9." or "Bourke, P. D. (2008), ‘Immersive gaming: a low cost projection environment’, Journal of MultiMedia, 3, pp. 41–46." 

## _Inputs:_ 
* Needs DrawStimulus (the tag for rendering a frame) as an input to be able to run
* FileName: .CSV mesh mapping file
* ClearColor: specifies the colour to use when clearing colour buffers


## _Outputs:_
* _This can be an end node_
* All the properties that are externalised can be sent forward as outputs.
