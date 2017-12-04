---
title: Lab 08B - Habitat Modeling
---

## Introduction to Lab

#### Background

Habitat models take many different forms. In this lab, we will run a very simple habitat model that predicts the probability of occupancy of ungulates on the landscape. In lecture, we discussed many types of different habitat models, but all the models had in common a number of inputs that help characterize abiotic physical habitat and then some 'model' that scores those inputs and combines them together to give an output.

In this lab we're going to try and figure out where the ungulates (cows) would hang out when left to their own devices. On many federal allotments  the cows are largely left to their own devices. They get dropped off in early summer and picked up in the fall. Active management (e.g. fencing and hiring riders to keep them moving) can significantly change these patterns. 

[![IMG_1942]({{ site.baseurl }}/assets/images/IMG_1942.jpg)]({{ site.baseurl }}/assets/images/hr/IMG_1942.jpg)

#### Data for Lab

- ![img]({{ site.baseurl }}/_/rsrc/1293667540566/config/pagetemplates/lab-template/zip_icon.gif) [Matlab Model & Input Data Files](http://etal.usu.edu/GCT/GrazingCapacity_FIS_InputsOnly.zip)

Given how hard we've been working you the past three labs, we're going to lighten the work-load of this lab (allow you to have a spring break). A major challenge in running these models is getting all your inputs together and in a consistent format. We've scaled back the scope of this lab.  Instead of having you plow through the tedious task of finding, cleaning up, and processing your inputs, we are simply providing you with the correctly formatted inputs for running the model in Matlab. The trickiest thing you'll have to deal with is getting the ascii rasters to display properly in ArcGIS (something you should be an expert at by now - HINT - calculate statistics and change display properties). 

------

#### Lab Objectives

- Gain experience running fuzzy logic model using common and familiar spatial datasets
- Exposure to Matlab
- Articulate a critical evaluation of model, methodology, and model outputs

Meets [Course Learning Outcomes]({{ site.baseurl }}/about/primary-learning-outcomes) 3 & 5. 

------

### Instructions & Lab Tasks

Overview of tasks

- Task 1 - Run an ungulate occupancy model for the Escalante Watershed

------

#### Task 1

 

Run the Matlab ungulate occupancy model with the inputs provided.  Note you will need Matlab with the fuzzy logic toolbox installed to run this lab. Matlab (and the required fuzzy logic toolbox) is available on the Quinney lab computers. You can complete the remaining ArcGIS portion of the lab elsewhere if you so desire. 

Create figures for each of the model inputs. Use the ascii to raster tool (see end of "Run the Model" section for details about this process). 

#### More Detailed Information & Instructions

- [Background on the Fuzzy Black Box]({{ site.baseurl }}/assignments/labs/lab-8---choice/lab-08B---habitat-modeling/background-on-the-fuzzy-black-box)
- [Inputs]({{ site.baseurl }}/assignments/labs/lab-8---choice/lab-08B---habitat-modeling/inputs)
- [Run the Model]({{ site.baseurl }}/assignments/labs/lab-8---choice/lab-08B---habitat-modeling/run-the-model)

### What to Submit

Prepare a webpage for this lab on your personal website for the course and prepare the following within that page or subpages (child pages):

- **Description and justification of methods**
- **Figure(s) for each of the inputs**
- **Figure for output**
- **Description of results and critical evaluation of model and what it produces**

The workload in this lab is light; the critical evaluation will be worth devoting time to.

Make sure your lab conforms to the general [lab submission guidelines](http://a/joewheaton.org/gis-wats-4930-6920/labs#TOC-Lab-Submission-Guidelines). Submit a URL for this lab's webpage.

------

### Additional Resources

#### [Escalante River Watershed 10 m DEM](http://etal.usu.edu/Courses/GIS/2013/Lab/Escalante__10mDEM.zip)

#### Tutorial or Step-by-Step Instructions for Specific Tasks

- [Ungulate Capacity Model](http://brat.joewheaton.org/home/documentation/manual-implementation/ungulate-capacity-model) from BRAT  website - *Same as your instructions on this site.*

#### Web Links:

- MacFarlane WW and Wheaton JM. 2013. [Modeling the Capacity of Riverscapes to Support Dam-Building Beaver - Case Study: Escalante River Watershed](http://etal.usu.edu/GCT/BRAT_Final_Report.pdf), Final Report Prepared for Grand Canyon Trust and the Walton Family Foundation, Logan, UT, 79 pp.
- [Beaver Restoration Assessment Tool](http://brat.joewheaton.org/) website - *BRAT*

#### Follow up Activities:

- You could of course derive these inputs on your own for a different location, with nothing more than a DEM and LANDFIRE data. 

- You could modify the `GrazingProb_3input.fis `to change any of the following:

- - Number and type of inputs
  - The number and text description of categories (e.g. low, medium, high vs. just low and high)
  - Calibrate input membership functions or output membership
  - Change rule table that drives model

- Write your own model that instead of combining the inputs as we have here through a fuzzy inference system, score the inputs using habitat suitability curves (HSCs) and combine in to a global habitat suitability index (HSI). See [here for examples of HSIs](http://www.nwrc.usgs.gov/wdb/pub/hsi/hsiindex.htm) for many different species. 