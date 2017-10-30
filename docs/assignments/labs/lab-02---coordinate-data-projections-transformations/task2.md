---
title: Task 2 - Transforming Data Using CTT
---

#### Introduction

The key to transforming any data from one coordinate system to another coordinate system is having some coordinate values for the same points (typically 2-5) in BOTH coordinate systems. In our case, we want to transform survey data in un-projected assumed Cartesian coordinate space to real world projected coordinates (NAD 83 UTM Zone 12 N), and we have three benchmarks to do it. The benchmarks were surveyed in with both a total station (very precise: +/- 5 mm) in an assumed coordinate system, and in real world coordinates with a very inaccurate hand held GPS (+/- 5 m). However, using the GPS coordinates as a basis for a simple affine transformation (i.e. a shift, rotate and datum adjustment), these coordinates will be good enough for GIS overlay purposes. The cartoon below illustrates conceptually the process of shifting and rotating the total station survey data using the GPS coordinates of the same points. In the example below, BM3 is used as the point around which the transformation is based (click on image for larger view). You will use the CHaMP Transformation Tool to help you. 

#### Download & Look at GPS Data

Download [`CBW05583-028079 Benchmarks.csv`](http://etal.usu.edu/Courses/GIS/2012/Labs/Lab02/CBW05583-028079%20Benchmarks.csv) and open these in Excel or a Notepad. If you want an explanation of these data and how we will use them, see this video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/pRjWrJ7svc8" frameborder="0" allowfullscreen></iframe>

#### Install CHaMP Toolbar

Install [CHaMP Transformation Tool](http://ctt.joewheaton.org/home/download-tool) Add-In (download [here](http://ctt.joewheaton.org/home/download-tool); installation instructions [here](http://ctt.joewheaton.org/read-me#TOC-Installation-Procedure-)). Make sure you do not have ArcGIS running when you install the Add-in and download the correct version (10.0/10.1).

<iframe width="560" height="315" src="https://www.youtube.com/embed/Gz3jtxLN474" frameborder="0" allowfullscreen></iframe>

#### Get Map Document Ready to Go

Start a new empty ArcMap Document and get oriented.

<iframe width="560" height="315" src="https://www.youtube.com/embed/etY2YOpumOY" frameborder="0" allowfullscreen></iframe>

#### Apply CTT to Unprojected Data

You can follow the CTT example [here](http://ctt.joewheaton.org/home/how-to-use-the-ctt) (using your data instead) to transform the unprojected data into projected coordinates using the CTT. Choose the best transformation parameters based on a combination of visual inspection and minimization of residual errors. Alternatively, the video below shows you how to do the same thing, but with the same data you're working with.

<iframe width="560" height="315" src="https://www.youtube.com/embed/VTx0bKZqJEY" frameborder="0" allowfullscreen></iframe>

Remember to take a measurement between CP1 and CP3 to verify that the intrinsic accuracy of the data hasn't been destroyed in the transformation.

Make note of your residuals for your submission.

