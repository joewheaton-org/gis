---
title: Georeferencing
---

### Introduction to Lab

#### Background

One of the many powers of GIS is combining various data based on spatial location.  Information can be obtained from aerial imagery or scanned maps, but to correctly overlay other layers of data, spatial reference or a coordinate system must be defined for, and assigned to, the aerial imagery or scanned maps.  This is the process of [georeferencing](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Fundamentals_for_georeferencing_a_raster_dataset/009t000000mn000000/): aligning some type of raster imagery to a map coordinate system.  This workshop works through two exercises on georeferencing raster imagery, intended to reinforce some of the coordinate system and projection principles we cover in week 2, as an example from which to build good maps from existing data. 

#### Prerequistites

- Completion of [Lab 01]({{ site.baseurl }}/assignments/labs/lab01).  It is also expected that you are familiar with the[ 6 C's]({{ site.baseurl }}/about/grades#TOC-The-Six-C-s-Rubric) to make effective maps.

------

### Lab Objectives

 The two primary objectives of this lab are to 1) teach you how to georeference rasters and 2) reiterate building persuasive and convincing maps. 

During this workshop you will learn how to take digital images or maps that are not georeferenced and georeference (or register) them onto an appropriate coordinate system.  Upon completion of the workshop exercise, you will have: 

1. Georeferenced a scanned historical aerial photo to allow you to overlay it on a map
2. Georeferenced a digital aerial photo collected from a small blimp (like the one you will use next week) using control points.

------

### Lab Tasks

 This week, you are working for an environmental consulting firm who specializes in watershed management. Your boss has asked you to georeference the photos provided for Sulphur Creek (in California) and he would like you to: 

1. Produce a good map showing a correctly georeferenced historical aerial photo from 1953 side-by-side with a provided 2002 aerial photograph.
2. Produce a good map showing a correctly georeferenced aerial photograph from a 2006 blimp survey of the channel survey area on Sulphur Creek.

#### Sulphur Creek Watershed

<iframe src="https://www.google.com/maps/embed?pb=!1m10!1m8!1m3!1d40859.65423114738!2d-122.50179599999998!3d38.486929!3m2!1i1024!2i768!4f13.1!5e1!3m2!1sen!2sus!4v1515090486163" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>

You are provided with the following new data (in[ Georeferencing_StHelena.zip](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab09/Georeferencing_StHelena.zip)![img]({{ site.baseurl }}/_/rsrc/1357494636601/assignments/labs/old-labs/Georeferencing/zip_icon.gif)): 

 

- For Task 1, you are provided with a correctly georeferenced aerial photograph from 2002 (`2002_SulphurCreek_AP.tif`).
- For Task 1, you are provided with a non-georeferenced scanned historical aerial photograph of roughly the same area (`1953_StHelena_AP.jpg`).
- For Task 2, you are provided with a non-georeferenced image acquired from a digital camera mounted to a blimp flown in 2006 over the topographic survey area of the channel (`2006_BlimpPhoto.jpg`). You will notice that this image has six control targets (numbered) visible in it. You are also provided with an ASCII file that provides the coordinates of these targets, which were surveyed concurrently with the topographic survey (`2006_Blimp_Targets.asc`).

------

#### Task 1 - Georeferencing a Scanned Historical Image

You need to georeference a scanned historical image (`1953_StHelena_AP.jpg`) based on establishing control points in a more recent (`2002_SulphurCreek_AP.tif`) correctly georeferenced image. This means that the new georeferenced image you produce will take on the coordinate system and projection of the more recent image. You should also assess how good a job you did at georeferencing the imagery, and create a map that convinces your boss that you did the georeferencing correctly. See [here]({{ site.baseurl }}/assignments/labs/old-labs/Georeferencing/task-1-georeferencing-a-scanned-historical-image) for detailed instructions. 

#### Task 2 - Georeferencing a Digital Aerial Photograph

In this task you will take an image acquired from an aerial platform (`2006_BlimpPhoto.jpg`) and georeference it using aerial targets visible in the image, which correspond to known ground coordinates (`2006_Blimp_Targets.asc`). Again, you will need to assess how good a job you did at georeferencing and create a convincing map. See [here]({{ site.baseurl }}/assignments/labs/old-labs/Georeferencing/task-2-georeferencing-a-digital-aerial-photograph) for some instructions.

------

### What to Submit

Prepare a webpage for this lab on your personal website for the course, which presents the results of Tasks 1 & 2 with attention paid in both your maps and write-up to convincing your boss you understand the process of georeferencing and that you did the tasks correctly.

