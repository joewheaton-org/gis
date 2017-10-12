---
title: More About File Types
---

There are a few more things we’d like to point out about the file types you will encounter in ArcGIS, what they do and how to move them around. 

These are several important file types you will see frequently when working in ArcGIS.

| **File Type**                            | **Extension**    | **What it is**                           |
| ---------------------------------------- | ---------------- | ---------------------------------------- |
| Shapefile                                | .shp             | This stores the feature geometry of the shapefile. |
| Shapefile (XML file)                     | .shp (XML)       | There are 2 .shp files, one is an XML   file. The .XML file contains the metadata for the shapefile. |
| Shapefile index                          | .shx, .sbn, .sbx | An index file linking the .shp file to the .dbf file |
| Shapefile attribute table file stored as dBASE tabular data file | .dbf             | This is the table associated with the attributes for your shapefile – can be opened with Excel or Access. |
| Shapefile projection definitions file    | .prj             | Contains the projection information for the associated layer. |
| Text file                                | .txt             | A text file.                             |
| Info directory                           | info             | Info directory contains files which are associated with ARC/INFO coverages that you don’t want to move or delete. |
| Arc/Info coverage data files.            | .adf             | These are ARC/INFO coverage datafiles located in a directory with the coverage name. |
| Geodatabase containers                   | .mdb             | This contains a suite of files (you can view them in Microsoft access). |
| ArcGIS project document                  | .mxd             |                                          |
| Log file                                 | log              | This file records everything anyone   does to the files and when it was done. |

Please refer back to this [Lab 01 reference page](http://gis.joewheaton.org/assignments/labs/lab01/getting-organized-and-oriented/arcgis-10-desktop-orientation/working-with-arccatalog) for how some of these formats are displayed in ArcCatalog. See [here](http://spatialnews.geocomm.com/education/av_fileextensions.html) for information on commonly used extensions.

**IMPORTANT:** If you want to move your shapefile, you need to move all of these associated files together. A coverage can only be moved together with the INFO directory. If you separate the two you will corrupt the coverage. The best way to move files around is in ArcCatalog, because it keeps files together that need to be together (e.g., you can move the shapefile and all the associated files are automatically moved with it).

