# What Kind of Data Do I Need?

## Map Datasets for Use with SchoolSite Pro
In order to use the SchoolSite Pro Extensions, you must have the following **required** map datasets:

 

1. **Study Areas** - A polygon dataset of the district showing planning areas coded by school attendance areas

1. **Schools** - A point dataset of schools geocoded to a street dataset of the district

1. **Students** - A point dataset of students geocoded to a street dataset of the district

 

Additionally, the following datasets are optional and not necessary to run the application, but can help you with other features in SchoolSite Pro:

 

4. **Streets** - A line dataset

5. **Tract** - A point or area dataset of planned residential development within the district

6. **Assessor** - A point feature of existing housing data within the district. This dataset is necessary only if you wish to run maturation projections or create student yield factors.

 

## Data Formats
Although the [feature class](https://desktop.arcgis.com/en/arcmap/latest/manage-data/geodatabases/feature-class-basics.htm) is the recommended format for ArcGIS Pro, any of the following Esri formats can be used to store your data for use with SchoolSite Pro and to create Redistricting Plans or Forecasts:

 

* ArcGIS File Geodatabase Feature Class

* ArcGIS Personal Geodatabase Feature Class

* ArcGIS SDE Geodatabase Feature Class

* Esri Shapefile

 

Each of the three dataset attributes must be precisely defined in order to run the application.  To learn about field/attribute definitions required for SchoolSite Pro, refer to the topic ["How to Create Your Own Data"](../dataManagement/createData/howToCreateData.md).

**See Also:**

[What Are Study Areas?](studyAreas.md)

[Where Can I Obtain Data?](obtainData.md)

[How to Create Your Own Data](createData/howToCreateData.md)
