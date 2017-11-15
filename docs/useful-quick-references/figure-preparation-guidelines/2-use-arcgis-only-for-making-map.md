<<<<<<< Updated upstream
=======
<<<<<<< Updated upstream
>>>>>>> Stashed changes
---
title: 3. Use ArcGIS ONLY for Making Figure Building Block
---

The take home here, is **get out of ArcGIS as quick as possible**! Why? Because ArcGIS is a finicky, klutzy  slow and cumbersome environment that does not always behave consistently. There are more powerful and efficient software (see [intro](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines)) to put together a figure. Having said that, if you are making a simple figure, ArcGIS alone will often suffice. If you have any thoughts of using this figure for multiple purposes (e.g. a slide in a talk, on a poster, on a website and in a report), get into ArcGIS, do your analysis, make your image building block, and get out!

There are many options for making maps and using multiple data frames within one ArcMap document. 

The main options:

- One Stand-Alone Data Frame (recommended default)
- Two Data Frames (One full size; One Inset Map)
- Multiple Data Frame Tiles 

There are also several export options.  Which option you choose will depend on the level of control you anticipate needing over your map and map elements (i.e. scale bar, north arrow, legend) once you've exported them.  Generally we do not end up needing that much control over our maps since we won't make edits once maps been exported from Arc.  But there are some situations where you may need to make edits, such as if your supervisor insists the inset map frame should be red and not black or you may end up submitting your report as a manuscript to a journal that uses a different font style.   

**Export Options** (See [here](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00sm00000004000000.htm) for more info)

- Raster (default; e.g. `*.png, *.gif, *.jpg, *.tiff`) 

- - PROS:

  - - simple
    - small file size

  - CONS:

  - - cannot edit vector map layers
    - cannot edit text

