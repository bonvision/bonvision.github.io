---
title: "GratingSpecification"
redirect_from: /docs/
excerpt: "docs"
last_modified_at: 
author_profile: false
---

A BonVision primitive that creates a sequence of grating parameters used for stimulus presentation. 

## Description
GratingSpecification allows the creation of an arbitrarily large collection of grating stimuli with different parameters that can be specified from their input Trials.

### Notes
Best used with _SphereMapping_ transformed coordinate frame

## _Inputs:_ 
* Needs DrawStimulus (the tag for rendering a frame) as an input to be able to run
* Trials: opens a window in which set the parameters of a collection of grating stimuli (trials)

## _Outputs:_
* This node is to be connected to EnsureGratingParameters
* All the properties that are externalised can be sent forward as outputs.
