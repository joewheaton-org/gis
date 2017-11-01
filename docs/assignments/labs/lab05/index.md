---
title: Lab 05 - Vector Analyses
---

### Introduction to Lab

#### Background

In an unprecedented series of events the dual 10-inch diameter Chevron oil pipelines transporting crude oil into the Salt Lake Valley for refinement has burst in Emigration Canyon. Emergency responders have identified the rupture location at (433321.82m, 4512098.776m). The pipeline break was not realized for 12 hours, allowing the 30,000 barrels of crude to flow downstream 7.5 kilometers to the above ground terminating point of Emigration Creek. 

#### Emigration Canyon, Salt Lake City, UT

<iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d112461.25615695489!2d-111.818295!3d40.751577!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDDCsDQ1JzA2LjAiTiAxMTHCsDQ4JzM0LjUiVw!5e1!3m2!1sen!2sus!4v1509544689807" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>

#### Data for Lab

In this lab you will retrieve data from the [Utah Automated Geographic Reference Center](http://gis.utah.gov/data/) (AGRC).  The AGRC is a warehouse for spatial data for the state of Utah.  They provide a wide variety of vector data as well as orthophotographs and terrain datasets. 

For this lab you will need to download the following data from the UT AGRC (link above):

Cadastre data:

- **Parcels_SaltLake_shp.zip** or **Parcels_SaltLake_gdb.zip**

Water data (Streams):

- **StreamsNHDHighRes_shp.zip** (or the geodatabase version)

The rest of the data for Lab 05 can be found in [**this zipped folder**](http://etal.usu.edu/Courses/GIS/2013/Lab/Lab05_data.zip) (click to download).

- SGID93.ENERGY.OilGasPipelines_UGS (data source: AGRC SGID)
- Map book grid shapefile (data source: Chris McGinty)
- EMS_CONTACT.xlsx (data source: Chris McGinty)

There are times when you might want to make a quick map, or browse AGRC vector data without downloading and unzipping files. You can connect your ArcGIS suite directly to the AGRC SDE vector geodatabase. This connection allows you to access and visualize all of the AGRC vector data in ArcMap or ArcCatalog without downloading each shapefile or geodatabase via the web browser.  However, accessing data via the AGRC server is not recommended if you plan on editing data, if you plan on saving your project and archiving the data, or if you are using/accessing large quantities of data and require fast processing speeds. 

Instructions for accessing AGRC ArcSDE database server are posted [here](http://gis.utah.gov/data/connecting-sgid-arcsde-server/) from the AGRC.

#### Prerequisites

Labs [03](http://gis.joewheaton.org/assignments/labs/lab03) & [04](http://gis.joewheaton.org/assignments/labs/lab04) 

### Lab Objectives

The overall lab objective is to build your confidence and proficiency with some of the basic vector analyses tools in ArcGIS. Specifically, you will learn how to:

- [Create a feature class](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00170000002p000000.htm) from a X,Y location
- Manipulate vector data through [*buffers*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//000800000019000000.htm), [*select by location*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//0017000000tr000000.htm), and [*select by attributes*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00s500000021000000.htm)
- Utilize *JOIN *to merge critical tabular data that will supplement spatial data
- Provide a ground-useable report for EMS and hazmat crews
- Understand page scale and [map books](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00s90000002s000000.htm)

Meets [Course Learning Outcome](http://gis.joewheaton.org/about/primary-learning-outcomes) 2. 

## Lab Tasks

You have been tasked to immediately address the following issues:

County officials have received numerous reports of residents being overcome and sickened by fumes, but there are still a number of residents that are not aware of the incident. The city and county officials are requesting a series of detailed maps and accompanying ownership information for the affected area.

#### Task 1

- Map the pipeline rupture, identify the stream reach affected, derive a 250-meter contamination buffer, and identify the parcels potentially impacted. 


- Develop an easy to read map book consisting of four maps (8.5 x 11 with page scale of 1:7500, in landscape format) and one reference page for EMS and hazmat teams to use in the field.  Make the map book downloadable as a `PDF `online (from your website).


- Display the critical data on a Google Map (online) for residents to view. Display the pipeline break, stream reach, and impacted parcels.

#### Task 2

Join the 

```
EMS_CONTACT.XLSX
```

 file to the new parcel feature class. Build an easy to read PDF document that identifies contact name, parcel ID, address, and phone number. Provide a “notes” field that workers may use to take field notes. Post the document online as a PDF for download.

## Detailed Instructions

#### Task 1

You should begin by identifying the spatial location of the pipeline rupture and create a spatial dataset containing this information. First responders have sent back the GPS coordinates of the rupture location at [(433321.]()82m, 4512098.776m). Note that the coordinates were collected in NAD83 UTM Zone 12N. 

You can use the short cut "Go To XY" tool on the main menu in ArcGIS to find the rupture location.  Or if you want to create a shapefile (point feature class) of the rupture location follow the instructions below. 

Adding XY data:

1. Create a simple table with the northing and easting values

​    Save and close Excel.

2. Add the table to Arc just like with any dataset.

3.  In the table of contents, right click the table > Display XY Data

4.  Verify that the point is in the right place (add a basemap, compare with other data layers).
5.  Change the temporary "Event" layer created to a permanent shapefile.

-    Right click the "Event" layer in the table of contents > Data > Export Data.



Once you have identified the rupture location, you need to identify and select the impacted portion of Emigration Creek. The NHD high resolution data from the Utah AGRC should provide you with the necessary information to complete this task. Note that due to the winter season, the irrigation spur located at (431099.378m, 4511359.276m) was not impacted and you should disregard this stream data.

You may wish to "cut" the stream segment where the rupture occurred in order to capture the true length of impacted stream.  Select the segment, start editing, use the "Split Tool" on the editor tool bar to cut the line segment at the rupture location.  (Click on the highlighted line at the rupture point.)  Then test the cut by trying to select.

When you have identified and selected the stream features, you should save only those features to a new dataset (again, Data > Export Data) and then buffer that reach of the stream to 250-meters. The 250-meter zone is considered the critical fume impact area.  (When you run the Buffer tool, consider setting the Dissolve to "All" to avoid the Michelin man looking buffers around each reach segment.)

Use the buffer results to select the impacted parcels (using the Select by Location tool) (Main menu > Selection drop down > Select by Location).  

Responders are not interested in any parcels that have a “federal” OWN_TYPE attribute.  Remember when using the Select by Location tool, that the 'Spatial selection method' will greatly impact your selection results.  Experiment with this feature to get the results you feel are appropriate for this analysis.

When you have your parcels selected, you will create an EMS and hazmat team field map book. Make sure that your map book has four map pages (with page scale of roughly 1:7500, in landscape format) and a reference or index page for EMS and hazmat teams to use in the field.  Use the Map book grid shapefile as a guide for the 4 map page extents. 

The maps should show only those parcels potentially impacted within 250-meters of Emigration Creek.  Be sure to include appropriate labels, legend, and basemap. The map should NOT include parcels designated as “federal” in the attribute table. See the What to Submit section for details.

#### Task 2

To complete the work, you need to open and join the EMS_CONTACT.XLSX file that you downloaded to the impacted parcel feature class. This join will allow you to export the table to Excel so that you can create a readable PDF that lists the contact name, parcel ID, address, and phone number of the impacted parcels.

You will  post this PDF online with your map books.

For tutorials walking through Tasks 1 and 2, click [here](http://gis.joewheaton.org/assignments/labs/lab05/lab-5-detailed-instructions).

------

### What to Submit

Prepare a webpage for this lab on your personal website for the course and prepare the following:

#### Task 1:

-  On your webpage, provide a fully legible** image of the reference page and an image of the first map pag**e (furthest upstream reach). (If image can't be enlarged to see relevant details, provide link to high resolution PDF.)


- - The reference (index) page should identify the pages of your map book and include:


- - - the total area of the impact buffer,
    - the length of the impacted portion of Emigration Creek, 
    - your information (as the analyst), 
    - data source information, 
    - the date. 
    - The Select by Location method you chose for isolating the parcels in the contamination zone.

  - The upstream page should demonstrate that you "Split" the stream line at the rupture location.


- Also provide a **link to the four map page**s created with the Data Driven Pages tool. 


- - - Ensure the maps are highly readable and provide the appropriate map components for full credit. 
    - Use the Map book grid shapefile as a reference for each map page's extent.
    - Convince us that you used the Data Driven Pages tool by demonstrating the same layout on each page.


- - - Provide a link to download the 4 page map book


- Build a **Google Map displaying the buffer** for residents to view (as they do not have GIS) that displays the buffer layer. 

#### Task 2:

- Provide a legible image of the **first page of your joined PDF**.  Edit headers.  

- - table should clearly show both the name and address with parcel ID to demonstrate join 

 

Make sure your lab conforms to the general [lab submission guidelines](http://a/joewheaton.org/gis-wats-4930-6920/labs#TOC-Lab-Submission-Guidelines). Submit a URL for this lab's webpage

### Additional Resources

#### 

#### Links

- [Geodatabase Connections in ArcGIS](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00290000003q000000) - More information on geodatabase connections using ArcSDE



Subpages (1): [Lab 5 Detailed Instructions](http://gis.joewheaton.org/assignments/labs/lab05/lab-5-detailed-instructions)



