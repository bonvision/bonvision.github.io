---
title: "BonVision node library"
redirect_from: /docs
excerpt: "A quick start guide to installing and running the Bonsai editor."
last_modified_at: 
author_profile: false
toc: true
---

There are _5_ types of BonVision nodes:
 
I. [Primitives](/docs/docs#1-primitives)
These are the nodes that define fundamental visual stimulus characteristics.

II. [Environment](/docs/docs#2-environment)
These define the aspects of the visual display devices.

III. [Collections](/docs/docs#3-collections)
These are nodes that define visual stimuli that comprise a collection of Primitives.

IV. [Logging](/docs/docs#4-logging)
These are nodes to help keep log of stimulus parameters for analysis

V. [_Generic_](/docs/docs#5-generic)
These are generic helper nodes



# I. Primitives
1. [DrawCheckerboard:](/docs/DrawCheckerboard/) Draws a parameterized checkerboard stimulus.

2. [DrawCircle:](/docs/DrawCircle/) Draws a single colored circle.

3. [DrawGratings:](/docs/DrawGratings/) Draws parameterized 2D sinewave gratings.

4. [DrawImage:](/docs/DrawImage/) Draws an affine transformed 2D image.

5. [DrawModel:](/docs/DrawModel/) Draws a transformed 3D model stimulus.

6. [DrawQuad:](/docs/DrawQuad/) Draws a single axis-aligned colored quad.

7. [DrawText:](/docs/DrawText/) Draws affine transformed multi-line text using the specified style.

8. [DrawTexturedModel:](/docs/DrawTexturedModel/) Draws a textured and transformed 3D model stimulus.

9. [ParameterRange:](/docs/ParameterRange/) Generates a linear range of values between min and max.

10. [PrimitiveResource:](/docs/PrimitiveResource/) Loads mesh and shader resources for rendering primitive stimuli.

11. [RangeAnimation:](/docs/RangeAnimation/) Animates a linear range of values between min and max at the specified cycles per second.



# II. Environment 
1. [DrawViewport:](/docs/DrawViewport) Renders all currently stored draw commands to the specified viewport.

2. [GammaCorrection:](/docs/GammaCorrection) Renders the current scene to a texture and applies gamma correction as a post-processing effect.

3. [MeshMapping:](/docs/MeshMapping) Renders the current scene to a texture and applies mesh mapping and brightness correction as a post-processing effect.

4. [NormalizedViewport:](/docs/NormalizedViewport) Specifies an orthographic viewport with normalized screen coordinates for rapid prototyping of 2D environments.

5. [OrthographicViewport:](/docs/OrthographicViewport) 
Specifies an orthographic viewport, commonly used for 2D stimulus environments.

6. [PerspectiveViewport:](/docs/PerspectiveViewport) Specifies a perspective camera viewport with the given field of view.

7. [SphereMapping:](/docs/SphereMapping) Renders the current viewport to a cubemap texture which can be used for environmental mapping of physical screens around the origin.

8. [ViewingWindow:](/docs/ViewingWindow) Renders the sphere map from the perspective of a viewing window of the specified size, position and orientation relative to the origin.



# III. Collections
1. [EnsureGratingParameters:](/docs/EnsureGratingParameters) Specifies default values for optional parameters in the gratings specification.

2. [GratingSpecification:](/docs/GratingSpecification) Creates a sequence of grating parameters used for stimulus presentation.

3. [SparseNoise:](/docs/SparseNoise) Generates and draws a non-overlapping discrete sparse grid of randomly activated quads.



# IV. Logging
1. [EventLogger:](/docs/EventLogger) Creates and initializes a CSV file, and matching behavior subject, on which to log events.

2. [LogEvent:](/docs/LogEvent) Logs a value into the specified common event stream.

3. [TimeStampedEventLogger:](/docs/TimeStampedEventLogger) Creates and initializes a CSV file, and matching behavior subject, on which to timestamp and log events.



# V. Generic
1. [Angle:] Represents a workflow property specifying a single-precision angle, in degrees.
cycles per second.

2. [SampleMany:] Draws multiple random samples from the input distribution.
