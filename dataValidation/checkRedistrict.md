# Data Checks Made for Redistricting Plans

Below is a list of the data checks that SchoolSite Pro makes when using the Data Validator for the Redistricting Extension.

## Step 1: Validate individual feature classes
There are three required datasets that are required for Redistricting plans:

1. Study Areas
2. Schools
3. Students
 

## Study Areas
* Validate contains field STDYAREA,  field is type Text, and maximum length is 6
* Validate contains field ELEM_, and field type is Short Integer
* Validate contains field MID_, and field type is Short Integer
* Validate contains field INT_, and field type is Short Integer
* Validate contains field HIGH_, and field type is Short Integer
* Validate contains field DISTRICT, field type is Text, and maximum length is 50
* Validate contains field MOBILITY, field type is Text, and maximum length is 3
* Validate contains field ELEM_DESC, field type is Text, and maximum length is 50
* Validate contains field MID_DESC, field type is Text, and maximum length is 50
* Validate contains field INT_DESC, field type is Text, and maximum length is 50
* Validate contains field HIGH_DESC, field type is Text, and maximum length is 50
* Check fields STDYAREA, ELEM_, MID_, INT_, HIGH_, DISTRICT, MOBILITY, ELEM_DESC, MID_DESC, INT_DESC, and HIGH_DESC
  * Validate no null records in each of these fields
* Check field STDYAREA
  * Validate no duplicate values
  * Validate no special characters
* Check field ELEM_
  * If one record has ELEM_ > 0, then all records must have ELEM_ > 0
* Check field MID_
  * If one record has MID_ > 0, then all records must have MID_ > 0
* Check field INT_
  * If one record has INT_ > 0, then all records must have INT_ > 0
* Check field HIGH_
  * If one record has HIGH_ > 0, then all records must have HIGH_ > 0
* Check fields ELEM_, MID_, INT_, and HIGH_
  * If a record has 9999 in one of these fields then all of these fields must be 9999 for that record

## Schools
* Validate contains field NAME,  field type is Text, and maximum length is 50
* Validate contains field SCHL_CODE, and field type is Short Integer
* Validate contains field STRT_GRD, and field type is Short Integer
* Validate contains field END_GRD, and field type is Short Integer
* Validate contains field ELEM_, and field type is Short Integer
* Validate contains field MID_, and field type is Short Integer
* Validate contains field INT_, and field type is Short Integer
* Validate contains field HIGH_, and field type is Short Integer
* Validate contains field CAPACITY, and field type is Short Integer
* Validate contains field PERM_CLRM, and field type is Short Integer (warning only)
* Validate contains field PORT_CLRM, and field type is Short Integer (warning only)
* Check fields NAME, SCHL_CODE, STRT_GRD, END_GRD, ELEM_, MID_, INT_, HIGH_, CAPACITY, PERM_CLRM, and PORT_CLRM
  * Validate no null records in each of these fields
  * Validate no special characters
* Check field SCHL_CODE
  * Validate no duplicate values
  * SCHL_CODE must = ELEM_, MID_, INT_, or HIGH_
  * SCHL_CODE field must have unique values, unless SCHL_CODE = 0

* Check fields NAME, ELEM_, MID_, INT_, and HIGH_
  * Validate no duplicate values in each field
* Check field STRT_GRD
  * Check that value is not < -1
* Check field END_GRD
  * Check that value is not > 12
* Check field CAPACITY
  * Validate value > 0 (warning only)

## Students
* Validate contains field GRD, and field type is Short Integer

* Validate contains field SCHL_CODE, and field type is Short Integer

* Validate contains field STUTYPE, field type is Text, and length is 2

* Check fields GRD, SCHL_CODE, and STUTYPE
  * Validate no null records in each of these fields
* Check field STUTYPE
  * STUTYPE must contain a valid Davis Demographics defined code (See "Creating Students" for more information about valid Davis Demographics student type codes.)

* Check field SCHL_CODE
  * Student cannot have 9999 in the SCHL_CODE field
  * Students cannot be coded to school code 0. For example, a student cannot have SCHL_CODE = 0.

* Validate all students with GRD = -1 have STUTYPE = 'PK' or STUTYPE = 'TK'

* Validate all students with STUTYPE = 'PK' or STUTYPE = 'TK' have GRD = -1

* Check ALL eligible "Other Attribute fields" *
  * Validate fields don't have double field type
  * Validate no special characters in fields

 

*Eligible “Other Attributes” fields are fields in the Student feature class that can be used to display “Other Attributes” in the statistic window, such as Ethnicity, Program, School of Attendance, etc…  A field is eligible if it meets the following criteria:

* Has less than 100 unique values

* Is defined as a Text or an Integer field

* Has no special characters

* Does not have the field names: “ADDRESS”, “STUNUM”, “STATUS”, “SCORE”, “MATCH_TYPE”, “SIDE”, “STREET”, “LNAME”, “FNAME”, “LAST_NAME”, “FIRST_NAME”, “STUNAME”, “STUTYPE”, “GRD”, “GRADE”, “LOC_NAME” and any field name that contains “ADDR” or “ARC_”.

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

## Students vs. Study Areas
* Check STUTYPE to see if any RS students live out of district
  * If, spatially, a student lives outside the study areas boundaries but is labeled 'RS', then auto-correct to 'OD' student type

## Students vs. Schools
* Check Students field SCHL_CODE vs. Schools field SCHL_CODE
  * For each value in the Students field SCHL_CODE there needs to be one record in Schools that contains the same value in SCHL_CODE.

* Check Students are within their school's grade range

 
