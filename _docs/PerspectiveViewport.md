---
title: "PerspectiveViewport"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Specifies a perspective viewport, commonly used for 3D stimulus environments

## Description

### Notes

## _Inputs:_ 
* Can take the RenderFrame node as an input
* Path: The bottom boundary of the orthographic environment
* Eye: The eye, or camera position, in the world coodinate frame
* FieldOfView: The value of the angle of the field of view, in degrees
* Light: The position of the main point light
* Target: The target position in the world coordinate frame
* Up: The up vector of the camera, in the world coordinate frame. Should be parallel to the camera direction
* FarClip: The distance to the far clip plane
* NearClip: The distance to the near clip plane

## _Outputs:_
* Can have the DrawStimuli node as an output
* _This can be an end node_
