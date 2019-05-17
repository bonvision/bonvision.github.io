---
title: "RenderFrame"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

A Bonsai node that produces a sequence of events whenever it is time to render a frame.

## Description
RenderFrame is a source node that sets the parameters of the current shader configuration such as window, meshes, textures, and shaders parameters.

## _Inputs:_ 
* It is a source node so it does not require any input to be able to run 

## _Outputs:_
* Normally it is connected to viewport node.
* All the properties that are externalised can be sent forward as outputs.
