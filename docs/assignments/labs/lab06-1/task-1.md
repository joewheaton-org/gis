---
title: Task 1
---

### NOTE: you may need to activate the Spatial Analyst extension to access some of the tools needed for this lab. 

In ArcMap go to the Customize drop down > Extensions.  Click in the Spatial Analyst box to toggle on the check mark > Close. (You can go ahead and turn on any other extensions you want at the same time.)

## Task 1 - Overview

Task 1 is really all about getting four different resolution DEMs for our study watershed (Big Cottonwood Canyon) into ArcGIS and then displaying them in a useful format. This sounds like a straight-forward task, but in reality it is a somewhat nuanced exercise and takes a while to get everything in exactly the format you want for the areas you want. This is typical of working with raster data provided from others ([Utah AGRC](http://gis.utah.gov/data/#) in this case). 

These instructions DO NOT walk through every step of that process for you. However they do cover most of the tricky parts once (i.e. for one of the four resolution DEMs) and then we expect you to be able to apply that knowledge by doing the same thing for the other datasets. We start our instructions focusing on finding where our study site is, and then we start with the high resolution data first (2m LiDaR DEM) and move on to the easier coarser resolution datasets. As with all the instructions in these [labs]({{ site.baseurl }}/assignments/labs), this is not the only way to do things, but it is suggested. 

### Figure out Where the Big Cottonwood Canyon Watershed Is

 Download* and unzip the `Watersheds_Area_shp or _gdb file` from the [Utah AGRC](http://gis.utah.gov/data/water-data-services/watersheds/) for the state of Utah. After [lab 4]({{ site.baseurl }}/assignments/labs/lab04) you should appreciate the differences between the two formats. 

1. Load the `Watersheds_Area` polygon feature class for Utah into an empty map document.
2. Add an imagery basemap for context.
3. Explore the attribute table of `Watersheds_Area` to see what the attribute fields are. For tasks 1 and 2, you will be acquiring DEMs and comparing them for the Big Cottonwood Canyon Watershed (i.e. where [Solitude](http://www.skisolitude.com/) and [Brighton](http://www.brightonresort.com/) Ski Resorts are). The HUC 12 name is 'Headwaters Big Cottonwood Canyon.' 
4. I would suggest exporting just the Big Cottonwood Canyon Watershed to its own shapefile or feature class.

------

## Get Data

### Get the 2m LiDaR DEMs

For 2 m LiDaR DEM... you will need to know what tiles to download. You can do this in a variety of ways. I downloaded the **LiDAR2006_2m_BareEarth_Tiles** from the [2m LiDaR page](http://gis.utah.gov/data/elevation-terrain-data/2-meter-lidar/), and performed a [*Select by Location*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00s50000002q000000.htm) to find the tiles in the **LiDAR2006_2m_BareEarth_Tiles** attribute table that were within the Big Cottonwood Canyon Watershed:

[![2011-02-13_112019]({{ sites.baseurl }}/assets/images/2011-02-13_112019.png)]({{ sites.baseurl }}/assets/images/hr/2011-02-13_112019.png)

Now we have a problem. When we look at the **LiDAR2006_2m_BareEarth_Tiles** attribute table, we see the query has correctly returned 51 records (note you can view just the selected in the attribute table with the *Show Selected Records* button ![ShowJustSelcted]({{ sites.baseurl }}/assets/images/ShowJustSelcted.png): 

[![2011-02-13_112907]({{ sites.baseurl }}/assets/images/2011-02-13_112907.png)]({{ sites.baseurl }}/assets/images/hr/2011-02-13_112907.png)

The problem is that it would take a VERY long time to download all 51 tiles individually, then load them up, perhaps combine them into one very large raster layer (e.g. using the 

*mosaic*

 command). If at the end of lab you're feeling particularly ambitious and have extra time, feel free to undertake such a brute force exercise for extra credit. However, for the rest of us, this is a perfect example of where we may want to make an executive decision to limit our download and processing time up front, and instead, create an detailed visual comparison using a subset of the LiDAR data, and make a compelling case to the client detailing the pros and cons of using high resolution lidar data.  

#### A Compromise

Lets download just the two tiles that cover most of the Solitude Ski Resort. We will use these two tiles to illustrate to our boss and the Cottonwood Canyon Foundation the nature and resolution of the 2m LiDaR DEMs in Task 1, and do the requested comparison in Task 2. 

To figure out these tiles, I zoomed into the area around Solitude (easy to spot from aerial imagery basemap layer if you've been there, but also easy to confuse with Brighton).  The video shows you how to choose the tiles.

<iframe width="560" height="315" src="https://www.youtube.com/embed/vrFW9LO7ov0" frameborder="0" allowfullscreen></iframe>

The LiDaR tiles we want from [Utah AGRC](http://gis.utah.gov/data/elevation-terrain-data/2-meter-lidar/) are `12TVK480940 `and `12TVK480960`. There are several options for downloading these tiles ranging from an FTP listing to various interactive maps. Each has its own advantages and disadvantages. I chose to download these from the **2 meter Bare Earth LiDAR Interactive Map** because I knew where to navigate to within the map (note because the raster is an ASCII text file, if you left click on it it may just open the text file in your browser; try right clicking instead and *Save Target As.* If your browser doesn't allow this, try switching to Internet Explorer).  

[![2M_Download]({{ sites.baseurl }}/assets/images/2M_Download.png)]({{ sites.baseurl }}/assets/images/hr/2M_Download.png)

One of the annoying things about how Utah AGRC is providing these LiDaR tiles is that they are in an [Arc ASCII grid format](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000z000000.htm). The format is convenient for being able to read the file in a text editor and/or other programs, but is not at all convenient for straight import into ArcGIS. The Arc ASCII grid also has no projection associated with it. You will notice that on the [Utah AGRC download page](http://gis.utah.gov/data/elevation-terrain-data/2-meter-lidar/) they have provided instructions for [Using ASCII Files in ArcMap](http://gis.utah.gov/wp-content/uploads/ASCII_Elevation_Data.doc). They tell you the projection and datum you should use and how to add these files to their own geodatabase. I suggest you follow [those instructions](http://gis.utah.gov/wp-content/uploads/ASCII_Elevation_Data.doc) (excerpt below):

'The File-based Geodatabase is great for working with elevation data. In ArcCatalog right mouse click in the location you want to create your database and select *New->File Geodatabase*. Next right mouse click the database and select *New->Raster Dataset*. The Pixel Type should be set to 32_BIT_FLOAT and the Spatial Reference set to NAD83 UTM Zone12 North for the XY Coordinate System and a North America NAVD1988.prj for the Z Coordinate System. With your new Raster Dataset, Right mouse click and select *Load->Load Data*. Select the `.asc` files you want to load and set the other parameters for the load (you can leave defaults). Once you have successfully loaded your data you will want to "Compact" the database (data management tool) then Generate Statistics on the newly populated Raster Dataset (right click on dataset in ArcCatalog).'

[![CreateRasterDataset]({{ sites.baseurl }}/assets/images/CreateRasterDataset.png)]({{ sites.baseurl }}/assets/images/hr/CreateRasterDataset.png)

There are multiple places in the simple step of converting and loading the ASCII raster DEMs into a more useful form in ArcGIS that folks get confused and get derailed. As ASCII raster data is such a common form in which DEMs and other raster datasets are made available, these are essential skills to develop and understand each step. The video tutorial provides you with a little extra explanation and step-by-step explanation of the steps described in the [Using ASCII Files in ArcMap](http://gis.utah.gov/wp-content/uploads/ASCII_Elevation_Data.doc) instructions from the Utah AGRC.

<iframe width="560" height="315" src="https://www.youtube.com/embed/n7krR-dqpvQ" frameborder="0" allowfullscreen></iframe>

Note, you will find these rasters display quicker if you [*Build Pyramids*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t00000019000000.htm) for them (right click on the raster dataset to access this command).

**Note**: If this process doesn't work, Run the ASCII to Raster tool (Conversion) - saving the ascii files as *.TIF files, then the Mosaic to New Raster tool which will combine the two new TIF rasters.  Make sure you set the XY and Z coordinate systems for the New Raster in this second step. Don't include a file extension.  Pixel type and Bands should match the input rasters (check the properties).  

### Get the 5 m Auto-Correlated DEM

For 5 m DEM, you can undertake a similar process to decide what tiles to download. You can do this in a variety of ways. In analogy to above, you can download the tile index **Auto_Correlated_DEM_5m** from the 5 Meter Auto-Correlated Elevation Model (DEM)	page on the Utah AGRC. Using a similar [select by location](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00s50000002q000000.htm) to find the tiles in the **Auto_Correlated_DEM_5m** attribute table that were within the Big Cottonwood Canyon Watershed. You should find that there are four tiles you will need (this is better then 50+ tiles, get them all):

[![Where%20to%20Select]({{ sites.baseurl }}/assets/images/Where%20to%20Select.png)]({{ sites.baseurl }}/assets/images/hr/Where%20to%20Select.png)

If you use the [interactive download map](http://stage.mapserv.utah.gov/raster/?cat=5%20Meter%20%7BDEM%7D), the tiles that intersect the Big Cottonwood Canyon Watershed are those highlighted in orange above.

You will notice that like the LiDaR rasters you download, these are also Arc ASCII Raster (`*.asc`) files. You will need to go through a similar process as with the LiDaR rasters above to covert these into a useful format (don't forget about projection... check the metadata [they provide](http://gis.utah.gov/data/elevation-terrain-data/5-meter-auto-correlated-elevation-models/)). **Warning**: each of these four rasters is 125 MB in size and the Mosaic step may take a fair bit of time (i.e. 5-15 minutes depending on your computer's speed).

### Get the 10m & 30 m NED DEMs

Whereas downloading the 2m and 5m DEMs was somewhat tricky and cumbersome, downloading the 10 m and 30 m resolution DEMs is fairly straightforward (especially through Utah AGRC). These DEMs are part of the 

National Elevation Dataset

 from the US Geological survey and are derived from the contour data used to make the 7.5" USGS Topographic Maps we worked with in Lab 3 and an earlier quiz. We will download these datasets from Utah AGRC because they have organized this by county (fortunately our entire watershed falls within Salt Lake County) and because they provide these in Arc Raster Grid formats that include pyramids, projections, and metadata. Use:

- <http://gis.utah.gov/data/elevation-terrain-data/10-30-meter-elevation-models-usgs-ned/> for both the10 m and 30 m resolution DEMs

## Displaying DEMs in a Useful Format

Although DEMs are very useful, by themselves, raster DEMs don't display the topography by default in a way that makes the terrain jump out at you. It turns out that the context we like from DEMs is best provided by a product derived from DEMs - a hillshade. Moreover, to compare different DEMs effectively, we want to use the same display properties (i.e. color ramp and elevation classification).  

For task 1, you've been asked to make figures comparing each of these four DEMs at the full watershed scale. In order to make these graphically pleasing and to use consistent symbology between the DEMs, we need to learn how to use Hillshades and manipulate the symbology and display properties, applying the same color ramps to the different rasters. This video covers those basics with a comparison between two of the four data sets:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ud-gtM6Ka0M" frameborder="0" allowfullscreen></iframe>

If you find that you are having trouble getting the 2m LiDaR to have a comparable color ramp to the three other DEMs, you may find this video tutorial helpful:

<iframe width="560" height="315" src="https://www.youtube.com/embed/M0SwZCKXAuA" frameborder="0" allowfullscreen></iframe>

#### Clipping Views vs. Raster Data

Finally, your Boss's instructions do not provide specific guidance as to how  to display your DEMs. He did say he wants them just for the watershed, but you may decide that you want to show the DEM for the watershed as well as part of the DEM outside your watershed (for context). This is exactly what the Salt Lake City Public Utilities Department did in the map below:

![CanyonsContext3]({{ sites.baseurl }}/assets/images/CanyonsContext3.png)

There is no single correct way to make your maps for Task 1 and we will leave that up to your creativity and professional judgment. You may find that either implementing a [display clip](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00s90000000q000000.htm) (of a data frame) or a [physical clip](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00170000009n000000.htm) of the raster dataset to the watershed boundary are extremely useful tools to have at your disposal. This video tutorial goes through an example of each with the 30 m DEM. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/8FEaDx-r91U" frameborder="0" allowfullscreen></iframe>

#### Using ArcScene to Create a 3D View

So that the Cottonwood Canyons Foundation has some eye candy, you can use [ArcScene](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00q8000000p0000000.htm) to create a 3D view of the Canyon. You can choose any of the DEMs to do this from. This video can help you through the basics: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/Rh5n1esNwps" frameborder="0" allowfullscreen></iframe>

### What to Submit

See the [what to submit]({{ site.baseurl }}/assignments/labs/lab06-1#TOC-What-to-Submit) section for Task 1.

[Proceed to Task 2]({{ site.baseurl }}/assignments/labs/lab06-1/task-2)



