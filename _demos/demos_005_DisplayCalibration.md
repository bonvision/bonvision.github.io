---
title: "Display Position Calibration"
redirect_from: /demos
excerpt: "A quick start guide to installing and running the Bonsai editor."
last_modified_at: 
author_profile: false
toc: true
---

### Under Construction

# Display Position Calibration

BonVision is fundamentally based on creating stimuli that are true to the experimenter's definition of the visual environment around a subject, and display devices (monitors/projectors) are merely windows into this environment. Therefore, it is important to know which part of the environment the displays are looking into.  

The position of the visual field that the display is looking into is defined by the parameters in the _ViewPort_ node. Specifically, the parameters: ___, ____, ____, & ____.

There are two ways of calibrating the position of a display in BonVision:

## __1. Old school with ruler and protractor__ 
Measure the physical distances and angles. This can get a little tricky with getting accurate measurements of angle. However, if you have a method to measure this, or are happy with approximate values, these are the measurements you would need:
* The size of the display in azimuth and elevation
* The distance of the bottom of the screen from the subject's position
* The angles of the __ __ of the monitor from the subject's position

## __2. Automated calibration with camera__ 
We developed these workflows to enable easy and effective calibration of display position. Conceptually, this is done using a calibrated camera (we provide a workflow to calibrate here) and [Aruco markers](https://docs.opencv.org/trunk/d5/dae/tutorial_aruco_detection.html) to identify the 3D coordinates of the display relative to the subject. 

The workflow identifies the Aruco patterns on the display and in the subject's position, using a calibrated camera, and automatically calculates the display's position. This automatic calibration has three workflow associated with it (each of them is expanded on below):
_A. Measuring camera intrinsics_
_B. Show an Aruco image on the display_
_C. Calibrate the screen position_

# __A. Measuring camera intrinsics__
This workflow is to calibrate the intrinsic properties of the camera-lens combination, using standardized OpenCV formats. If you have previously calibrated the camera, you can simply save the value in the OpenCV format and link the function C (below) to that file. Alternatively, you will need to run this program. Running it displays a checkerboard pattern on the screen. (You can also print a checkboard patter of known size). Once it is displayed in the screen, measure the size a unit square and enter it under __  __ After that you will have to take pictures of the checkerboard pattern from different camera viewing angles. In the workflow, an image can be taken by hitting the _spacebar_. As a standard, we use 7 images: (1) from the front of the pattern, (2) from the Left, (3) from the Right, (4) from below the pattern, (5) from above, (6) from the top, right corner, and (7) from the bottom left corner (illustrated in the figure below).

# __B. Show an Aruco marker on the display__
This is just used to show a single image at the centre of the display. Once displayed, it is important to measure the size of the image using a ruler, to ensure that it is of a known size. 

# __C. Calibrate the screen position__
We would need to have one Aruco marker on the centre of the display and one at the positon of the subject. The latter is ideally a print out of a known size. Once these are displayed, we just need them to be viewed simultaneously through the camera and run the workflow which generates the calibrated position values. _Note that Aruco markers are directional, i.e. it matters which of the four sides of the square faces the front (or 0 deg)._
