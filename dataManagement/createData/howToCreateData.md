# How To Create Your Own Data

To use either of the SchoolSite Extensions, three major datasets are required:

* [Study Areas](createStudyareas.md)

* Students

* Schools

 

For SchoolSite Projections Extension, there are two optional datasets that you can include but are not necessary to run the application:

 

* Streets

* Tracts

* Assessor

 

Each dataset has certain attribute data requirements which are listed in the following topics. Additional fields may be added as desired. All of these datasets should be created and saved in an Esri supported format. Supported Esri formats are listed below:

 

* File geodatabase

* Personal geodatabase

* Coverage

* Shapefile

 

File geodatabase is the preferred format. Please note that creating your own data assumes proficiency in ArcGIS software.

 

**Please Note:** Here are some notes that will help you create data that is compatible with SchoolSite:

* The spelling of each required field must be as shown in these help documents.

* Any null values generated when creating the required fields listed below must be converted to an empty string.

* SchoolSite does not support special characters such as periods, commas, ampersand, dashes, slashes, etc. (i.e. .,&-/`~) in any field in any dataset.

Any field in any dataset that is defined as a short integer cannot contain a number longer than 4 digits long. If you require a longer field, please define it as a long integer.

 

See Also:

