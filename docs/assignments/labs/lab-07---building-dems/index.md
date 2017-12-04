---
title: Lab 07 - Building DEMs
---

### Introduction to Lab

#### Overview

During this lab you will work on building, displaying and manipulating digital elevation models (DEMs). You will build on what you learned in last week's lab, but this time build your own DEMs from raw topographic survey data. The skills you develop are critical in terms of understanding how to convert raw vector data into interpolated surfaces from which additional spatial analyses can be done. Although we use elevation as the 3D data to build a surface from, these same skills apply to any type of spatial data you can interpolate (e.g. temperature, pressure, habitat quality, gravity, etc.). 

#### Prerequisites

The only prerequisite for this lab is a basic proficiency in using ArcGIS 10 (e.g.[ Lab 1]({{ site.baseurl }}/assignments/labs/lab01) and [Getting Oriented]({{ site.baseurl }}/assignments/labs/lab01/getting-organized-and-oriented)). It is also expected that you are familiar with the[ 6 C's]({{ site.baseurl }}/about/grades#TOC-The-Six-C-s-Rubric) to make effective maps.

### Lab Objectives

This lab is intended to make you proficient in  the construction of DEMs from raw topographic survey data . The lab not only gives you experience working with DEMs, but many of the skills you develop here are more generally applicable to dealing with raster datasets in general. By the end of the lab, you will have:

1. Worked with raw topographic data in common formats
2. Built a high-resolution DEM from raw topographic survey data (ground-based)
3. Built a high-resolution DEM from processed airborne LiDaR data (remotely-sensed)
4. Run a simple change detection analysis on multiple year DEMs

Meets [Course Learning Outcomes]({{ site.baseurl }}/about/primary-learning-outcomes) 2, 3 & 5. 

### Instructions & Lab Tasks

**As with all labs... This is a fictitious scenario!**

You are still working for the environmental consulting firm (Big Cheese Watershed Management) which specializes in watershed management. Your boss asked you to build some DEMs from raw data provided by a client for a new project in Oregon and he  wants you to put together your figures and findings on a couple of project pages (your lab pages).  The pages will be used to  illustrate for the client the variety of DEM data available for their project and to help them understand the differences between the data types. 

His vague instructions and context can be summarized as follows:

###  Bridge Creek Watershed Monitoring at Pats Cabin Reach (Tasks 1 & 2)

"We got another project out in Central Oregon working for NOAA as part of their [ISEMP](http://www.nwfsc.noaa.gov/research/divisions/cbd/mathbio/isemp/projects_bridge_creek.cfm) program. We'll be helping them make sense of some monitoring data from restoration work they are doing out there. They had an airborne LiDaR flight flown back in 2005 of the whole stream and they've been monitoring individual stream reaches within this area with rtkGPS topographic surveys since then. They have not built DEMs of their data yet and I want to take one of their reaches (Pats Cabin Reach) and show them what we can do with their data."  

#### Task 1: Build DEM from GPS Data of Pats Cabin Reach

"They've given us their raw GPS survey data, which includes both the individual topographic survey points and breaklines they surveyed in and some water's edge data. Build a DEM of the reach and overlay a water depth map on it."

#### Task 2: Build DEM of Valley around Pats Cabin Reach from LiDaR

"That LiDaR survey they had flown back in 2005 was by [Watershed Sciences](http://www.watershedsciences.com/), and is now publicly available on the Open Topography portal. Go download the raw bare earth point data and construct a DEM for the same reach to provide a little more landscape context and demonstrate the resolution differences between the raw survey data and Lidar."

#### Task 3: Analyze DEMs to detect change in channel over time

"There has been a lot of geomorphic activity along this reach. Analyze the DEMs to quantify change in the channel and map the areas of erosion and deposition. Then build a tool to automate this change detection analysis process for the rest of us."

#### Detailed Instructions: Translation of Your Boss's Vague Instructions

- [Task 1 - Ground Based Topography]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/tas)
- [Task 2 - Airborne LiDaR]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-4)
- [Task 3 - Change detection analysis]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-5)

### What to Submit

Prepare a webpage(s) for this lab on your personal website for the course and prepare the following within that page or subpages:

- For Task [1]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/tas):

- - Set of informal figures illustrating

  - - the raw topographic survey data (i.e. points and breaklines) and
    - the TIN, 
    - Descriptively caption figures for full credit

  - **Provide a figure that makes a formal comparison illustrating the differences between DEMs derived from the same TIN at different resolutions **(e.g. 0.05 m, 0.10 m, 0.15 m, 0.20 m, 0.25 m, 1.0 m, ) (NOTE: choose a scale/extent that illustrates the differences at **all** **resolutions - focus on a feature**)

  - Choose the most appropriate resolution at which to model this topography with a raster DEM. Justify your choice in a brief discussion about the resolution of the raw survey data and what you know about raster creation processes.

  - Provide a figure displaying your final DEM (of resolution chosen for analysis) w/ water depth layer (include resolution in figure caption)

  - Provide links to higher resolution JPG or PDFs** if** the images on your webpage don't show relevant details. 

