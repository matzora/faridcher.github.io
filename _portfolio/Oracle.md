---
title: "Oracle DBMS"
excerpt: "A summary of my involvement with Oracle Spatial and Graph"
header:
  <!-- image: foo-bar-identity.jpg -->
  teaser: Oracle_Spatial.png
sidebar:
  - title: "Role"
    image: Oracle_Spatial.png
    image_alt: "Oracle logo"
    text: "Database SQL/PLSQL Programmer, Front-End Developer"
  - title: "Responsibilities"
    text: "Develope custom database functions and procedures for the web developer, prepare map based javascript code for the back-end web developer."
gallery:
  - url: taf/hq/Search.jpg
    image_path: taf/lq/Search.jpg
  - url: taf/hq/Print.jpg
    image_path: taf/lq/Print.jpg
  - url: taf/hq/SpatialQuery.jpg
    image_path: taf/lq/SpatialQuery.jpg
  - url: taf/hq/Layers.jpg
    image_path: taf/lq/Layers.jpg
  - url: taf/hq/Tools.jpg
    image_path: taf/lq/Tools.jpg
  - url: taf/hq/UpdateLayer.jpg
    image_path: taf/lq/UpdateLayer.jpg
---
{% include toc icon="" title="Table of Contents" %}

My experience with oracle spatial backs to 2012-2013; working as a database developer in private company, [NRS](http://www.nrsgeo.com/). I have been involved in a project for municipality called "detailed plan of Tehran". The technologies that were used in the project were ASP.NET, C#.NET, Oracle Spatial (DB back-end), Oracle maps (as a web map viewer) and ESRI ArcGIS with ArcSDE to edit the data.

## PLSQL / SQL
Working with large spatial tables with over 1 million parcels is a challenge even with the best database in the world. My main role was to develop and tune highly optimized spatial queries and save them as PLSQL functions/procedures so the C#.NET developer would call them from the application layer. To write highly performable spatial queries I had to take advantage of Oracle advanced features such as table partitioning and parallel query processing. 

### Spatial Queries and Tuning
Among many spatial operators and predicates available in oracle spatial, the most demanding operations were `buffering`, `intersect` and `nearest_neighbour` type of queries. For example: finding the zoning of a parcel which is the intersect of zoning and parcel layers. 
Various topological errors were present in the spatial layers that must be taken care of while building the queries, e.g. a parcel overlaps with more that one zoning feature.

### Adjacent Roads
A special algorithm in this project was to find the adjacent road network features to a selected parcel to extract the roads width and name attributes. We avoided using k nearest neighbor queries because we didn't know the k and the best search distance in advance.
After trying many algorithms we ended up with the following procedure to solve the problem:

- `Buffer` the road layer with a radius double the width of the road features (`R = 2 * Road_Width`)
- Select from buffered road using `intersect` of parcel and buffered road layers
- Extract the road width and name from the selected road features

It turned out that this simple algorithm was giving the best answer compared to other implemented approaches.

## Map Builder
Map builder is an Java SE application to create and define symbology for themes (layers), creating Base Maps, Tile Layers and etc. Map builder works mainly with the meta data tables of Oracle spatial so care must be taken while backing up the database tables.

## Oracle Maps Javascript API
OpenLayers, ArcGIS Server, Geoserver, UMN Mapserver were all possible candidates as the web map viewer component of the project. However Oracle Mapviewer javascript api was chosen as the mapping framework due to its performance, scalability and ease of use. Oracle Mapviewer being from the same company as in Oracle DBMS, has many javascript classes and functions for mapping between Oracle in database classes. Benchmarking Oracle Mapviewer over a weak Internet connection showed promising performance.
My role was to use the API to write client side (js) code for the following tasks:

- Showing the map, themes (e.g. feature layers), tile layers etc
- Creating fancy table of contents (TOC)
- Enable identify for some themes
- Export current map extent as jpeg/  png
- Simple feature creation and update using redlining
- Searching based on the attributes of some layers
- Securing spatial objects and layers


## Screen-shots
Here are some screen-shots of the final project:

{% include gallery caption="Snapshots of the Detailed Plan of Tehran" %}
