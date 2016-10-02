---
title:  "ArcGIS Command's GUID Generator"
mathjax: false
categories: 
  - software
tags:
  - arcgis
  - arcobjects
  - extension
---

Those who have been involved in ESRI SDKs software development know how important it is to now the GUID of some commands. In this regards I developed an extension that enables you to catch the GUID of any command or button you click in ArcMap. To try the extension see the [project page](https://github.com/faridcher/ArcGIS-GUID).

## Features

This ArcMap Addin shows command details (GUID, Name, Subtype, ...) when you click a command in ArcMap, A creative tool for an ArcGIS Desktop Developer.
In ArcObjects [documentation](http://resources.arcgis.com/en/help/arcobjects-net/conceptualhelp/index.html#//00010000029s000000), there is a list of popular commands accompanied by their corresponding GUIDs. Looking for a command in this document page could be tedious and frustrating, and most of the time you get disappointed at finding a command.

GUID (Global Unique Identifier) of a command is useful when:

- You want to programmatically call a pre-built command.
- You may want to customize ArcGIS UI (User Interface) programmaticaly.
- You want to create a python Addin toolbar with a custom set of built-in commands and tools. For more information click
  [here](http://blogs.esri.com/esri/arcgis/2012/08/27/python-add-ins-how-to-add-built-in-commands-to-your-custom-toolbar-or-menu).
  
In all these scenarios you need the built-in command or tool GUID.

The Addin is built for ArcGIS Desktop 10.2, although it should also work with higher versions too.

## Snapshot

![ArcGIS GUID Interceptor Snapshot](http://faridcher.github.io/uploads/ArcGIS-GUID.png)
