---
title: 4. Gather Up Your Other Figure Components
---

If you are making a simple figure that is ONLY a map, you can skip this step. However, if your figure includes things like:

- Tables 
- Graphs & Plots
- Images
- Other Maps

you'll want to get all these graphic pieces organized so you can assemble them in your figure. The key things are: 

1. to keep track of whether or not these components are going to be inserted from clipboard (i.e. control C and control V) or exported to a file and inserted from a file, and
2. to distinguish between vector vs. raster formats for these other graphic components (these are slightly different than vector [GIS file formats](http://gis.joewheaton.org/topics/digitalmaps/more-about-file-types)... rasters file types can overlap, but to be used in GIS need some georeferencing information in form of `*.xml` or world file). 

A table, for example, is vectorized when it consists of actual lines and editable text; and is rasterized when it is just an image. Some programs (e.g. Excel) will allow you to copy a vectorized graphic into a vector drawing program where you make the figure (just using the clipboard). Others will let you export either a vector graphic or raster graphic to a file. In general, vectorized formats provide the most flexibility in that they can be edited and modified, but can also quickly lead to huge file sizes and become cumbersome to work with. The encapsulated post script format (`*.eps`) is one of the most common vector file formats. Other common vector file formats include `*.svg, *.ai, *.emf, *.dxf, *.vml `and even` *.pdf `can act as a vector format (e.g. when exported from ArcGIS). Most of the programs (e.g. Excel, R, SAS, Matlab) where you might make tables, graphs, plots, or images (even ArcGIS) allow you to export those figures as raster images (e.g. `*.png, *.gif, *.jpg, *.tiff`) , and some copy these images to a clipboard as rasters. Also, just to confuse you, some vector formats (e.g.` *.ai` and `*.pdf`) allow the inclusion of both raster and vector objects in the vector document. 

#### Rules of Thumb and Trade-Off

1. If you are going to use components in multiple places, export them to files once, so they can be resused consistently. For example, I often export my legends that I reuse separately and keep them as *.png and *.ai files. 
2. Unless you want to edit text and or linework later, it is easier to work with raster files. I would export things with transparent backgrounds, in a *.png format at 600 to 800 DPI (300 DPI minimum). This generally works for many typical situations in that it produces reasonably small size files and preserves resolution.
3. Limit the amount of text labels you use in these figure components to the bare minimum (because if you take advice above you can't edit it). Add text in the drawing program.

------

← Back to  [3. Use ArcGIS ONLY for Making Figure Building Block](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map)

 Next to  → [5. Assemble the 'Figure' in a Drawing Application](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/4-assemble-the-figure-in-a-drawing-application)

