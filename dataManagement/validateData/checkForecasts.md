# Data Checks Made for Forecasts - SEE NOTES
Below is a list of the data checks that SchoolSite Pro makes when using DataSet Up specifically for use in forecasts.

## Step 1: Validate individual feature classes
There are three required fields that must be added to the geocoded student attribute table in order for SchoolSite Pro to properly identify students to be excluded or optionally included in the enrollment forecasts.:

1. [Study Areas](../createData/createStudyareas.md)
2. [Schools](../createData/createSchools.md)
3. [Students](../createData/createStudents.md)
 

Additionally, there are two optional datasets you can import for use in forecasts:
1. [Tracts](../createData/createTracts.md)
2. [Assessor Data](../createData/createAssessor.md)


## Step 2: Validate feature class relationships
### Schools vs. Study Areas
* Check StudyArea field ELEM_ vs. Schools field ELEM_
  * If a StudyAreas record has ELEM_ > 0, then there needs to be one record in Schools that contains the same ELEM_

* Check StudyArea field MID_ vs. Schools field MID_
  * If a StudyAreas record has MID_ > 0 then there needs to be one record in Schools that contains the same MID_

* Check StudyArea field INT_ vs. Schools field INT_
  * If a StudyAreas record has INT_ > 0, then there needs to be one record in Schools that contains the same INT_

* Check StudyArea field HIGH_ vs. Schools field HIGH_
  * If a StudyAreas record has HIGH_ > 0, then there needs to be one record in Schools that contains the same HIGH_

### Students vs. Study Areas
* Check STUTYPE to see if any RS students live out of district
  * If, spatially, a student lives outside the study areas boundaries but is labeled 'RS', then auto-correct to 'OD' student type

### Students vs. Schools
* Check Students field SCHL_CODE vs. Schools field SCHL_CODE
  * For each value in the Students field SCHL_CODE there needs to be one record in Schools that contains the same value in SCHL_CODE.

* Check Students are within their school's grade range

### Tracts vs. Study Areas
* Check Tracts field STDYAREA vs. Study Areas field STDYAREA
  * For each value in the Tracts field STDYAREA, there needs to be only one record in Study Areas that contains the same value in the field STDYAREA

### Tracts vs. Assessor
* Check Tracts field TYPE vs. Assessor field "Housing Type"
  * For each value in the Tracts field TYPE, there needs to be at least one record in Assessor that contains the same value in "Housing Type"
