# How To Create Your Own Data - REVIEWED

To use either of the SchoolSite Pro Extensions, three major datasets are required:

* [Study Areas](createStudyareas.md)

* [Students](createStudents.md)

* [Schools](createSchools.md)

 

For SchoolSite Pro Forecasts Extension, there are two optional datasets that you can include but are not necessary to run the application:

 

* [Streets](createStreets.md)

* [Tracts](createTracts.md)

* [Assessor](createAssessor.md)

 

Each dataset has certain attribute data requirements which are listed in the following topics. Additional fields may be added as desired. All of these datasets should be created and saved in an Esri supported format. Supported Esri formats are listed below:

 

* File geodatabase



Please note that creating your own data assumes proficiency in ArcGIS software.

 

**Please Note:** Here are some notes that will help you create data that is compatible with SchoolSite Pro:

* The spelling of each required field must be as shown in these help documents.

* Any null values generated when creating the required fields listed below must be converted to an empty string.

* SchoolSite Pro does not support special characters such as periods, commas, ampersand, dashes, slashes, etc. (i.e. .,&-/`~) in any field in any dataset.

Any field in any dataset that is defined as a short integer cannot contain a number longer than 4 digits long. If you require a longer field, please define it as a long integer.

 

See Also:

* [Creating Study Areas](createStudyareas.md)
* [Creating Students](createStudents.md)
* [Creating Schools](createSchools.md)
* [Creating Tracts](createTracts.md)
* [Creating Assessor Data](createAssessor.md)
* [Creating Streets](createStreets.md)

