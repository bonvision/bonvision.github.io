---
title: "Logging"
redirect_from: /pages
excerpt: "A quick start guide to installing and running the Bonsai editor."
last_modified_at: 
author_profile: false
toc: true
---

# This page is under construction.
By 'Logging' we refer to saving information relavant for the experiment. In general, there are three kinds of data one might want to log during an experiment: 
- What are the stimulus parameters used in the experiment
- When were the stimuli presented
- Keeping track of external events

We created two nodes that can deal with all the three types of logging (we describe the three types of logging below). These nodes are: _FrameEventLogger & LogEvent_. The logger saves data to a .csv file and there are three aspects saved __Current frame index__, __Current Time__, __Logged information__.

_FrameEventLogger_: This is used to setup a logger. It needs to be placed after RenderFrame in the workflow as shown below. The first time this is encountered, it starts the clocks, both the frame counter and time. It also opens the .csv file that is specified where the information is saved. A logger then becomes a behaviour subject that can be accessed in the rest of the workflow. 

_Note A: You can start multiple loggers if you want to save different types of information in different files._

_Note B: You can start the logger either at the start of the experiment which will keep logs globally, or within a trial which will save data with respect to the relevant trial._

_Note C: There are options to overwrite, append (default), etc for the files, so make sure you do not lose information by overwriting the files_

< Image : workflow> 
< Image : parameters> 

_LogEvent_: This is actually used to save the data to the file. A _LogEvent_ node subscribes to a _FrameEventLogger_ subject, and writes to the correspoding file. Therefore, when there are multiple _FrameEventLogger_ subjects, we need to ensure to write to the correct file. The input to the _logEvent_ node can be the parameters that need to the saved (described below), and contain the format in which the data is saved. 

< Image : show parameters> 

*** 
### A. Logging screen update / refresh times
This is to note the time at which every frame was presented. It would therefore have the frame index and the time. The best way to save this is to have a _LogEvent_ node straight after the _FrameEventLogger_ that comes after the _RenderFrame_ node as shown below.

< Image : workflow> 

***
### B. Logging external events
There are many things happening during behavioural experiments. We describe this for a KeyPress on a keyboard, but the same concept applies to any extenal event (for example, if an animal is carrying out a nose poke). In this case, the _FrameEventLogger_ remains in the same place. The _logEvent_ would follow the node that is observing the external event, in this case a KeyPress. We need to specify which of the inputs are to be logged and the format in which to log them. 

_Note: the external events can be sampled at a different sampling frequency compared to the visual stimulus presentation. In the situation where the external data is at a higher rate, the frame index might not change as frequently, however, the time will remain precise_

This is an example workflow with a KeyBoard event logged.

< Image : workflow> 

< Image : format and output > 

*** 
### C. Logging stimulus parameters

< Image : workflow > 

< Image : format and output> 
