---
title: "SparseNoise"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

Renders a sparse noise stimulus.

A BonVision primitive that generates and draws a non-overlapping discrete sparse grid of randomly activaated quads. 

## Description
DrawQuad as the name suggests displays a quad of specified size, at the defined location. The colour, location and size can all be controlled by the experiment.

### Notes
This node requires TextureResources to be initialised with DynamicVideo[Texture2D] in order to work. The display information of this stimulus can be logged using MatrixWriter. This node saves a binary file containing the linearised colour matrix of each image combination. The vector saved is long GridSize(1)xGridSize(2)x(RunTime/Duration) where RunTime is the total display time of the Bonsai programme.

## _Inputs:_ 
* It is a source node so it does not require any input to be able to run 
* ActiveQuads: number of quads to be displayed at the same time during a single image combination
* Duration: display time for a single image combination
* GridSize: number of columns and rows in which the display is divided. Quads dimension is the inverse of these values [int, int]


## _Outputs:_
* The output is to be connected to UpdateTexture
* All the properties that are externalised can be sent forward as outputs.
