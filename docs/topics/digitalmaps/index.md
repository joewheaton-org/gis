---
title: Week 02 : Abstracting the World to Digital Maps
---

### Background

#### Introduction to Topic

The spatial or geographic representation of the world has to be abstracted into specific data types to be used in GIS. GIS is all about data and until you appreciate how that data is represented digitally you can not make effective maps. Data is added into maps in GIS as layers which can be overlayed.  You can't effectively overlay and display that data unless it is stored in a coordinate system (projected or geographic) that is known.  This week we'll cover the basics of projections as well as handling data in GIS. This video provides a nice illustration of some of the many projections are possible for unfolding the earth off of a globe onto a flat map:

<iframe width="560" height="315" src="https://www.youtube.com/embed/b1xXTi1nFCo" frameborder="0" allowfullscreen></iframe>

One of the most frustrating and typical complaints of GIS students is that *'\**my data just disappeared! **It was there when I saved it now its gone!' *This in indicated by the notorious red exclamation point **!** next to your layer. The reason for this is simple, the link between your [map document](http://www.google.com/url?q=http%3A%2F%2Fhelp.arcgis.com%2Fen%2Farcgisdesktop%2F10.0%2Fhelp%2Findex.html%23%2FEssential_ArcMap_vocabulary%2F006600000003000000%2F&sa=D&sntz=1&usg=AFrqEzecxxHQzJhGOgdcIEtvCmCKIdjtCQ) and the location the data was previously stored has been broken. Many things can break it, and it is easy to [repair](http://www.google.com/url?q=http%3A%2F%2Fhelp.arcgis.com%2Fen%2Farcgisdesktop%2F10.0%2Fhelp%2Findex.html%23%2F%2F00s500000020000000.htm&sa=D&sntz=1&usg=AFrqEzcvPP0X2D5CverWyRmW1W4n-PO4Hw). 

Another common complaint amongst naive and newbie GIS users is that **'my data doesn't lineup when I overlay it!'** This is most typically because a [projection](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//003r00000001000000.htm) and [coordinate system](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Georeferencing_and_coordinate_systems/00v20000000q000000/) was either not or not correctly defined. 

![GIS_BrokenLink]({{ site.baseurl }}/assets/images/GIS_BrokenLink.gif)

This week, we will help you better understand how data is represented in GIS and how those layers are projected to make maps. 

#### Why we're Covering it

You can not make effective use of GIS without an in depth understanding of the a) choices you have in data types to represent your spatial data, and b) the projections & coordinate systems necessary to locate your spatial data correctly. ArcGIS makes some of these choices so easy for you that you can get yourself in trouble. As such, the next two lectures are designed to expose you to each of these aspects, whereas the [lab]({{ site.baseurl }}/assignments/labs/lab-02---coordinate-data-projections-transformations) will put those concepts and theories to practice by having you make some *good* maps with different data types and then taking some unprojected data and [georeferencing](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t000000mn000000.htm) it. 

Although you SHOULD recall most or all of this if you have taken the [prerequisites]({{ site.baseurl }}/about/catalog-description), my past experience has been that most students are very weak when it comes to understanding these fundamentals and it hinders them from progressing as a GIS user. Review never hurts, and we'll take you further and more in depth then you've hopefully gone before.

#### Learning Outcomes

These lectures, readings and Labs [03]({{ site.baseurl }}/assignments/labs/lab03) & [04]({{ site.baseurl }}/assignments/labs/lab04) all help fulfill [primary learning outcomes]({{ site.baseurl }}/about/primary-learning-outcomes) 1 & 2.

### Lectures 

#### 

#### Projections & Coordinate Systems

