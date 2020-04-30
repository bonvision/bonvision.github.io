---
title: "Stimulus Series List"
redirect_from: /pages
excerpt: "A quick start guide to installing and running the Bonsai editor."
last_modified_at: 
author_profile: false
toc: true
---

This is to create a stimulus series, by loading parameters from either a csv file, or create a collection within Bonsai. The result is to have something similar to what is discussed in the [Grating Series](/pages/08-GratingSeries), without the custom nodes for grating stimuli, hence creating a convienient workflow from scratch. Similar to the grating stimuli, one can load the stimulus set either from a csv file or a collection. Loading from a csv file, can be generated without any additional nodes. While, the collection route makes it easier to edit the experimental parameters within Bonsai, this requires writing a custom code in C# that we will walk you through below. (you do not really need expertise in C# to be able to modify this for your own stimuli).

## Stimulus series from CSV file
This is the workflow called "__X__" in the examples folder. 

Here we start with the workflow at the end of [Grating Series](/pages/08-GratingSeries), and substitute the _CreateGratingTrial & GratingSequence_ nodes with a _CreateObservable_ group and a _Concat_:
![]({{ '/assets/Images/StimulusSeries/StimSeries-A1.PNG' | relative_url }})

Within the CreateObservable group:
![]({{ '/assets/Images/StimulusSeries/StimSeries-A1-1CreateObservable.PNG' | relative_url }})

We create a BehaviourSubject from the inputs to the group, i.e. the outputs of _ExpressionTransform_ 
![]({{ '/assets/Images/StimulusSeries/StimSeries-A1-1CreateObservable2.PNG' | relative_url }})

Some of the parameters can be directly mapped to the the externalised properties of the _DrawGratings_ node:
![]({{ '/assets/Images/StimulusSeries/StimSeries-A1-1CreateObservable3.PNG' | relative_url }})

And here is an example where the parameter is converted into the correct units (degrees to radians):
![]({{ '/assets/Images/StimulusSeries/StimSeries-A1-1CreateObservable4.PNG' | relative_url }})

## Stimulus series using a collection
This is the workflow called "__X__" in the examples folder. 

Here we start with the workflow from the start of [Grating Series](/pages/08-GratingSeries), and substitute the GratingSpecification node with a _CSharpTransform_ like this:
![]({{ '/assets/Images/StimulusSeries/StimSeries-B1.PNG' | relative_url }})

and this is an example of the C# code in the extensions folder

![]({{ '/assets/Images/StimulusSeries/CSharpCode.PNG' | relative_url }})
