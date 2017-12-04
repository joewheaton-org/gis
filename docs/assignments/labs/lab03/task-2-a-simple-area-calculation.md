---
title: Task 2: A simple area calculation
---

Perhaps it would be nice to know what the area of each rock unit is and what percentage of the smaller map area it occupies. Here I will walk you through these simple calculations to illustrate the use of the geometry calculator for vector data sets. 

### Introduction

Either Save your Task1 map as new Task2 document, or start a new document and add the `UpdatedClippedGeoUnits` layer. 

The first thing we want to do is determine the areas for each rock type.

If you open the attribute table for the `UpdatedClippedGeoUnits `layer you will see that there is already an AREA field. There are three problems with this existing area field which came in the original shape file from the Geologic Survey. The first is that we don’t know the units for the values.  Given that the projection is UTM, and default units are meters, it is likely that it was square meters, but we’d have to check. The second problem is that in Task 1 we clipped this data layer so all of the units intersecting the edge of the map will have inaccurate areas. S*hapefile attributes (like the area field) don't update when a new output file is created.*

But in the bigger picture we have a bigger problem.  We want to know which rock unit Types represent at least 5% of the total map area.  If you look in the attribute table of the 

```
UpdatedClippedGeoUnits 
```

layer and sort the rock unit name field, you will see that there are multiple polygons for each rock type.  To get a more accurate representation of rock type area, we need to combine these polygons into one record.  To do this you can use the "dissolve" tool (Data Management). 

### Dissolving

The Dissolve tool allows us to 'merge' polygons based on attributes in a specific field (in this case "UnitName"). Don't set the statistics to calculate SUM. Leave that, but make sure you leave the box checked to allow for multi-part polygons.

[![dissolve]({{ site.baseurl }}/assets/images/dissolve.jpg)]({{ site.baseurl }}/assets/images/hr/dissolve.jpg)

- Run the Dissolve tool and evaluate the results in the attribute table.  Sort on the UnitName field. You should see one of each rock unit type (although many have duplicates with question marks).  
- Clip this Dissolved rock type layer to the boundary of the Clip Extent if you haven't already done so.
- In the attribute table of the newly clipped dissolved rock type layer, Add a field "Area_m2" type float.
- Calculate Geometry (Right Click on the header) of each polygon
- Find the total area by summing these areas (right click on the header > Statistics > Copy the Sum)
- Add a field "prop_tot" (for proportion of the total area) - type Float
- Do a Field Calculation (right click on "prop_tot") by dividing the area field by the total area
- Sort the resulting proportions Descending and evaluate. You should have six rock types that make up at least 5% of the total map area.

### Calculating Area

- We will calculate new areas, this time in square kilometers.

- - Open the attribute table of the **Dissolved** `UpdatedClippedGeoUnits` layer.
  - Scroll over to the `AREA_SQ_K` field (you have to add this field to the dissolved table). Highlight the column by clicking on the `AREA_SQ_K` header.
  - Right click on the `AREA_SQ_K` header and bring up the [Calculate Geometry](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//005s00000027000000.htm) dialog box:

[![g13]({{ site.baseurl }}/assets/images/g13.png)]({{ site.baseurl }}/assets/images/hr/g13.png)

- - It doesn't matter if you calculate in sq m or sq km as long as you keep track of your units.

  - 

  - Choose to calculate the area, using the data source's coordinate system. Click

  -  

  - OK

  - . 

  - You now have the area of the dissolved rock unit polygons for the extent of the data. 

  - (Note: it is a good idea when creating new fields for area or length calculations to include the units in the field name for future reference.)

### Calculate Areas as a Proportion of the total

Now we want to calculate the percent of rock unit type relative to the map's area.  

To calculate percent of total area for each rock type, we first need to know the area of the whole map. You can either derive map area from the clip extent polygon (add a field to the attribute table and calculate area just like above) or sum the areas of the rock type polygons in the dissolved clipped rock type layer.

To do the latter:

- In the attribute table of the CLIPPED rock type layer, right click on the Area header > Statistics > then look at the sum. 
- Control C to copy that value

Now you know the map's area, Calculate the proportion each rock type's area is of the total area:

- Add another field "prop_tot" to the same attribute table

- Right click the header > Field Calculator

- Using the buttons, create an equation to divide the area field by the total map area.

- - Make sure you use the buttons whenever possible
  - Double click on "area_m2" and the 'divide' button then Ctrl V to paste the area sum.
  - OK to run

- Sort the results descending and evaluate.

Create a table for your website in which you report the rock names, areas with units, and proportion or percent of the total area (with clear units).

This task illustrated how you can do some simple analyses of spatial data.

<- [Back to Task 1 ]({{ site.baseurl }}/assignments/labs/lab03/task-01---reproduce-geologic-map)         ^ [Back to Main Lab Page]({{ site.baseurl }}/assignments/labs/lab03)

