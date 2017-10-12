---
title: Week 03: Working with Data in GIS
---

#### Important Dates & Links

**Lecture Date(s):**

*See Calendar*

------

**Reading Assignments**

[See Here for Reading Assignments](http://gis.joewheaton.org/assignments/reading-assignments-2010)

------

Lab Assignment(s)

- [Lab 03 - Reproducing Maps - Geologic Map](http://gis.joewheaton.org/assignments/labs/lab03)

------

### Background

#### Introduction to Data

GIS is all about data and until you appreciate how to manage that data, you can never really unlock the power of GIS. Both GIS and CAD (computer assisted drafting) can be used to make maps (in CAD often thought of instead as a plan). Both rely on the concept of layers to overlay information (see left). The fundamental difference between GIS and CAD is the way in which they represent spatial objects on these layers. In CAD, you draw spatial objects (e.g. lines, polylines, polygons, solids, etc.) that are referred to as entities and these reside in a drawing. By contrast, in GIS you don't draw per se, but instead you load a reference to data (e.g. in [ArcMap](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_ArcGIS_Desktop/00v200000005000000/) you use the [Add Data tool ](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Adding_layers_to_a_map/00660000000t000000/)![img](http://gis.joewheaton.org/_/rsrc/1294288375649/topics/data/AddData.png)), which you choose how you want to display. Although CAD can be used to do GIS-type things, and GIS can be used to draw, neither are very good at doing what the other was fundamentally designed to do. In CAD you can draw very accurately and precisely with a multitude of options. This is extremely useful for design work, in which you want to create something. **In GIS, spatial data lies behind everything.** GIS is much more powerful then CAD when it comes to doing analyses, querying data, and managing large quantities of data. Over the next two weeks, we will help you better understand where data comes from and how it is manipulated in GIS.

#### The power of layers in GIS:
![GUID-5BD98316-8BF4-430C-BA24-F47EFF8BF66D-web]({{ site.baseurl }}/assets/images/GUID-5BD98316-8BF4-430C-BA24-F47EFF8BF66D-web.png)

#### Why we're Covering it

You should be aware of the plethora of data sources from which you can get GIS data and use it for context or analysis, and how to edit and make your own data. ArcGIS makes some of these choices so easy for you that you can get yourself in trouble. These skills will be crucial in your [projects](http://gis.joewheaton.org/assignments/project) and the if you intend to use GIS in your career to do more than just make location maps (i.e. [lab 01](http://gis.joewheaton.org/assignments/labs/lab01)).

#### Learning Outcomes

These lectures, readings and Labs [03](http://gis.joewheaton.org/assignments/labs/lab03) & [04](http://gis.joewheaton.org/assignments/labs/lab04) all help fulfill [primary learning outcomes](http://gis.joewheaton.org/about/primary-learning-outcomes) 1, 2, 3 & 4.

### Lectures and Podcasts

#### Quiz 2

Did you like Quiz 2? Most people find it frustrating and time consuming. However, it really puts into practice the concepts we talked about last week with projections and coordinate systems on a paper map. If you'd like further explanation on the Quiz answers, check out [this PODCAST](http://gis.joewheaton.org/topics/data/quiz-2-feedback-podcast).

#### Vector Data, Editing & Attributing Data + Metadata

At some point, you will want to modify some data someone gave to you, and you'll need to know about editing. In ArcGIS, editing is both 'editing' and another way of saying drawing. We will cover the somewhat confusing workflows and terminology that unlock the door to making GIS a much more powerful tool for you.As far as topics go, metadata is about as dull as it gets.... However, without it a lot of data is worthless. We will go over how to use metadata and how and when you should produce your own metadata. We will then talk about how this metadata is critical to displaying data correctly.

* [2015 Lecture Slides](http://etal.usu.edu/Courses/GIS/2015/Lectures/2_EditingAtributingDataMetadata.pdf)  - PDF 

* - See [here for individual topic PODCASTs](http://gis.joewheaton.org/topics/data/vector-data-podcast) or watch [whole series](http://youtube.com/watch?v=-9I3VWMZ1SQ).

Previous:

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/topics/goog_930015760)[ Thursday Lecture](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week03/3_EditingAtributingDataMetadata.pdf)  - PDF 

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) 2013 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2013/Lectures/Week_04/3_EditingAtributingDataMetadata.pdf)  - PDF 

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) 2012 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/3_EditingAtributingDataMetadata_2PP.pdf) - PDF w/ 2 slides per page

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) 2012 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/3_EditingAtributingDataMetadata_6PP.pdf) - PDF w/ 6 slides per page 

