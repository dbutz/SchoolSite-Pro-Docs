# Data Checks Made for Redistricting Plans - SEE NOTES

Below is a list of the data checks that SchoolSite Pro makes when using DataSetup specifically for redistricting plans.

## Step 1: Validate individual feature classes

These are the three required fields that must be added to the geocoded student attribute table in order for SchoolSite Pro to properly identify students to be excluded or optionally included in the various types of redistricting plans.:

1. [Study Areas](../createData/createStudyareas.md)
2. [Schools](../createData/createSchools.md)
3. [Students](../createData/createStudents.md)


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

## Students vs. Schools
* Check Students field SCHL_CODE vs. Schools field SCHL_CODE
  * For each value in the Students field SCHL_CODE there needs to be one record in Schools that contains the same value in SCHL_CODE.

* Check Students are within their school's grade range

 
