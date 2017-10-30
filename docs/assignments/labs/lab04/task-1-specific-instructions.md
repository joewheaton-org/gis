---
title: Task 1 Details: Create Campground Presentation Map
---

## **Step 1:  Set up map project, locate lake**

Download and extract the Weber County roads file, SWReGAP landcover data, and alternative sites from the [Lab 4 data folder found here.](https://usu.instructure.com/files/63543224/download?download_frd=1) (Must be logged onto Canvas) 

The approximate location of the campground is **425,666 E 4,578,749 N in the NAD 83 UTM Zone 12N **coordinate system. 

See the demonstration video on the Lab 4 assignment page (Canvas) for a couple tricks for using the coordinates to find the campground location.

## **Step 2:  Create Two New Feature Classes: Point and Polygon**

Design a campground.  It should have at least 4 sites. Use points to mark the site locations, polyline to map trails or paths, and polygons to create parking, site pads, or whatever you want.  

You will need to create three new feature classes (shapefiles); 

1. a shapefile of type polyline into which you will digitize paths, trails, or roads (you might call this trails.shp),
2. a shapefile of type polygon into which you will digitize parking areas, or camping pads, etc.
3. a shapefile of type point that will represent each campsite.

- In the ArcCatalog window within ArcMap, navigate to the folder in which you want to put these new shapefiles > right click > *New > Shapefile*.  
- Designate the name (trails, campground or campsite), 
- the file type (polygon or point), and 
- Edit button to select the projection to NAD 83 UTM Zone 12N. 

The new shapefiles should be added automatically to your map's table of contents.  They will be randomly assigned symbology, which you can change, but remember - nothing will display because they are 'empty' files (think of them as blank pieces of paper).

<iframe width="560" height="315" src="https://www.youtube.com/embed/YC2ErR4o604" frameborder="0" allowfullscreen></iframe>

This tutorial walks through setting up your map and the steps for creating a new shapefile.  **Note: this video refers to a USFS boundary file. You should disregard this data set.  You do not need to work with the USFS boundary data or Weber roads, data.  **

## **Step 3:  Digitize campground, campsites, trails**

Add the shapefiles to your map if they aren’t there already.

Start with the polygon.  

Start editing.  

In the table of contents, right click on the polygon/campground layer > Edit Features > Start Editing

This will make the layer available for editing and will open the Editor toolbar.

<iframe width="560" height="315" src="https://www.youtube.com/embed/cepuQws6feY" frameborder="0" allowfullscreen></iframe>

This tutorial walks through digitizing and editing a polygon as well as adding a field and text to your attribute table.  It is meant to be a general guide, not specific instructions for the lab assignment.

Remember (or note): you must double click to finish features (lines, polygons) when done drawing to 'finish the sketch'.  You can also right click while you are drawing and choose "finish the sketch".  If you don't 'finish the sketch' the editor won't have anything to save when you quit editing and you will lose your edits.

Populate the campsite (point) attribute table with the following information (minimally; feel free to get creative and add more if you feel appropriate):

- Campsite Number (different than the FID)
- On which side of the lake the campground is located (north, south, etc.)
- Type of water recreation access (e.g. Lake, Stream, Lake & Stream, None). Since all campsites are within walking access to such resources, this attribute is intended to specify whether the campsite is directly adjacent the water.
- Whether it has a parking spot (road access).

Adding fields to your attribute tables can only be done outside an editing session.  Select "text" as the field type.  While in an editing session, you can populate any record field by clicking on it and typing directly into it. 

Include this table (a screenshot is fine) in the write up on your Lab 4 webpage.  See Lab 3 Task 2 for a refresher on adding tables.  Make sure the header are descriptive (no jargon or undecipherable abbreviations).  Export to Excel if editing is warranted.

This is a good time to mention the importance of metadata for newly created data.

See [ESRI's white paper](http://www.esri.com/library/whitepapers/pdfs/metadata-and-gis.pdf) on Metadata and GIS for more information on why this is important.  But to summarize, "Metadata not only helps find data, but once data has been found, it also tells how to interpret and use data." (ESRI, 2002)  See [ArcGIS Desktop's Help](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Editing_metadata/003t0000000n000000/) for details about how to access, edit, and populate metadata for your files.  (Not required for this lab, but you should know how to do this.)

## **Step 4:  Analyze landcover for campground and alternative sites **

Summarize the dominant landcover and overall variety of landcover for a 1 km area around your liberty campground.  Compare this to the landcover for 5 alternative sites (shapefile in the zipped data folder).

#### IMPORTANT:

**Help! I am getting an error saying I don't have the required license to run the Zonal Statistics tool!**

You will need to **activate the Spatial Analyst** extension to run some of the tools needed in this lab.

- In ArcMap > Customize drop down > Extensions > check all the boxes and close.

You will have to do this every time you log into the Quinney computers, and once per install on your personal computer.

\1. Buffer Liberty Campground to 1 km.

- Search for and open Buffer tool. 
- Input your campground boundary. 
- Set distance to 1 km.  
- Run

\2. Use "Zonal Statistics" to summarize landcover for your campground buffer "zone"

- Search for and open "Zonal Statistics as Table" tool.  
- Input Zone data (campground buffer).  
- Set unique zone field (FID only option...).  
- Set Value Raster to Landcover (the raster data to be summarized).  
- Name and place output.  
- Run All statistics types.
- Run.

​    Table is added to map. Open to view results.  

- **Minority** is the code for the landcover type that appears least often in the buffer region.  
- **Majority** is the landcover type appearing most often in the zone. 
- **Variety** field reports how many different landcover types appear in the zone. 

Prepare a table to report Most Common land cover type and How Many landcover types are within 1 km of *your  Liberty *campground.

Table should describe the **descriptive name** of the landcover type, *not the numeric key*. You may need to refer back to the original landcover dataset.

3.  Analyze landcover for the optional/alternative sites.

- Add the optional_sites point file to map (if you haven't already). 
- Buffer the points to 1 km.
- Run Zonal Statistics as Table on the alternative buffer zones.  (Make sure the Zone field is set to a field   containing **unique values**.)  
- Summarize results for most common vegetation type (report the descriptive name, not the numeric key) and landcover variety for your campground and the 5 optional sites.  

## **Step 5:  Create formal map of campground - post to website**

Create a map or series of professional figures presenting your proposed campground. 

Presentation should include:

- Map(s) of the campground area, the campsites, and trails 

- Spatial context (where is this relative to regional landmarks

- - Consider using the interactive Google map to provide locational context.

- Table with results of landcover analysis

[^ Back to Parent Lab 4](http://gis.joewheaton.org/assignments/labs/lab04)                                           [-> Next to Task 2](http://gis.joewheaton.org/assignments/labs/lab04/task-2-details-share-files-with-internal-review-committee)  