- For Task [2]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-4):

- - **In a well marked section provide a brief explanation about the differences between the DEM created from raw survey data in Task 1 and the LiDAR DEM created in Task 2 with respect to channel change detection. What are the pros and cons of each?**  (Use additional figures to illustrate your points if necessary.)  *Specifically, with the goal of analyzing the surface to detect changes in channel morphometry, address whether the airborne LiDAR would be more or less effective than the survey DEM.  Incorporate what you've learned about airborne LiDAR and the survey data, and think about data extent, resolution, and what types of features can or can't be resolved by each data set to support your decision to use one or the other for change detection analysis.*

- For Task 3: 

- - **Provide a figure that effectively displays the results of your change detection analysis**

  - - include appropriate context (descriptive caption, scale, location)
    - **Use LiDAR DEM from Task 2 as your base layer.**

  - Provide a screenshot of your model with a caption that fully describes how the model works and what it does.

  - Provide a link to download the DoD model/toolbox you created. 

Make sure your lab conforms to the general [lab submission guidelines](http://a/joewheaton.org/gis-wats-4930-6920/labs#TOC-Lab-Submission-Guidelines). Submit a URL for this lab's webpage.

### Additional Resources

#### Lab Introduction Slides

[![img]({{ site.baseurl }}/_/rsrc/1325801572897/assignments/labs/lab01/PDF_Icon.png)]({{ site.baseurl }}/assignments/labs/lab01/PDF_Icon.png?attredirects=0) [Lab 7 Slides](http://etal.usu.edu/Courses/GIS/2013/Lab/ppt/4930_wk07_DEM_build.pdf) - Shannon Belmont Spring 2013

#### Where to get DEM Data:

- USGS  [National Map Seamless Server](http://seamless.usgs.gov/index.php) - *Download various elevation datasets 10 m, 30 m and 90m for entire country *
- [USDA’sGeospatial Data Gateway](http://datagateway.nrcs.usda.gov/) - *You can also download 10 m and 30 m DEMs from here (much easier to use then National Map Seamless Server)*
- [Open Topography Portal](http://opentopography.org/) - *This is primarily just high resolution LiDaR data, but very useful if it happens to fall within your study area.*
- [Utah GIS Portal Elevation Datasets](http://gis.utah.gov/elevation) *- In Utah, we have access to a lot of great DEM datasets that other states do not!*
- [Columbia Habitat Monitoring Protocol](http://champmonitoring.org/) - *Has total station survey data for 100's of sample reaches similar to Task 1 throughout the Columbia Basin*

#### Information on Topographic Survey Technologies

- [LiDaR Technology & Applications Course Pag](https://www.e-education.psu.edu/lidar/resources/l1.html)e - This is a course web page for a LiDaR course taught at Penn State. It is an excellent resource of information to learn more about how LiDaR data is acquired and what can be done with it.

#### Follow up Activities:

- [Introduction to 3D Analyst Tutorials](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Introduction_to_the_ArcGIS_3D_Analyst_tutorial/00q800000093000000/)
- [3D Visualization Techniques Using ArcGIS 10](http://training.esri.com/acb2000/showdetl.cfm?DID=6&Product_ID=997) - This one isn't free.
- Using ArcGIS 9.3.X to Construct and Manipulate DEMS -![img](http://www.joewheaton.org/_/rsrc/1288548319243/lab/unlisted/IPC_GCD/pdf_icon.gif) [Tutorial ](http://etal.usu.edu/ICRRR/PartII/2010/Part_II/ICRRR_D2_Topo_Excercise.pdf);![img](http://www.joewheaton.org/_/rsrc/1288548319243/lab/unlisted/IPC_GCD/zip_icon.gif) [Data](http://etal.usu.edu/ICRRR/PartII/2010/Part_II/ProvoTopoData.zip) (Part of ICRRR [Part II Short Course](http://www.cnr.usu.edu/streamrestoration/htm/course-information)) -  *I prepared this for ArcGIS 9.3x and it is very similar to Task 1.*

### ArcGIS 10 References

- [Fundamentals of Surfaces](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Fundamentals_of_Surfaces/00q80000005z000000/)- ESRI Help Document
- [Building a TIN to represent a Terrain](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Exercise_4_Building_a_TIN_to_represent_terrain/00q8000000w1000000/) - ESRI Help Tutorial
- [Creating and Using a Terrain Dataset](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Exercise_8_Creating_and_using_a_terrain_dataset/00q800000007000000/) - ESRI Help Tutorial

Subpages (3): [Task 1 - Ground Based Topography]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/tas) [Task 2 - Airborne LiDaR]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-4) [Task 3 - Change detection analysis]({{ site.baseurl }}/assignments/labs/lab-07---building-dems/task-5)