Here we dive into the details of what allows us to overlay data so seemingly seemlessly in GIS: projections and coordinate systems. Without projections and coordinate systems, GIS would not be possible.

 [2015 Thursday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2015/Lectures/1_Projections&CoordinateSystems.pdf) ; See [here for PODCAST]({{ site.baseurl }}/topics/digitalmaps/1-podcast#TOC-Wrap-up-of-Tuesday-s-Lecture) wrapping up what we did not finish in class:

<iframe width="560" height="315" src="https://www.youtube.com/embed/RkMFaBt1nNI" frameborder="0" allowfullscreen></iframe>

Past Materials:

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014 Thursday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week02/1_Projections&CoordinateSystems.pdf)
- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif)  [2013 Tuesday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2013/Lectures/Week_02/1_Projections&CoordinateSystems.pdf)
-  2012 [Tuesday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2002%20-%20Abstracting%20World%20to%20GIS/1_Projections&CoordinateSystems_2PP.pdf) w/ 2 slides per page 
-  2012 [Tuesday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2002%20-%20Abstracting%20World%20to%20GIS/1_Projections&CoordinateSystems_6PP.pdf) w/ 6 slides per page
- 2012 [Video of Tuesday's Lecture](http://youtu.be/cDHM6va6OKQ)

<iframe width="560" height="315" src="https://www.youtube.com/embed/cDHM6va6OKQ" frameborder="0" allowfullscreen></iframe>

#### Data Types

Here we review what you should already know, but will surely have forgotten because it is not so exciting. We'll try and make it interesting....

- [2015 Thursday Podcast Sides](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week02/2_DataTypes.pdf) - PDF  
- See individual [PODCASTs and topics here]({{ site.baseurl }}/topics/digitalmaps/1-podcast#TOC-Thursday-PODCAST-on-Data-Types) or watch the whole series:

<iframe width="560" height="315" src="https://www.youtube.com/embed/HpKq2WyLwlw" frameborder="0" allowfullscreen></iframe>

Past Materials:

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014 Tuesday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week02/2_DataTypes.pdf)
- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2013 Thursday Lecture - PDF](http://etal.usu.edu/Courses/GIS/2013/Lectures/Week_02/2_DataTypes.pdf)
-  2012 [Thursday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2002%20-%20Abstracting%20World%20to%20GIS/2_DataTypes_2PP.pdf)  - PDF w/ 2 slides per page 
-  2012 [Thursday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2002%20-%20Abstracting%20World%20to%20GIS/2_DataTypes_6PP.pdf) - PDF w/ 6 slides per page
- 2012 [Video of Thursday's Lecture](http://youtu.be/0i2mb2-VCAc)

<iframe width="560" height="315" src="https://www.youtube.com/embed/0i2mb2-VCAc" frameborder="0" allowfullscreen></iframe>

### Additional Resources

Below are some very useful references on projections and coordinate systems from ESRI's online help (ArcGIS Resource Center), which you should browse through and make sure you understand.

- [How a GIS represents and models geographic information](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/How_a_GIS_represents_and_models_geographic_information/00v20000000w000000/)

#### Data Types

- [Three fundamental representations of geographic information layers](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00v200000010000000.htm)

- [About Geographic Data Formats](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/About_geographic_data_formats/00r90000006r000000/)

- In Geodatabases:

- - [Feature Class Basics](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//003n00000005000000.htm)
  - [Raster Basics](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Raster_basics/003n00000006000000/)

#### Projections & Coordinate Systems

- [Georeferencing and Coordinate Systems](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Georeferencing_and_coordinate_systems/00v20000000q000000/)
- [What are map projections?](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//003r00000001000000.htm)
- [Projection Basics for the GIS Professional](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Projection_basics_for_GIS_professionals/003r00000002000000/)
- [Identifying an unknown coordinate systems](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Identifying_an_unknown_coordinate_system/003r00000004000000/)

Thanks to Shannon Bardot for bringing to my attention this great YouTube video from the West Wing (see too here for the article on '[We Have Been Misled By An Erroneous Map of the World for 500 Years](http://www.upworthy.com/we-have-been-mislead-by-an-erroneous-map-of-the-world-for-500-years?c=reccon1)'. 

![True_Size_Of_Africa]({{ site.baseurl }}/assets/images/True_Size_Of_Africa.png)

#### Making Good Maps

Our [grading system]({{ site.baseurl }}/about/grades) in these classes is based entirely on your ability to make good maps.

![mapchecklist_2_lg]({{ site.baseurl }}/assets/images/mapchecklist_2_lg.jpg)

A very useful article in ESRI's ArcUser was recently published by Buckley & Field (2011) on how to '[Make a Meaningful Map](http://www.esri.com/news/arcuser/0911/making-a-map-meaningful.html)'. Buckley & Field (2011) suggest posing the following questions:

1. Do I know what my map's story is?
2. Am I using the right map projection?
3. Am I using data at the right level of generalization?
4. Is my symbology clear?
5. Do my symbols match my data?
6. Have I used the right text symbols?
7. Does my map have figure-ground organization?
8. Does my map have good visual hierarchy?
9. Do I need to add anything else to my map?
10. Have I asked for a critique?

* Buckley, A. and K. Field (2011). [Making a Meaningful Map: A Checklist for Compiling More Effective Maps](http://www.esri.com/news/arcuser/0911/files/mapchecklist.pdf). ArcUser. Redlands, CA, ESRI. 14: 40-43.

Subpages (2): [1. Podcasts]({{ site.baseurl }}/topics/digitalmaps/1-podcast) [More About File Types]({{ site.baseurl }}/topics/digitalmaps/more-about-file-types)

