---
title: "Grating Series"
redirect_from: /pages
excerpt: "A quick start guide to installing and running the Bonsai editor."
last_modified_at: 
author_profile: false
toc: true
---

## Under Construction

As grating stimuli are commonly used in visual physiology experiments, we have created a few nodes that make it convenient to design experiments very easily. These include the nodes _GratingTrial, CreateGratingTrial & GratingSpecifications_. This page will elaborate two ways of creating a grating series experiment. The first, simplest is to use the pre-designed nodes. The second option discusses an option of loading the list of parameters from a csv file.

_NOTE: On the page [Stimulus Series]() we show two other methods of creating such a stimulus without using the pre-designed nodes, which can adapted for any stimulus type that you would like to use._

*** 

## A. Simplest method: Using GratingSpecifications
This is the workflow called "__X__" in the examples folder. 

### Step 1. Add the nodes
For this one just needs to have the three nodes in this order. 

![]({{ '/assets/Images/GratingSeries/GratingSeriesA1.PNG' | relative_url }})

*** 

### Step 2. Enter parameters of stimuli
You can then specify the parameters of the stimuli to run by clicking on the Collections. This opens up a list such as this.

![]({{ '/assets/Images/GratingSeries/GratingSeriesA1-2.PNG' | relative_url }})

Each row in this is one stimulus (set of parameters). You can add the specific values by adding numbers in the corresponding ... 
If you want to set a parameter across all trials to some value, enter the value after selecting all the trials. 

![]({{ '/assets/Images/GratingSeries/GratingSeriesA1-3.PNG' | relative_url }})
![]({{ '/assets/Images/GratingSeries/GratingSeriesA1-4.PNG' | relative_url }})

*** 

## B. Alternate method: Loading parameters from a CSV file
This is the workflow called "__X__" in the examples folder. 
This is a version of the workflow that can run the same experiment, but loads the parameters of the grating stimulus from a csv file.  

### Step 3
From Step 1 above, instead of the __GratingSpecifications__ node, add three codes, _CSVReader, ExpressionTransform & Input mapping_.

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-1.PNG' | relative_url }})

The first node reads a csv file, the second parses the csv file details, and the third part maps it onto the corresponding parameters of the _CreateGratingTrial_ node.

*** 

### Step 4. Setup the CSV reader

Add the path to the csv file and details of the file. Here ',' is the separator, and the first line is skipped as it defines the columns.

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-2-1.PNG' | relative_url }})

Here is what the raw 'gratings.csv' file looks like:

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-CSV.PNG' | relative_url }})

Below this is what the formatted version looks like. You can add additional trials by adding new rows to the file:
B2.

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-CSV2.PNG' | relative_url }})

*** 

### Step 5. Setup the ExpressionTransform

Enter the details by expanding the details of the ExpressionTransform node

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-ExpTrans1-1.PNG' | relative_url }})

Here is the script within ExpressionTransform node

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-ExpTrans2.PNG' | relative_url }})

This follows from the csv files details, the first column goes to Orientation (in this case it is being converted to radians), the second column is speed, third is Contrast and the final one is Duration of the stimulus. 

*** 

### Step 6: Setup the InputMapping node
First have the InputMapping node between the ExpressionTransform and CreateGratingTrial nodes, and add the details within Collection.

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-InputMap2.PNG' | relative_url }})

Add four members to the Collection on the left:

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-PropMap3.PNG' | relative_url }})

Then add the mapping. __Name__ will show a drop-down menu of the properties from the _CreateGratingTrial_ node that can be set. And choose the corresponding output from the ExpressionTransform node under __Selector__ :

![]({{ '/assets/Images/GratingSeries/GratingSeriesB1-PropMap4.PNG' | relative_url }})


The page [Stimulus Series]() has a more generic version of creating the same stimulus, without the benefit of having the additional nodes for creating grating stimuli.
