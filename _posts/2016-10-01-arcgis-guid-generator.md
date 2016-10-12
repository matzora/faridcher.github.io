---
title:  "ArcGIS commands GUID generator"
mathjax: false
categories: 
  - software
tags:
  - arcgis
  - arcobjects
  - extension
---

Those who have been involved in ESRI software development know how important it is to know the GUID of some commands. In this regard, I have developed an extension that enables you to catch the GUID of any command or button you click in ArcMap. To try the extension see the [project page](https://github.com/faridcher/ArcGIS-GUID).

## Features

This ArcMap Addin shows command details (GUID, Name, Subtype, ...) when you click a command in ArcMap; it is a creative tool for an ArcGIS desktop developer.
In ArcObjects [documentation](http://resources.arcgis.com/en/help/arcobjects-net/conceptualhelp/index.html#//00010000029s000000), there is a list of popular commands accompanied by their corresponding GUIDs, although looking for a command in this page could be tedious and frustrating, and most of the time you get disappointed at finding a command.

GUID (Global Unique Identifier) of a command is useful when you want to:

- programmatically call a pre-built command or tool.
- customize ArcGIS UI (User Interface) programmatically.
- create a python Addin toolbar with a custom set of built-in commands and tools. For more information click [here](http://blogs.esri.com/esri/arcgis/2012/08/27/python-add-ins-how-to-add-built-in-commands-to-your-custom-toolbar-or-menu).
  
In all these scenarios you need the built-in command or tool GUID.

The Addin is built for ArcGIS Desktop 10.2, although it should also work with higher versions.

## Snapshot

![ArcGIS GUID Interceptor Snapshot](http://faridcher.github.io/uploads/ArcGIS-GUID.png)
