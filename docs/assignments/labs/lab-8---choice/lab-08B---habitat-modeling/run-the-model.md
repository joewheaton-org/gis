---
title: Run the Model
---

Task 1: Run the 

**Probability of Ungulate Utilization (**

grazing capacity) three input FIS

- **Step 1: **Click on the MATLAB R2012a icon to start the program.
- **Step 2:** Browse to the location where the model: `GrazingCapacity_3input.fis` is stored. You want the contents of the folder containing this `GrazingCapacity_3input.fis `file to display in the window on the left side of the Matlab screen:

![Ungulate_FIS_1]({{ site.baseurl }}/assets/images/Ungulate_FIS_1.png)

- **Step 3:** In the command window type FIS_IT and the press enter.  If you get an Undefined function or variable error on the 'FIS_IT' command, you don't have the proper path (or folder) loaded in the directory window. 

Update the directory window and type the FIS_IT command again until the dialog box (below) prompts you to select an FIS:

The below dialog box should open and prompt you to select an FIS:

![Ungulate_FIS_2]({{ site.baseurl }}/assets/images/Ungulate_FIS_2.png)

Then you are prompted to Select the folder that contains your inputs.

Select the inputs folder (single click to add to 'Folder' window and choose 'Select Folder').

The below dialog box should open and prompt you to select Vegetation_Preference Input Raster:

![Ungulate_FIS_3]({{ site.baseurl }}/assets/images/Ungulate_FIS_3.png)

- **Step 5:** Path to the GrazingCapacityFIS/Input folder and selected the input_veg.asc

The below dialog box should open and prompt you to load slope input raster:

![ungulate_FIS_4]({{ site.baseurl }}/assets/images/ungulate_FIS_4.png)

- **Step 6:** Path to the  GrazingCapacityFIS/Input folder and selected the input_slope.asc.

The below dialog box should open and prompt you to load water source input raster (Distance_To_Water):

![Ungulate%20dist_water]({{ site.baseurl }}/assets/images/Ungulate%20dist_water.png)

- **Step 7: **Path to the GrazingCapacityFIS and selected the distance_to_water.asc

The FIS should now start calculating… this may take a several minutes.

The below dialog box should open and prompt you to save your FIS 

![Ungulate_FIS_save]({{ site.baseurl }}/assets/images/Ungulate_FIS_save.png)

 Then it will need to save the FIS Grid to a File.  This will take a bit longer than the previous step.

**Task 2: Convert the FIS output ASCII raster to .img raster**

- **Step 1:** Open ArcMap

- **Step 2:** load the output FIS output ASCII

- **Step 3:** Use the ASCII to Raster command

- - Output format should be FLOAT

![ASCII_to_Raster]({{ site.baseurl }}/assets/images/ASCII_to_Raster.png)

- **Step 4:** Output the FIS grid to the output folder.  This is the final step of the probability of ungulate utilization.  

You may need to Calculate Statistics on the output .img raster.  Additionally you may need to define a projection (Define Projection tool) for the new raster (NAD 83 UTM Zone 12N).  Note that the range of output values should be 0 - 1 (or nearly 1). The legend has been edited/relabeled and simplified.

![Escalante_Prob_Ungulate_distribution]({{ site.baseurl }}/assets/images/Escalante_Prob_Ungulate_distribution.png)

The final output should look something like the above.

