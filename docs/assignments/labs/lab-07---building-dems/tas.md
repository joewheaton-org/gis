---
title: Task 1 - Ground Based Topography
---

### Overview

In this task we are provided with some raw topographic survey data. Your job is to build a DEM from that data (of appropriate resolution), show the water depth overlaid on the DEM, and pull a longitudinal profile and some cross sections off the DEM. You will use a triangular irregular network (TIN) to interpolate between your raw topographic survey data and produce a continuous surface that you will later convert to a raster DEM.

These instructions are for ArcGIS 10 and are primarily provided in the form of video tutorials. As an additional reference, you might find the 'Using ArcGIS 9.3.X to Construct and Manipulate DEMs' tutorial listed in the [main Lab 6 page]({{ site.baseurl }}/assignments/labs/lab06-1#TOC-Follow-up-Activities:) helpful (it uses different data, and is for the old version of ArcGIS, but goes through a similar sequence of steps to arrive at the same end point in Part I of the document; one significant difference is the absence of TIN editing in ArcGIS 9.3.X). 

### Data

Everything you need to create a TIN can be found in the [`PatsCabinSurveyPoints.csv`](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab06/PatsCabinSurveyPoints.csv)* *file and the [`Task3_PatsCabinShapefiles.zip`](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab06/Task3_PatsCabinShapeFiles.zip)![img]({{ site.baseurl }}/_/rsrc/1325810037423/assignments/labs/lab-07---building-dems/tas/zip_icon.gif). This video tutorial goes through what is included in the data and how to import it into ArcGIS:

<iframe width="560" height="315" src="https://www.youtube.com/embed/jb-UY6S6r8I" frameborder="0" allowfullscreen></iframe>

Although not covered in the video tutorial, I would suggest exporting the [`PatsCabinSurveyPoints.csv`](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab06/PatsCabinSurveyPoints.csv)* *table you imported as X-Y points to a shapefile or feature class to use in the construction of the TIN (I named mine `TopoSurveyPoints`).

### Building TINS

#### Your First TIN

In this video tutorial, we go through the simplest form of constructing a TIN from just raw topographic survey point data. We also highlight some of the potential pitfalls to this approach. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/FrXqYazKuAk" frameborder="0" allowfullscreen></iframe>

#### A Better TIN

In this video tutorial, we talk about how you can build a TIN using a polygon hardclip boundary as well as how to manually edit your tin with the TIN Editing Tools.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LoK6lazwGqM" frameborder="0" allowfullscreen></iframe>

#### A Better TIN yet

In this video tutorial, we will use the same data used in our first two TINs as well as the some 3D breakline data provided to you:

<iframe width="560" height="315" src="https://www.youtube.com/embed/x3iCJ9xBocE" frameborder="0" allowfullscreen></iframe>

### Building DEM

Building the DEM is a simple matter of [converting the TIN to a Raster](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00q900000077000000.htm). This video tutorial walks you through the considerations. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/cORkIYUp3_U" frameborder="0" allowfullscreen></iframe>

For this exercise, you need to tell your boss what is an 'appropriate' resolution at which to model this DEM. Thus, you should produce rasters over a range of resolutions.  You could do this manually by running the TIN to Raster tool multiple times.  Or you could employ **Batch Processing**. 

### Batch Processing

Batch Processing makes it possible to run this tool (or any other) over and over without your intervention.  

Right click on the TIN to Raster tool in the 3D Analyst (Conversion > From TIN) toolbox > choose Batch.

![TIN_to_raster_batch]({{ site.baseurl }}/assets/images/TIN_to_raster_batch.png)

Double clicking in the Input TIN  and Output Raster boxes will open new windows that will allow you to browse to your desired input TIN and destination folder.  Name the DEM with name that reflects the resolution (for example, I called mine DEM_01_00 for the 1 meter DEM, DEM_10_00 for the 10 meter, DEM_00_10 for the 10 centimeter, etc.).  

In the Output Data Type, Method, and Sampling Distance boxes, clicking in the window will display a drop down arrow allowing you to choose the correct inputs.  Use the "Add Row" button on the right to add a row for each resolution or DEM output you want to create.  Copy and paste the full paths of the Input TIN and Output Raster files and set the correct inputs for each row.  

Click OK to initiate batch processing of your various DEM resolution output files.

------

### Building Water Depth DEM

Since we have a DEM that includes shots above the water and below the water, and because the survey data denotes where the water's edge shots are, we can derive a bathymetric water depth DEM. The steps are:

1. Build a water surface TIN from the water edge data
2. Convert that water surface TIN into a DEM of the same resolution and extent (i.e. concurrent) as our original DEM
3. Use Raster Calculator to derive water depths by subtracting the lower elevation DEM from the higher elevation water surface.

The resulting water depth map can be overlaid on the DEM to provide a more intuitive context of the physical habitat within the reach as the pools, bars, and beaver ponds jump out more clearly than from the topography alone. This video walks you through the sequence:

<iframe width="560" height="315" src="https://www.youtube.com/embed/hSGW9p570Y8" frameborder="0" allowfullscreen></iframe>

### Pulling Some Cross Sections and a Long Profile Off DEM

Using the 3D Analyst interpolate line and profile graph features, you can easily pull off a longitudinal profile and cross section(s) from the DEM. This video shows you how:

<iframe width="560" height="315" src="https://www.youtube.com/embed/Kv263FBGJnE" frameborder="0" allowfullscreen></iframe>

### What to turn in
See the what to turn in section of the [main lab page]({{ site.baseurl }}/assignments/labs/lab-07---building-dems) for what is expected from Task 1.

​     [Up to Lab 7]({{ site.baseurl }}/assignments/labs/lab-07---building-dems)                                                                 [Ahead to Task 2->]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-4)