- Vector (e.g.  `*.svg, *.ai, *.emf,``*.pdf)`

- - PROS:

  - - can edit vector map layers (e.g. change color, point size, line width) 
    - can edit text

  - CONS:

  - - HUGE file size (orders of magnitude larger than raster file)

- Dots Per Inch (DPI)

- - minimum: 300 dpi
  - higher quality: 500 - 800 dpi
  - **\*NOTE for Manuscript Figures**:*** **most journals will have a required dpi for submitted figures.  The required dpi may vary depending on if the figure is color, grayscale, or a combination of the two.  This information can generally be found under the journal's 'Author Guidelines' (e.g. [Geomorphology](http://www.elsevier.com/journals/geomorphology/0169-555X/guide-for-authors#57200)).  

**WARNING**: The biggest downside to exporting out of ArcGIS and into a vector graphics drawing package is you loose the ability to do meaningful spatial analyses, and you are no longer working with correctly georeferenced data. You need to be especially careful not to indepently re-scale different map features and scale bars (see video below for tips).

**Export combinations** based on the amount of control needed to make post-export edits:

- *No control* - Export both the map and map elements (i.e. scale bar, north arrow, legend) as a raster (e.g. *png)

- *Full Control* - Export the vector and raster map elements separately

- - Export the raster layers as a raster graphic (e.g. *.png)
  - Eport the vector layers and legend, north arrow, etc. elements as vector  (e.g. *.ai or *.pdf)

### Examples

In the video below Martha shows us how to export some typical map elements from ArcGIS so we can use them [later in Adobe Illustrator](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/4-assemble-the-figure-in-a-drawing-application/using-adobe-illustrator-to-assemble):

#### Exporting from ArcMap for Adobe Illustrator

<iframe width="560" height="315" src="https://www.youtube.com/embed/inLym0l3O1s" frameborder="0" allowfullscreen></iframe>

If you wish to follow along with the exact same data used in the video above, you can download the data from <http://etal.usu.edu/Downloads/ArcmapToIllustrator/>:

- [CHaMP Sites](http://etal.usu.edu/Downloads/ArcmapToIllustrator/CHaMPSites.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/CHaMPSites.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/CHaMPSites.zip)
- [Perennial Stream Drainage Network](http://etal.usu.edu/Downloads/ArcmapToIllustrator/PerennialStreams.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/PerennialStreams.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/PerennialStreams.zip)
- [Tucannon Hillshade](http://etal.usu.edu/Downloads/ArcmapToIllustrator/Tuc10mDEMClipHS.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/Tuc10mDEMClipHS.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/Tuc10mDEMClipHS.zip)
- [Tucannon Watershed Boundary ](http://etal.usu.edu/Downloads/ArcmapToIllustrator/TucannonWatershedUTM.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/TucannonWatershedUTM.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/TucannonWatershedUTM.zip)

In the video below, Sara shows us a slightly different version of above... Sara uses a few different methods, but both videos provide useful tips and tricks:

#### Export Options - Detailed Tutorial

<iframe width="560" height="315" src="https://www.youtube.com/embed/bQGepVTM9KM" frameborder="0" allowfullscreen></iframe>

← Back to  [2. Planning your Figure Layout](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/2-planning-your-figure-layout)

 Next to  → [4. Gather Up Your Other Figure Components](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/3-gather-up-your-other-figure-components)

<<<<<<< Updated upstream
=======
=======
---
title: 3. Use ArcGIS ONLY for Making Figure Building Block
---

The take home here, is **get out of ArcGIS as quick as possible**! Why? Because ArcGIS is a finicky, klutzy  slow and cumbersome environment that does not always behave consistently. There are more powerful and efficient software (see [intro](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines)) to put together a figure. Having said that, if you are making a simple figure, ArcGIS alone will often suffice. If you have any thoughts of using this figure for multiple purposes (e.g. a slide in a talk, on a poster, on a website and in a report), get into ArcGIS, do your analysis, make your image building block, and get out!

There are many options for making maps and using multiple data frames within one ArcMap document. 

The main options:

- One Stand-Alone Data Frame (recommended default)
- Two Data Frames (One full size; One Inset Map)
- Multiple Data Frame Tiles 

There are also several export options.  Which option you choose will depend on the level of control you anticipate needing over your map and map elements (i.e. scale bar, north arrow, legend) once you've exported them.  Generally we do not end up needing that much control over our maps since we won't make edits once maps been exported from Arc.  But there are some situations where you may need to make edits, such as if your supervisor insists the inset map frame should be red and not black or you may end up submitting your report as a manuscript to a journal that uses a different font style.   

**Export Options** (See [here](http://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//00sm00000004000000.htm) for more info)

- Raster (default; e.g. `*.png, *.gif, *.jpg, *.tiff`) 

- - PROS:

  - - simple
    - small file size

  - CONS:

  - - cannot edit vector map layers
    - cannot edit text

- Vector (e.g.  `*.svg, *.ai, *.emf,``*.pdf)`

- - PROS:

  - - can edit vector map layers (e.g. change color, point size, line width) 
    - can edit text

  - CONS:

  - - HUGE file size (orders of magnitude larger than raster file)

- Dots Per Inch (DPI)

- - minimum: 300 dpi
  - higher quality: 500 - 800 dpi
  - **\*NOTE for Manuscript Figures**:*** **most journals will have a required dpi for submitted figures.  The required dpi may vary depending on if the figure is color, grayscale, or a combination of the two.  This information can generally be found under the journal's 'Author Guidelines' (e.g. [Geomorphology](http://www.elsevier.com/journals/geomorphology/0169-555X/guide-for-authors#57200)).  

**WARNING**: The biggest downside to exporting out of ArcGIS and into a vector graphics drawing package is you loose the ability to do meaningful spatial analyses, and you are no longer working with correctly georeferenced data. You need to be especially careful not to indepently re-scale different map features and scale bars (see video below for tips).

**Export combinations** based on the amount of control needed to make post-export edits:

- *No control* - Export both the map and map elements (i.e. scale bar, north arrow, legend) as a raster (e.g. *png)

- *Full Control* - Export the vector and raster map elements separately

- - Export the raster layers as a raster graphic (e.g. *.png)
  - Eport the vector layers and legend, north arrow, etc. elements as vector  (e.g. *.ai or *.pdf)

### Examples

In the video below Martha shows us how to export some typical map elements from ArcGIS so we can use them [later in Adobe Illustrator](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/4-assemble-the-figure-in-a-drawing-application/using-adobe-illustrator-to-assemble):

#### Exporting from ArcMap for Adobe Illustrator

<iframe width="560" height="315" src="https://www.youtube.com/embed/inLym0l3O1s" frameborder="0" allowfullscreen></iframe>

If you wish to follow along with the exact same data used in the video above, you can download the data from <http://etal.usu.edu/Downloads/ArcmapToIllustrator/>:

- [CHaMP Sites](http://etal.usu.edu/Downloads/ArcmapToIllustrator/CHaMPSites.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/CHaMPSites.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/CHaMPSites.zip)
- [Perennial Stream Drainage Network](http://etal.usu.edu/Downloads/ArcmapToIllustrator/PerennialStreams.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/PerennialStreams.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/PerennialStreams.zip)
- [Tucannon Hillshade](http://etal.usu.edu/Downloads/ArcmapToIllustrator/Tuc10mDEMClipHS.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/Tuc10mDEMClipHS.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/Tuc10mDEMClipHS.zip)
- [Tucannon Watershed Boundary ](http://etal.usu.edu/Downloads/ArcmapToIllustrator/TucannonWatershedUTM.zip) [![http://etal.usu.edu/Downloads/ArcmapToIllustrator/TucannonWatershedUTM.zip](http://gis.joewheaton.org/_/rsrc/1397705972437/useful-quick-references/figure-preparation-guidelines/2-use-arcgis-only-for-making-map/winzip_icon_16.gif)](http://etal.usu.edu/Downloads/ArcmapToIllustrator/TucannonWatershedUTM.zip)

In the video below, Sara shows us a slightly different version of above... Sara uses a few different methods, but both videos provide useful tips and tricks:

#### Export Options - Detailed Tutorial

<iframe width="560" height="315" src="https://www.youtube.com/embed/bQGepVTM9KM" frameborder="0" allowfullscreen></iframe>

← Back to  [2. Planning your Figure Layout](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/2-planning-your-figure-layout)

 Next to  → [4. Gather Up Your Other Figure Components](http://gis.joewheaton.org/useful-quick-references/figure-preparation-guidelines/3-gather-up-your-other-figure-components)

>>>>>>> Stashed changes
>>>>>>> Stashed changes
