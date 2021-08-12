# Organizing Your Data
The diagram below is a possible suggestion for organizing all of your GIS data holdings as well as your SchoolSite Redistricting Plans and Projections.

<p align="center">
  <img src="organizingData.png">
</p>

**This organizational layout including Windows folders, and geodatabases accomplishes the following:**

* Organizes data by school year to provide for archiving older data for easy access.

* Organizes data by functions including map data geodatabases in one location as well as map documents and annual SchoolSite projections (and possible redistricting plans) in other easily recognizable locations.

* Provides for easy copying of main data sets (streets, study areas, schools, etc.) into future years for ongoing updates and maintenance.

 

## Brief Rationale
First and foremost, all map data holdings should be stored within an Esri geodatabase format.  We do not suggest that your long-term data be in shapefile format due to editing and other limitations within the ArcGIS software.

 

Data should, if possible, be stored on an shared network file server for access by different users as well as the likely possibility of nightly data backups as part of typical IT data strategy.  In the example diagram, we have indicated a network drive as S:\ with a GIS_DATA folder.

 

Data is stored by "school year" so that the most recent updated mapping and other data can be easily located and a logical progression of historical data can be created.  These folders under GIS_DATA are indicated by Schlyr1415 (ie. school year 2014-15), Schlyr1516 (school year 2015/16), etc.  As a new year approaches in July, a new folder can be created in Windows Explorer or ArcCatalog and certain data copied into the new folder for ongoing update and maintenance.

 

Under each school year folder, we have created additional folders which organize our data holdings by type.  Data types include our geodatabases (GDB folder), map documents that we create within ArcMap (Map_Docs folder), layer files that we also create in ArcMap and that are used to quickly add new symbolized layers within map documents (Layers folder), and our SchoolSite Projections and Redistricting Plans which are stored under the SchoolSite folder.

 

## GDB Folder
Under the GDB folder are several Esri geodatabases (typically file geodatabases over other types of geodatabases for performance and data size considerations).  The Basemap.GDB geodatabase contains the Main feature dataset.  The Main feature dataset contains the feature classes that are typically updated on an ongoing basis by the school district including streets, study areas (and the inherent school attendance zones through attribute codes), school locations and development tracts.  A topology set of rules are setup for streets (ie. streets must not have dangles) and a separate set of topology rules are setup for study areas (ie. study area polygons must not have gaps or must not have overlaps. If desired from an editing "comfort" standpoint, the streets (and streets topology) can be copied from one geodatabase to another for editing purposes and then copied back after accuracy validation.  An Address Locator for student geocoding purposes against the reference data such as streets is maintained in the Basemap geodatabase.  It should be remembered to "rebuild" the address locator if any editing has been accomplished on the reference street data.

 

The Students_091614.GDB geodatabase contains all items related to the geocoding of students including the original data table extract (in this example rawstudent.txt) from the district's student information system (SIS).  The date of the student extract from the SIS in this example is 09/16/2014.  Additional student geocoding during other times of the year, if necessary and desired, are placed within additional Student geodatabases with appropriate date related names. All geocoded students are placed within the geodatabase as the feature class, StudentsAll.

 

The Misc.GDB geodatabase contains feature classes that typically do not change (ie. lakes, railroads, etc) or are obtained and updated by other agencies (ie. parcels).  This geodatabase can be used to store a variety of feature classes.

 

## Map_Docs Folder
This folder contains all of the map documents (.mxd)  that you might create within ArcMap during the course of the year. For further organizational purposes, you might consider creating subfolders for each individual map document which might contain the .mxd as well as supporting files that are created during analysis or specific mapping purposes within that map document. This possible sub-folder structure allows you to quickly remove or delete selected map documents that are no longer needed (by deleting the subfolder) including all of the supporting files associated with the map document. This is a good way to keep your map documents and any associated files organized.

 

If you wish to keep any map documents that are critical for year-to-year mapping tasks you can copy the .mxd to the next year's Map_Docs folder using Windows Explorer or ArcCatalog and correct the data source pathnames for the layers in the map document to the new location of the feature classes.

 

## Layers Folder
The same discussion for the Map_Docs folder holds true for the Layers folder. See above discussion.

 

## SchoolSite Folder
The SchoolSite folder can be organized in a variety of ways. One solution is to create a subfolder for redistricting plans and a second subfolder for projections. Each folder would contain a SchoolSite geodatabase with the appropriate items. By maintaining your projections and redistricting plans under the SchoolSite folder in a particular school year, the user can always go back to revisit  (ie. open within SchoolSite) the projections or boundary plan options considered in previous years.


 
