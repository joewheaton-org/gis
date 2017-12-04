---
title: Task 2 - Airborne LiDaR
---

After your experience working with LiDaR DEMs in [Task 2]({{ site.baseurl }}/assignments/labs/lab06-1/task-2) from Lab 6, and building TINs and DEMs in [Task 1]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/tas), this step will be pretty straight forward. Your boss wants you to simply use the Watershed Sciences 2005 LiDaR survey of Bridge Creek to provide some contextual topography for the Pats Cabin Creek and talk about how this might be used in the monitoring. The image below is a [hillshade](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Hillshade/00q900000036000000/) created in [Open Topography](http://opentopography.org/) from that dataset in the vicinity of the Pats Cabin reach on Bridge Creek.

### 

![1297660556218111]({{site.baseurl}}/assets/images/1297660556218111.jpg)

Although you could use [Open Topography](http://opentopography.org/) to build the surface for you, we will show you an alternative method of building a digital elevation model in ArcGIS, where you build a [Terrain](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//005v00000002000000.htm) (instead of a [TIN](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_a_TIN_surface/006000000001000000/)) and then convert it to a [raster DEM](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Surface_formats/00q800000094000000/). 

### Download the Data

We need to download the data from [Open Topography](http://opentopography.org/) for the vicinity of our study reach (Pats Cabin) in Bridge Creek. This video tutorial walks you through how to download that data from [Open Topography](http://opentopography.org/): 

<iframe width="560" height="315" src="https://www.youtube.com/embed/b0LNwZF5bGs" frameborder="0" allowfullscreen></iframe>

This video tutorial walks you through how to import the 

```
*.las
```

 file you download into ArcGIS into a geodatabase (using [*LAS to Multipoint*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00q90000009m000000.htm)):

<iframe width="560" height="315" src="https://www.youtube.com/embed/fLjU6npubng" frameborder="0" allowfullscreen></iframe>

#### Build a Terrain and Convert to DEM

After we have the *.las points imported as a Multipoint feature class, we need to [build a Terrain](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//005v0000001p000000.htm), and then [convert that terrain to a raster DEM](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Terrain_To_Raster/00q90000002t000000/). This video tutorial walks you through those steps:

<iframe width="560" height="315" src="https://www.youtube.com/embed/bB1qVJcAuzQ" frameborder="0" allowfullscreen></iframe>

### What to Submit

You should create a figure that displays the LiDAR DEM with the survey DEM from Task 1. You have some liberty in how you choose to display this data. But consider framing it within the context of channel change detection analysis.  You should think about (and include in your write up) the differences between the survey point DEM created in Task 1 and the LiDAR DEM created in Task 2.   Specifically, with the goal of analyzing the surface to detect changes in channel morphometry, would the airborne LiDAR be more or less effective than the survey DEM?  Incorporate what you've learned about airborne LiDAR and the survey data, and think about data extent, resolution, and what types of features can or can't be resolved by each data set to support your decision to use one or the other for change detection analysis.

Refer to the [What to Submit Section]({{ site.baseurl }}/assignments/labs/lab06-1#TOC-What-to-Submit) for guidelines.

[<-Back to Task 1 ]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/tas)                                                                        [Up to Lab 7]({{ site.baseurl }}/assignments/labs/lab-07---building-dems)[ ^]({{ site.baseurl }}/assignments/labs/lab06-1)                                            [ Ahead to Task 3->]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-5)