- Map 1 - present the results of Task 1, two georeferenced images (historical and currect) side by side with the results of the land use mapping.


- - To be convincing, your map should make this comparison very easy and should include elements that work to illustrate the correctness of the georeferencing analysis (grid, matching extents and scale, RMS error, etc.)
  - Symbology for the land use map should be intuitive, effective, consistent, and work towards convincing that mapping was done correctly.
  - On your map you should report the transformation method used and total RMS error from the georeferencing.  Also report the total area Urban, Agricultural, and Undeveloped for each year (in percent total area), the percent increase or decrease in change over time for each land use type, and a confidence threshold associated with your land use mapping results. 


- Map 2 - present the results of Task 2, georeferencing the digital aerial photo

- - Again, to be convincing, your map should demonstrate the correctness of the analysis and be convincing.  Include final RMS error on your map (in addition to any other elements that would help convince transformation and resampling were done correctly).


- Decide what is the most effective way to layout your results with a combination of images and/or PDFs for your map(s) and enough contextual text to explain what was asked of you (i.e. introduction and purpose), how you addressed it (i.e. methods), what you produced (i.e. results) and your analysis/interpretation of how well this worked (i.e. discussion). *Discussion should include subjectivity and related uncertainty in your analysis to justify the confidence threshold you applied to your results of the land use mapping.*


- There is no need to build an interactive Google Map for this exercise.

Make sure your lab conforms to the general [lab submission guidelines](http://a/joewheaton.org/gis-wats-4930-6920/labs#TOC-Lab-Submission-Guidelines). Submit a URL for this lab's webpage.

------

### Suggested Instructions & Workflows

#### Workflows

[Task 1: Georeferencing a Scanned Historical Image]({{ site.baseurl }}/assignments/labs/old-labs/Georeferencing/task-1-georeferencing-a-scanned-historical-image)
[Task 2: Georeferencing a Digital Aerial Photograph]({{ site.baseurl }}/assignments/labs/old-labs/Georeferencing/task-2-georeferencing-a-digital-aerial-photograph)

### Additional Resources

#### Lab Introduction Slides

[![img]({{ site.baseurl }}/_/rsrc/1325801572897/assignments/labs/lab01/PDF_Icon.png)]({{ site.baseurl }}/assignments/labs/lab01/PDF_Icon.png?attredirects=0) [Lab Slides](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab09/WATS4930_2012_wk9.pdf) - Shannon Belmont

#### Tutorial or Step-by-Step Instructions for Specific Tasks

- [Fundamentals for Georeferencing a Raster Dataset](http://www.google.com/url?q=http%3A%2F%2Fhelp.arcgis.com%2Fen%2Farcgisdesktop%2F10.0%2Fhelp%2Findex.html%23%2F%2F009t000000mn000000.htm&sa=D&sntz=1&usg=AFrqEzfMsZz0NlIPP0ohZ6ZuhEbw7yXCjA) - *From ArcGIS 10 Help*
- [Georeferencing a Raster Dataset](http://www.google.com/url?q=http%3A%2F%2Fhelp.arcgis.com%2Fen%2Farcgisdesktop%2F10.0%2Fhelp%2Findex.html%23%2FGeoreferencing_a_raster_dataset%2F009t000000mq000000%2F&sa=D&sntz=1&usg=AFrqEzfA1dKA-gQKNSazqk-hO5mPtW2beQ) - *From ArcGIS 10 Help. This is what you need for Task 1.*
- [Entering Specific X,Y Coordinates when Georeferencing](http://www.google.com/url?q=http%3A%2F%2Fhelp.arcgis.com%2Fen%2Farcgisdesktop%2F10.0%2Fhelp%2Findex.html%23%2FEntering_specific_x_y_coordinates_when_georeferencing%2F009t000000mr000000%2F&sa=D&sntz=1&usg=AFrqEzeFXFR03QwXgU3Y7rL1CaqcVGyjYQ) *- From ArcGIS 10 Help. This is what you need to do for Task 2*

#### Web Links:

- Grossinger R, Striplen C, Brewster E and McKee L. 2003. [Ecological, Geomorphic, and Land Use History of Sulphur Creek Watershed: A component of the watershed management plan for the Sulphur Creek watershed, Napa County, California](http://www.napawatersheds.org/files/managed/Document/2398/Sulphur%20Draft%20HE%20report%20Final%20v1.pdf). A Technical Report of the Regional Watershed Program, San Francisco Estuary Institute, Oakland, CA, 51 pp. 
- [Watershed Information Center & Conservancy of Napa County](http://www.napawatersheds.org/)