- - 2012 [Video of Lecture](http://youtu.be/djawcbprGIg)

#### NOT THE PODCAST! - 2012 Lecture For Reference

<iframe width="560" height="315" src="https://www.youtube.com/embed/djawcbprGIg" frameborder="0" allowfullscreen></iframe>

#### Raster Imagery, Data Sources & Intro to Remote Sensing

We will go through an overview of raster imagery basics with a review/intro to remote sensing. We'll then talk about some of the places you can acquire raster and vector data to use in your own maps (e.g. for the [Reproducing Maps... Geologic Map lab](http://gis.joewheaton.org/assignments/labs/lab03)).

*  [2015](http://etal.usu.edu/Courses/GIS/2015/Lectures/1_RasterImagery_DataSources.pdf)[ Lecture Slides](http://etal.usu.edu/Courses/GIS/2015/Lectures/1_RasterImagery_DataSources.pdf)  - PDF 

* - See [here for individual PODCASTs by Topic](http://gis.joewheaton.org/topics/data/raster-data-podcast) or [here for whole series](http://youtu.be/BA6ZEqh2QWo?list=PL0ZiZg4rilzKtluJ99W0DYC7aw9zKmzTB).

Previous:

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/topics/goog_1621448348)[ Thursday Lecture](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week03/1_RasterImagery_DataSources.pdf)  - PDF 

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) 2013 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2013/Lectures/Week_03/1_RasterImagery_DataSources.pdf)  - PDF 

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) 2012 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/1_RasterImagery_DataSources_2pp.pdf)  - PDF w/ 2 slides per page 

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) 2012 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/1_RasterImagery_DataSources_6pp.pdf) - PDF w/ 6 slides per page

- - 2012 [Video of Lecture](http://youtu.be/B_94S2hnDDA)

#### NOT THE PODCAST! - 2012 Lecture For Reference

<iframe width="560" height="315" src="https://www.youtube.com/embed/B_94S2hnDDA" frameborder="0" allowfullscreen></iframe>

#### TLS Demo - Getting Lots of Vector Data

This year we did the TLS Demo and Synthesis of GIS Fundamentals in One Go

[2015](http://gis.joewheaton.org/topics/goog_136810839)[ Thursday Lecture](http://etal.usu.edu/Courses/GIS/2015/Lectures/3_TerrestrialLaserScanning.pdf)  - PDF 

Previous Years: 

- 2014 ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/topics/goog_930015760)[ Thursday Lecture](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week03/4_TerrestrialLaserScanning.pdf)  - PDF 
- 2012 ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [Thursday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2005%20-%20Vector%20Analyses/2_TerrestrialLaserScanning_2PP.pdf)  - PDF w/ 2 slides per page 
- 2012 ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [Thursday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2005%20-%20Vector%20Analyses/2_TerrestrialLaserScanning_6PP.pdf) - PDF w/ 6 slides per page
- 2012 [Video of Lecture](http://youtu.be/EDtIFOto5cs)

#### NOT THE PODCAST! - 2012 Lecture For Reference

<iframe width="560" height="315" src="https://www.youtube.com/embed/EDtIFOto5cs" frameborder="0" allowfullscreen></iframe>

### Additional Resources

#### Data Sources

- [GIS Data Links](http://www.joewheaton.org/river-links/gis-data) - *This is a page I maintain with some links to downloadable GIS Data sources*
- [GIS Class LibGuide](http://libguides.usu.edu/content.php?pid=176243&sid=1484011) - *This is a custom page our librarian has put together just for this class!*
- [Datasets Provided with ArcGIS](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_ESRI_Data_and_Maps/001z00000002000000/) -  *These are known as ESRI Data and Maps*
- [A quick tour of ArcCatalog](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/A_quick_tour_of_ArcCatalog/006m00000001000000/) - *ArcCatalog is the place to manage and browse your GIS data with ArcGIS*
- [Adding data from ArcGIS online](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Adding_data_from_ArcGIS_online/006600000441000000/) - *There are wealth of great basemap layers you can now load into your maps without having to download anything! Very convenient!*

#### WMS - Web Mapping Services

You can add data directly into ArcGIS from a WMS. See here for how to add a WMS in ArcGIS.

- [WMS from the Seamless Data Warehouse](http://seamless.usgs.gov/services.php) (includes National Elevation Dataset, Landcover and Imagery)
- [Virtual Utah](http://earth.gis.usu.edu/utah/wms.html) - from RSGIS Lab
- [Inside Idaho WMS](http://insideidaho.org/webservices.html)
- [Oregon Imagery Explorer](http://oregonexplorer.info/imagery/AccesstheImagery/StreamImagery)
- [GEBCO Web Map](http://www.gebco.net/data_and_products/gebco_web_services/web_map_service/) - General Bathymetric Chart of the Oceans
- [OGC Public WMS Server List](http://www.skylab-mobilesystems.com/en/wms_serverlist.html)

#### Metadata & Displaying Data

- [What is metadata?](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_metadata/003t00000001000000/)
- [A quick tour of metadata](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//003t00000002000000.htm)
- [Editing Metadata](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Editing_metadata/003t0000000n000000/) (in ArcGIS)

#### Editing & Attributing Data

- [What is editing](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_editing/001t00000001000000/) (in ArcGIS)
- [A quick tour of editing](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/A_quick_tour_of_editing/001t00000002000000/) (in ArcGIS)
- [About creating and editing annotation](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/About_creating_and_editing_annotation/001t000000pm000000/) (in ArcGIS)
- [About editing attributes](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/About_editing_attributes/001t000000m1000000/) (in ArcGIS)

