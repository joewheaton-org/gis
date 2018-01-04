---
title: Week 04 - Geoprocessing & Uncertainty
---

#### Important Dates & Links

**Lecture Date(s):**

*See Calendar*

------

**Reading Assignments**

[See Here for Reading Assignments]({{ site.baseurl }}/assignments/reading-assignments-2010)

------

Lab Assignment(s)

- [Lab 04 - Digitzing, Editing & Sharing Data]({{ site.baseurl }}/assignments/labs/lab04)

### Background

#### Introduction to Geoprocessing

From ESRI's Help:

"Geoprocessing is for everyone that uses ArcGIS. Whether you're a beginning user or a pro, geoprocessing will become an essential part of your day-to-day work with ArcGIS.

The fundamental purposes of geoprocessing are to allow you to automate your GIS tasks and perform spatial analysis and modeling. Almost all uses of GIS involve the repetition of work, and this creates the need for methods to automate, document, and share multiple-step procedures known as workflows. Geoprocessing supports the automation of workflows by providing a rich set of tools and a mechanism to combine a series of tools in a sequence of operations using models and scripts...." - ...[READ MORE](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_geoprocessing/002s00000001000000/).

#### The power of layers in GIS:
![GUID-5BD98316-8BF4-430C-BA24-F47EFF8BF66D-web]({{ site.baseurl }}/assets/images/GUID-5BD98316-8BF4-430C-BA24-F47EFF8BF66D-web.png)

#### Why we're Covering it

Geoprocessing is what helps make you efficient in your spatial analyses. Whether its combining multiple tools into one using model builder, batch processing a large quantity of data, writing some simple Python scripts, or leveraging the functionality of the Results window, geoprocessing is what can help you move from a novice GIS user, to a highly proficient power user.

#### Learning Outcomes

These lectures, readings and Labs [03]({{ site.baseurl }}/assignments/labs/lab03) & [04]({{ site.baseurl }}/assignments/labs/lab04) all help fulfill [primary learning outcomes]({{ site.baseurl }}/about/primary-learning-outcomes) 1, 2, 3 & 4.

### Lectures and Podcasts

#### Geoprocessing, Model Building & Scripting

So many of the geoprocessing tasks we do in ArcGIS are highly mundane and repetitive. Building models and/or writing scripts in ArcGIS is an effective way of increasing your efficiency.

View

[Podcast Here]({{ site.baseurl }}/topics/week-04---geoprocessing-uncertainty/geoprocessing-podcast) or [stream whole podcast series here](https://www.youtube.com/playlist?list=PL0ZiZg4rilzJ8p6ap_EQ7A7r7_xUD8E6D)

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2015]({{ site.baseurl }}/topics/goog_670769724)[ Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2015/Lectures/4_Geoprocessing.pdf)  - PDF

