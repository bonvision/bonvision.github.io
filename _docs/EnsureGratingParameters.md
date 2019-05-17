---
title: "EnsureGratingParameters"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

A BonVision primitive that specifies default values for optional parameters in the grating specification.

## Description
This node, as the name suggests, ensures the the grating parameters are formatted before

## _Inputs:_ 
* Needs a GratingSpecification node as an input to be able to run
* Contrast: contrast of the grating(0 to 1)
* Diameter: diameter of the grating in normalised screen units (0 to 1)
* Duration: displaying time of the grating (in seconds)
* Orientation: orientation of the grating in radians (0 to pi)
* SpatialFrequency: cycles per degree 
* TemporalFrequency: cycles per second 
* X: x coordinate of the centre of the grating in normalised screen coordinates (-1 to 1)
* Y: y coordinate of the centre of the grating in normalised screen coordinates (-1 to 1)
* Path: specifies an already save protocol to use for the grating. For example, a collection of grating stimuli with varying orientation or temporal frequency. After choosing the protocol, this node is automatically grouped in a sub-workflow whose name is the name of the protocol. 

## _Outputs:_
* _This can be an end node_
* All the properties that are externalised can be sent forward as outputs.
