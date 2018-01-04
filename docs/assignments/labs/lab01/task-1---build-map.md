---
title: Task 1 - Create Study Site Map
---

### Make New Map & Bring in Data and Context Layers

- If you have not already, make a [folder connection](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00sn00000007000000.htm) to your `...\WATS4930\Labs\Lab01` folder. 
- Download and unzip the contents of ![img](http://gis.joewheaton.org/_/rsrc/1294374366830/assignments/labs/lab01/task-1---build-map/zip_icon.gif)[StudySite Polygon](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab01/Lab01_StudySite.zip) (data credits: Joe Wheaton) to your `...\WATS4930\Labs\Lab01` folder (Note this step is not in ArcGIS).
- In ArcMap's Catalog Window, you should be able to browse to the Lab01 folder through your folder connections and see the downloaded shapefile (`StudySite.shp`) and layer file (`Study Site.lyr`). If it does not show up, you may need to hit F5 to refresh the contents. 

![CatalogWindow_wShapeFile]({{ site.baseurl }}/assets/images/CatalogWindow_wShapeFile.PNG)

In the catalog, right click on the `StudySite.shp` file and click on *Properties*. Take note of the coordinate system on the* XY Coordinate System* tab for the shapefile.

![Shapefile_CS]({{ site.baseurl }}/assets/images/Shapefile_CS.PNG)

Before adding this data, right-click on the **Layers **data frame in the *Table of Contents* and click on *Properties*. In the *Data Frame Properties* dialog, switch to the *Coordinate System* tab and notice that no projection is defined for the data frame (this is normal for a blank new map document). Click OK to close the dialog.

![DataFrame_CS_Before]({{ site.baseurl }}/assets/images/DataFrame_CS_Before.PNG)

(Your image may be different depending on the ArcMap version used.)

- Now add the `Study Site.lyr` file to the map (by either dragging it to the Table of Contents from the catalog, or using the *Add Data ![img](http://gis.joewheaton.org/_/rsrc/1294558850323/assignments/labs/lab01/task-1---build-map/AddDataButton.PNG) *command).  Note, if your layer shows the dreaded red exclamation source next to it (**!**) just right click on it >* Data ->  Repair Data Source* and point the layer to the source file: `StudySite.shp`.
- Again, right-click on the **Layers **data frame and notice that a projection is associated with this data frame. Is it the same as the shapefile?

![DataFrame_CS_After]({{ site.baseurl }}/assets/images/DataFrame_CS_After.PNG)

- It is very important to verify that the map document you are working in has the coordinate system you want loaded. By default, ArcMap assigns the coordinate system for the data frame based on the coordinate system of the first layer added to the data frame. If other layers are later added without coordinate systems, ArcMap assumes they are in the same coordinate system as the data frame. If other layers are added with different coordinate systems, ArcMap reprojects those layers on the fly and attempts to correctly overlay that layer with the others. This is convenient, but dangerous if you don't know what is happening behind the scenes and don't know what you are doing. We will cover this topic in more detail [next week](http://gis.joewheaton.org/topics/digitalmaps) and in [Lab 02](http://gis.joewheaton.org/assignments/labs/old-labs/Georeferencing). 

#### Add Some Context

- Add some context to the map. Right now you probably have no idea where these two polygons (representing your study site) are because there is no context. The easiest way to add context is to add a [Basemap Layer](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/Adding_layers_to_a_map/00s50000000v000000/).   (Drop down arrow on the Add Data button.)

![Add%20Basemap]({{ site.baseurl }}/assets/images/Add%20Basemap.PNG)

- Choose a Basemap layer and click *Add*. (Note, you can check when the imagery for your map was flown [here](http://mvexel.dev.openstreetmap.org/bing/#), and see [here for how to properly cite Imagery](http://www.arcgis.com/home/item.html?id=677cd0c509d842a98360c46186a2768e)).
- You should now see a lake, which you might recognize, in between the two polygons. You can use your mouse scroll wheel to zoom in and out or any of the zoom commands. If you notice that it seems a little slow when you zoom in and out at first, its because the basemap you just added is being loaded based on your internet connection to an ArcGIS Online server. Zoom out enough until you recognize where you are. Notice that as you zoom in and out, the resolution of the imagery loading changes (these are different [pyramid levels](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t00000019000000.htm)).

### Make your Map Layout

- This first map is where you show us what you've got (cartographically speaking).

- - Create clear map purpose, unifying the title with the symbology, scale, and extent of your map.

- Elements of a Good Map:

- ![GUID-C96216DF-CB9C-4467-831B-F7892A59E39B-web]({{ site.baseurl }}/assets/images/GUID-C96216DF-CB9C-4467-831B-F7892A59E39B-web.png)

- - Switch to the [layout view](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/A_quick_tour_of_page_layouts/00s900000007000000/). 

  - Using your [background knowledge of ArcGIS](http://gis.joewheaton.org/assignments/labs/lab01/getting-organized-and-oriented/arcgis-10-desktop-orientation), create a nice looking map that meets the [six C's criteria](http://gis.joewheaton.org/about/grades#TOC-The-Six-C-s-Rubric) and fits the [purpose defined for this lab](http://gis.joewheaton.org/assignments/labs/lab01#TOC-Background). For the context C, [minimally](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/How_maps_convey_geographic_information/00v20000000s000000/), your map should include:

  - - Effective symbology
    - North arrow 
    - Title
    - Scale bar and/or [grid or graticule](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#/What_are_grids_and_graticules/00s900000010000000/)
    - Second data frame showing location or inset details
    - [Legend](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00s900000023000000.htm) and/or Labels
    - Data source(s) and any other *pertinent* details
    - Who produced the map
    - Date of map production

  - You may wish to use different basemaps (whatever you find the most effective)

  - Alter the polygon symbology.  Remember blue tends to read as water - so you might want to change that polygon's color. Play with polygon transparency, fill color, and outline color.

  - **Add a locator map: **a second data frame with a basemap and use of [extent indicators](http://pro.arcgis.com/en/pro-app/help/layouts/extent-indicators.htm)?...

  - Export your finished map to a PDF (see [here](http://gis.joewheaton.org/assignments/labs/lab01/getting-organized-and-oriented/arcgis-10-desktop-orientation/working-with-arcmap#TOC-Exporting-a-Map-as-an-Image) if you need help), AND  jpeg format. 

- ### Convert your Study Site Layer as a KMZ file

- - In ArcMap, save your new polygon symbology as a Layer File (table of contents, right click Study Site layer > Save As Layer File)
  - Bring up the [search window](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00660000007q000000.htm) in ArcGIS. Do a search for KML (keyhole markup language; i.e. a google earth file) in the search window.



![KMZ_Search]({{ site.baseurl }}/assets/images/KMZ_Search.PNG)

- Use the [*Layer to KML*](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00120000004n000000.htm) tool from the search results to export your `Study Site` layer to a KML in  your `...\WATS4930\Labs\Lab01` folder.

![LayerToKML]({{ site.baseurl }}/assets/images/LayerToKML.PNG)

- Open the KMZ file in Google Earth and make sure it looks like it is in the correct location.
- KMZ and KML are both keyhole markup files. The Z is for 'zipped'.

This concludes the instructions for Task 1. You've created a map of your study site that meets the [six C's criteria](http://gis.joewheaton.org/about/grades#TOC-The-Six-C-s-Rubric)and demonstrates your mad GIS visualization skills. You've exported your map into both a PDF and a JPG image format. You've converted the study site polygons from ArcGIS to a KMZ format that can be viewed in Google Earth.

------

[Next Task](http://gis.joewheaton.org/assignments/labs/lab01/task-2---build-website) (Task 2)

