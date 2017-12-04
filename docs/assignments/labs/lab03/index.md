---
title: Lab 03 - Reproducing Maps - Geologic Map
---

### Introduction to Lab

#### Background

In this lab you will be provided with raw vector and raster data and you will be required to use editing and display tools to reproduce a portion of an existing geologic map in a professional manner. The trick to making it look good you'll find is NOT to do it all in ArcGIS! You will also be exposed to some basic spatial analysis tools to pull quantitative information off of the provided data sets. This lab explains the workflow in some detail as to highlight very specific tips and tricks associated with making maps documents and doing basic spatial analyses. Having now struggled with manipulating your maps in Arc, you will hopefully appreciate some of the added functionality you will be exposed to in this lab.

We will use some data from the [Utah Geologic Survey](http://geology.utah.gov/) from the 30' x 60' Logan Quad to reproduce a geologic map for an area of interest to us.

![Logan3060]({{ site.baseurl }}/assets/images/Logan3060.PNG)

#### Data for Lab

Navigate to the Utah Geological Survey website (http://geology.utah.gov/) and use the navigation menu on the left to browse to ‘Databases & Data’ -> ‘GIS Geologic Map Data’ and scroll down to download the 30’ x 60’ Logan Quad as a GIS zip file. Unzip all the data to [wherever you are working]({{ site.baseurl }}/assignments/labs/lab01/getting-organized-and-oriented/file-management) for Lab 3 (e.g. in a 

```
Lab03\Raw_Data
```

 folder). 

Prerequisites

- [Lab 01]({{ site.baseurl }}/assignments/labs/lab01)
- [Lab 02]({{ site.baseurl }}/assignments/labs/old-labs/Georeferencing) is helpful but not necessary

### Lab Objectives

1. To teach you how to manipulate display properties and symbology to reproduce a map in as close as possible a fashion to the original.
2. To teach you how to extract summary statistics and data from existing data
3. Learn how to make professional maps not just using ArcGIS, but by leveraging the power of a vector graphics application (e.g. Adobe Illustrator)

This lab helps fulfill [primary learning outcomes]({{ site.baseurl }}/about/primary-learning-outcomes) 2 & 4.

## Lab Tasks

1. Reproduce a portion of the 1:100,000 scale Logan 30’ x 60’ covering portions of Smithfield, Logan, and Logan Canyon up to Wood Camp at 1:100,000 scale on an 8.5” x 11” sheet.

2. For the above, report the areas and relative portions of each rock unit.

Detailed Instructions[Task 1: Reproduce Geologic Map]({{ site.baseurl }}/assignments/labs/lab03/task-01---reproduce-geologic-map)[Old Instructions (text)]({{ site.baseurl }}/assignments/labs/lab03/task-01---reproduce-geologic-map/old-instructions-text)[Task 2: A simple area calculation]({{ site.baseurl }}/assignments/labs/lab03/task-2-a-simple-area-calculation)

### What to Submit

 personal website

 

- Shows an appropriately sized PNG image of your reproduced map;

- Makes a high resolution, but correctly scaled version available as a PDF;

- Provides all the necessary context in the form of a write-up which should include:

- - context for your geologic map

  - context for your Task 2 area calculations

  - results of your Task 2 calculations including

  - - table with rock units greater than 5% of total map area
    - text as appropriate to report your findings.

Your task one map should end up looking something like:

#### Example Map

[![Lab03_GeologicMapDEMO]({{ site.baseurl }}/assets/images/Lab03_GeologicMapDEMO.png)]({{ site.baseurl }}/assets/images/hr/Lab03_GeologicMapDEMO.png)

Make sure your lab conforms to the general [lab submission guidelines](http://a/joewheaton.org/gis-wats-4930-6920/labs#TOC-Lab-Submission-Guidelines). Submit a URL for your webpage for this lab to Canvas under Lab 3.

### Additional Resources

#### Lab Introduction Lecture Slides

[![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1325801572897/assignments/labs/lab01/PDF_Icon.png)]({{ site.baseurl }}/assignments/labs/lab01/PDF_Icon.png?attredirects=0)[ Lab 3 Slides](http://etal.usu.edu/Courses/GIS/2013/Lab/ppt/4930_wk03_geolmap.pdf) - Shannon Belmont (2013)

#### Tutorial or Step-by-Step Instructions for Specific Tasks

- [Making a Geologic Map with ArcGIS](http://opentopo.sdsc.edu/shortcourses/GSA_2009_Course_515/GeologicMap_ArcGIS%20Tutorial.pdf) - *Tutorial by Mike Oskin – November 23, 2009*
- [Geologic Mapping Template](http://resources.esri.com/mapTemplates/index.cfm?fa=codeGalleryDetails&scriptID=16317) - *A Geologic Mapping Template for ArcGIS*
- [Methods to Create ArcMap® Styles with Examples for Lithology and Time](http://pubs.usgs.gov/of/2005/1314/) - *U.S. Geological Survey Open-File Report 2005-1314. By Lorre A. Moyer, Jordan T. Hastings, and Gary L. Raines*
- [Labeling Strike & Dip](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//003s00000043000000.htm)*- ArcGIS Help*

