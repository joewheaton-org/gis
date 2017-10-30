---
title: Lab 04 - Digitzing, Editing, Sharing Data & Intro to Geoprocessing
---

### Introduction to Lab

#### Background

The Forest Service has funds to create a new campground.  The site will be located in northern Utah, on the east side of the Wasatch Range, north of Liberty.  You have been tasked with creating a map to present a campground of your own design, reporting some development specifics, and making your plan (a map) and GIS files available via your website. 

The manipulation and creation of vector data (points, polylines and polygons) is a fundamental part of your GIS toolkit. In ArcGIS, the manipulation, modification, drawing, and digitizing of vector data is referred to as editing. We need to build proficiency in these tasks before we can do vector-based spatial analyses (i.e. [Lab 05](http://gis.joewheaton.org/assignments/labs/lab05) & [Week 05](http://gis.joewheaton.org/topics/vector-analyses)). 

#### Potential Campground Site, Liberty, Utah

<iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d210336.77310429767!2d-111.790363!3d41.448546!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDHCsDIxJzI0LjYiTiAxMTHCsDUzJzE5LjIiVw!5e1!3m2!1sen!2sus!4v1509377102060" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>

#### Lab Objectives

- Edit existing vector data layers
- Create new vector data layers and edit them (e.g. digitizing)
- Edit and create tabular data
- Share vector and tabular data with other GIS users
- Learn how to use Model Builder & Geoprocessing

Meets [Course Learning Outcomes](http://gis.joewheaton.org/about/primary-learning-outcomes) 2, 4 & 5. 

### Lab Tasks Overview

#### IMPORTANT

**Help! I am getting an error saying I don't have the required license to run the Zonal Statistics tool!**

You will need to **activate the Spatial Analyst** extension to run some of the tools needed in this lab.

​    In ArcMap > Customize drop down > Extensions > check all the boxes and close.

You will have to do this with *every time* you log into the Quinney labs and once per install on your personal computer.

#### Task 1 - Create Campground Design Map

You will design a campground for the US Forest Service at a specific site near Liberty Utah (approximate location: 425,666 E 4,578,749 N meters in the NAD 83 UTM Zone 12N coordinate system).   

- Use the above coordinates to find the location of the campground.
- Create campground and campsites using point and polygons
- Create trails, roads, or paths, using polylines
- Populate an attribute table with details about the campsites
- Determine dominant vegetation and landcover variety for this campground plus 5 alternative sites
- Present design and landcover results

You will need to *create* 3 shapefiles: 

- a polygon layer for digitizing the campground, 
- a point layer that will represent the specific layout of the campsites, and 
- a polyline shapefile for trails. 

See the “what to submit” section below for map details.  

Click [here](http://gis.joewheaton.org/assignments/labs/lab04/task-1-specific-instructions) for specific instructions for Task 1.

#### Task 2 - Share GIS Data for Campground Design in Different Formats

There are many ways to share your vector data, and/or map including:

- `*.KML/KMZ` - Keyhole Markup Language format (i.e. Google Earth)
- `*.mxd` Map Document with all associated data files 
- *.MPK  [Map Package](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//006600000403000000.htm) - bundles map project with all associated data files ([more here](http://www.geomattix.com/blog/what-i-love-about-arcgis-10-map-packages/))
- `*.shp` files Shape files with all dependencies (i.e. `*.dbf, *.prj, *.sbn, *.sbx, *.xml, *.shx`)
- `*.shp` files with `*.lyr` file Shape files and layer file
- File Geodatabase
- File Geodatabase with `*.lyr` file (note that a [`*.lyr `file cannot be saved in a file geodatabase](http://forumsstg.arcgis.com/threads/28274-Saving-Layer-Files-in-a-File-Geodatabase))
- `*.lpk` Layer Package File - Can share on ArcGIS Online (see [here](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_ArcGIS/00v200000007000000/))
- [Sharing Layers in ArcGIS Online](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_ArcGIS/00v200000007000000/).

```
*.MPK
```

For this task, you will only be sharing your project as an ArcGIS Desktop Map Package (`*.MPK` map package) which bundles your map project and all the dependent data files, 

But you need to be familiar and comfortable with each of these file types. 

- How can each of these file formats be described?  
- How do they function?  
- What are the advantages and disadvantages of each of these file formats?   

**To reinforce these concepts, a brief "quiz" accompanies this lab to help promote understanding of these core concepts.**

[Link to Canvas Lab 4 Quiz page](https://usu.instructure.com/courses/360981/quizzes/504498)

Click [here](http://gis.joewheaton.org/assignments/labs/lab04/task-2-details-share-files-with-internal-review-committee) for specific instructions for Task 2.

#### Detailed Instructions

- [Task 1 Details: Create Campground Presentation Map](http://gis.joewheaton.org/assignments/labs/lab04/task-1-specific-instructions)
- [Task 2 Details: Share Files with Internal Review Committee](http://gis.joewheaton.org/assignments/labs/lab04/task-2-details-share-files-with-internal-review-committee)

#### Data for Lab

Data for this lab includes: 

1. a fictional point file containing optional campground sites for Step 4 (data credits S Belmont), and 
2. a landcover layer for Weber County (SWReGAP: http://earth.gis.usu.edu/swgap/landcover.html) for use in Step 4.  

[Lab04_data folder available for download here.](https://usu.instructure.com/files/63543224/download?download_frd=1) (must be logged into Canvas)

------

### What to Submit

- Display a series of figures that represent your proposed campground, campsites, and trails. 

- - Your presentation should have a clear purpose, 
  - celebrate the 6 C's, and 
  - should have clear location context.

- Create an interactive Google Map to display the campground extent and campsites (this could be used as a locator map depending on the scale)

- Display a table containing campsite attributes and second table with results of landcover analysis.


- Along with the URL for your Lab 4 webpage, submit the **map package** to Canvas > Assignment 4 page


- - Map package (`*.MPK):`

  - - map project (*.mxd) with all associated shapefiles and layer files


- Take [Canvas Lab 4 quiz on file type](https://usu.instructure.com/courses/360981/quizzes/504498)s. (Log into Canvas for link to work).

Your webpage should include a brief write up that provides contextual background information about the campground design project.

Make sure your lab conforms to the general [lab submission guidelines](http://a/joewheaton.org/gis-wats-4930-6920/labs#TOC-Lab-Submission-Guidelines). Submit a URL for this lab's webpage.

------

### Additional Resources

#### 

#### Web Links:

- [Recreation.gov](http://recreation.gov/) - *This site has a handy search tool for campgrounds in the U.S.*
- US Forest Service Home Page (<http://www.fs.fed.us/>) - *Main page has a great article about smokejumpers fighting Asian longhorned beetles in their off-time.*