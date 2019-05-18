---
title: "SphereMapping"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Renders the current viewport to a cubemap texture which can be used for environmental mapping of physical screens around the origin.

## Description

### Notes

## _Inputs:_ 
* Can take the DrawStimuli node as an input
* Path: The path of the workflow to include
* ClearColor: The color used to clear the framebuffer before rendering
* FaceSize: The optional texture size for each of the cubemap faces
* Height: The optional height of the texture used for spherical mapping. Higher values reduce blurring but decrease performance
* Width: The optional width of the texture used for spherical mapping. Higher values reduce blurring but decrease performance

## _Outputs:_
* Can have the DrawStimuli node as an output
* _This can be an end node_
