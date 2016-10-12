---
title: "GE Smallworld GIS"
excerpt: "One year and half of experience with Smallworld GIS"
header:
  <!-- image: foo-bar-identity.jpg -->
  teaser: smallworld.png
sidebar:
  - title: "Role"
    image: smallworld.png
    image_alt: "Smallworld GIS logo"
    text: "Software Developer, Support"
  - title: "Responsibilities"
    text: "Develope and support software modules written in Magik Programming language"
gallery:
  - URL: foo-bar-identity.jpg
    image_path: foo-bar-identity-th.jpg
---
{% include toc icon="" title="Table of Contents" %}

I have had almost 18 months (2014-2015) of experience with Smallworld GIS. The company I worked with, [Behineh Rassam Pars (BRP)](http://rassam-pars.ir/), was mainly involved in utility GIS software projects. The purpose was to create a GIS solution for electricity and gas companies. The end products were like those of [ArcFM](http://resources.arcfmsolution.com/), but our platform was GE Smallworld rather that ESRI GIS stack.

## Shape Exporter
Smallworld GIS didn't have a built-in shapefile exporter. The customers didn't want to use FME due to its complexity. My task was to write an interface to convert native Smallworld spatial layers to shapefile. I used [shapelib](http://shapelib.maptools.org/) and Smallworld `TICS` C library and some Magik code to develop the application.

## Oracle Insync
To replicate Smallworld VMDS (version managed data store) in oracle, I had to utilize Oracle Insync technology. However, `Oracle InSynch` had many bugs while working with Persian character encoding which caused the system to crash. My role was to debug and setup Oracle Insync in a way to run smoothly and in an automated fashion without user intervention.

## Digsilent Converter
I also wrote some Magik code to convert GIS objects to DigSilent objects. 

The bottom line is that, despite my huge involvement in the Smallworld platform during this period, I concluded that it is not a promising platform to invest more time in it.