Previous:

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/topics/goog_930015760)[ Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week03/2_Geoprocessing_AND_Uncertainty.pdf)  - PDF
- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2013](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/topics/goog_930015760)[ Thursday Lecture](http://etal.usu.edu/Courses/GIS/2013/Lectures/Week_03/2_Geoprocessing.pdf)  - PDF
- ![img]({{ site.baseurl }}/_/rsrc/1325824218298/past-year-s-course-topics/geoprocessing/pdf_icon.gif) 2012 [Thursday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/2_Geoprocessing_2PP.pdf) - 2 Slides per page
- ![img]({{ site.baseurl }}/_/rsrc/1325824218298/past-year-s-course-topics/geoprocessing/pdf_icon.gif) 2012 [Thursday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/2_Geoprocessing_6PP.pdf) - 6 Slides per page
- 2012 [Video of Lecture](http://youtu.be/rG0Zq-S7k50)

[![podcast]({{ site.baseurl }}/assets/images/podcast.jpg)]({{ site.baseurl }}/topics/week-04---geoprocessing-uncertainty/geoprocessing-podcast)

#### NOT the Podcast.... Old Lecture From 2012

<iframe width="560" height="315" src="https://www.youtube.com/embed/rG0Zq-S7k50" frameborder="0" allowfullscreen></iframe>

#### Uncertainty in GIS & Synthesis of GIS Fundamentals

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2016 Thursday Lecture](http://etalweb.joewheaton.org/Courses/GIS/2017/Lectures/5_Uncertainty.pdf) - PDF

This year, the Uncertainty in GIS was combined with the Geoprocessing Lecture

- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif)  [2015 Thursday Lecture](http://etal.usu.edu/Courses/GIS/2015/Lectures/5_Uncertainty.pdf) - PDF
- ![img](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/_/rsrc/1294035212312/topics/introgis/pdf_icon.gif) [2014](https://sites.google.com/a/joewheaton.org/gis-wats-4930-6920/topics/goog_930015760)[ Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2014/Lectures/Week03/2_Geoprocessing_AND_Uncertainty.pdf)  - PDF
-  2012 [Tuesday Lecture](http://etal.usu.edu/Courses/GIS/2012/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/4_UncertaintyInGIS_2pp.pdf) - PDF w/ 2 slides per page
-  2012 [Tuesday Lecture](http://www.gis.usu.edu/~jwheaton/courses/WATS4930/Lectures/Week%2003%20&%2004%20-%20Working%20with%20Data/4_UncertaintyInGIS_6pp.pdf) - PDF w/ 6 slides per page
- 2012 [Video of Lecture](http://youtu.be/QZ9zifqTBBQ)

#### NOT the Podcast.... Old Lecture From 2012

<iframe width="560" height="315" src="https://www.youtube.com/embed/QZ9zifqTBBQ" frameborder="0" allowfullscreen></iframe>

### Additional Resources

#### Geoprocessing in ArcGIS

- [Geoprocessing ArcGIS Resource Center](http://resources.arcgis.com/content/geoprocessing/10.0/about) - *This is the main hub of information on Geoprocessing and getting yourself up to speed.*
- [The Geoprocessing Forum](http://forums.arcgis.com/forums/31-Geoprocessing) - *Trying to do something with Geoprocessing and having trouble? Try posting a thread or searching this forum.*
- [Geoprocessing Help](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_is_geoprocessing/002s00000001000000/) - *An overview of Geoprocessing in ArcGIS*
- [Using the Results Window](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Using_the_Results_window/002100000013000000/)* - An essential new feature of Geoprocessing in ArcGIS*

#### Batch Processing

- [A quick Tour of Batch-Processing](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/A_quick_tour_of_batch_processing/00210000000w000000/) - *ArcGIS 10 Help topic*

#### Finding Existing Tools and Scripts

- [Geoprocessing Model and Script Tool Gallery](http://resources.arcgis.com/gallery/file/geoprocessing) - *A hub of tools you can download and install in ArcGIS that other users have made. Very useful!*
- See also this week's lab [Tutorial Topic 1]({{ site.baseurl }}/assignments/labs/old-labs/lab_homeless/1-basics-of-loading-and-using-a-toolbox-and-model)

#### Geoprocessing with Model Builder

- [Designing and Building Geoprocessing Tools](http://resources.arcgis.com/gallery/video/geoprocessing/details?entryID=B44B5D9E-1422-2418-7F09-D0B3A5E3C65F) - *This video walks you through the basics of building Geoprocessing Tools using Model Builder in ArcGIS 10.*
- [A quick tour of creating tools with ModelBuilder](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/A_quick_tour_of_creating_tools_with_ModelBuilder/00150000001t000000/)  - *ArcGIS 10 Help*
- [Tutorial for Building Tools with Model Builder](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Tutorial_Creating_tools_with_ModelBuilder/00150000001v000000/)* - ArcGIS 10 Help Tutorial*

#### Add-Ins

- [Add-Ins for ArcGIS 10](http://resources.arcgis.com/gallery/video/java/details?entryID=F8A0A38E-1422-2418-7FA3-CC2C83ED9674) -* Add-Ins are a new feature in ArcGIS. This video describes them.*
- [Add-Ins Blog](http://resources.arcgis.com/gallery/video/java/details?entryID=F8A0A38E-1422-2418-7FA3-CC2C83ED9674) -

#### Plug-Ins

Plug-Ins are typically tool-bars that are installed externally and produced by someone other than ESRI, to work within ArcGIS.

#### Python Programming

- [Scripting with Python in ArcGIS](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/A_quick_tour_of_creating_script_tools/001500000006000000/) - *ArcGIS 10 Help Topics*
- [Getting Started with Python in ArcGIS](http://resources.arcgis.com/gallery/video/geoprocessing/details?entryID=B4475D87-1422-2418-7F8B-E203050C5254) -* This ESRI video takes you from the basics of Python and running geoprocessing tools and functionality to creating your own tools using Python.*


- [Python Scripting for Map Automation in ArcGIS 10](http://resources.arcgis.com/gallery/video/geoprocessing/details?entryID=B449043B-1422-2418-7F7A-E7EA74EF068E) - *Do you have to make a lot of the same maps with just slightly different layers? This video goes through how you can use Python to automate that process.*
- [Using Python in ArcGIS 10](http://training.esri.com/acb2000/showdetl.cfm?DID=6&Product_ID=971) - *A free 3 hour Web-Based course offered from ESRI*

#### Some Good References on Uncertainty in GIS

- Bolstad P. 2005. [GIS fundamentals: A first text on geographic information systems](http://www.paulbolstad.net/gisbook.html). Eider Press, 620 pp. - *See Chapter 14 on Data Standards and Data Quality*
- Burrough PA and McDonnell RA. 1998. [Principles of Geographical Information Systems: Spatial Information Systems and Geostatistics](http://www.amazon.com/Principles-Geographical-Information-Systems-Spatial/dp/0198233655). Oxford University Press: Oxford, 333 pp. - *See Chapters Nine (Errors and Quality Control) and Ten (Error Propagation in Numerical Modeling)*
- Burrough P.A., van Rijn, R., and Rikken, M. 1996. [Spatial Data Quality and Error Analysis Issues: GIS Functions and Environmental Modleing](http://books.google.com/books?id=amzYLaY4ddcC&pg=PA29&lpg=PA29&dq=error+analysis+in+GIS&source=bl&ots=Ry4rI6vSzG&sig=IJ0wv-Kl6QNMOtGnhFQhPCnU074&hl=en&ei=e02aTYnrOIvPiAK546zgCA&sa=X&oi=book_result&ct=result&resnum=9&ved=0CFQQ6AEwCA#v=onepage&q=error%20analysis%20in%20GIS&f=false). In: GIS and Environmental Modeling, By Michael F. Goodchild, Louis T. Steyaert, Bradley O. Parks, Carol Johnston (Eds.), Wiley.
- Haining R. 2003. Spatial Data Analysis: Theory and Practice. Cambridge University Press: Cambridge, 432 pp. - *See Chapter 4 on 'Data quality: implications for spatial data analysis'*
- Hall ST and Post CJ. 2009. [Advanced GIS Exercise: Performing Error Analysis in ArcGIS ModelBuilder](http://www.jnrlse.org/view/2009/e08-0025g.pdf). Journal of Natural Resources and Life Sciences Education. 38: 41-44.
- Taylor J. 1997. [An Introduction to Error Analysis: the Study of Uncertainties in Physical Measurements](http://books.google.com/books?id=giFQcZub80oC&printsec=frontcover&dq=An+Introduction+to+Error+Analysis:+the+Study+of+Uncertainties+in+Physical+Measurements&hl=en&ei=6EyaTYGHE4LiiAKMmbGdCQ&sa=X&oi=book_result&ct=result&resnum=1&ved=0CC0Q6AEwAA#v=onepage&q&f=false), Second Edition. University Science Books: Sausalito, California, 327 pp.

#### Web Links on Uncertainty:

- [Error, Accuracy and Precision in GIS](http://www.colorado.edu/geography/gcraft/notes/error/error_f.html) -* A very helpful series of webpages on the basics of errors, accuracy and precision in GIS maintained by **Kenneth E. Foote and Donald J. Huebner, The Geographer's Craft Project, Department of Geography, University of Texas at Austin. *
- [Uncertainty Propagation in GIS](http://www.ncgia.ucsb.edu/giscc/units/u098/u098_f.html) - *Curriculum developed by : Gerard B.M. Heuvelink, Faculty of Environmental Sciences, University of Amsterdam.*
