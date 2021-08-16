# Data Checks Made for Locator

Below is a list of the data checks that SchoolSite makes when using the Data Validator for SchoolSite Locator.

## Step 1: Validate individual feature classes
There are two required datasets that are required for SchoolSite Locator:

1. Study Areas
2. Schools
 

Additionally, there is one optional dataset that you may want to include:

1. Trustee Areas

## Study Areas
* Validate contains field STDYAREA,  field is type Text, and maximum length is 6
* Validate contains field ELEM_, and field type is Short Integer
* Validate contains field MID_, and field type is Short Integer
* Validate contains field INT_, and field type is Short Integer
* Validate contains field HIGH_, and field type is Short Integer
* Validate contains field DISTRICT, field type is Text, and maximum length is 50
* Validate contains field MOBILITY, field type is Text, and maximum length is 3
* Validate contains field ELEM_DESC and field is type Text, and maximum length is 50
* Validate contains field MID_DESC and field is type Text, and maximum length is 50
* Validate contains field INT_DESC and field is type Text, and maximum length is 50
* Validate contains field HIGH_DESC and field is type Text, and maximum length is 50
* Validate contains field REGION1 and field is type Text, and maximum length is 50
* Validate contains field REGION2 and  field is type Text, and maximum length is 50
* Validate contains field TRUSTEE, and field type is Short Integer
* Validate contains field ADD_SCHL1, and field type is Short Integer
* Validate contains field ADD_SCHL2, and field type is Short Integer
* Validate contains field ADD_SCHL3, and field type is Short Integer
* Validate contains field ADD_SCHL4, and field type is Short Integer
* Validate contains field ADD_SCHL5, and field type is Short Integer
* Check fields STDYAREA, ELEM_, MID_, INT_, HIGH_, DISTRICT, MOBILITY, ELEM_DESC, MID_DESC, INT_DESC, HIGH_DESC, REGION1, REGION2, TRUSTEE, ADD_SCHL1, ADD_SCHL2, ADD_SCHL3, ADD_SCHL4, and ADD_SCHL5
  * Validate no null values in these fields
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
* Validate contains field GRD_RANGE, and field type is Text
* Validate contains field ELEM_, and field type is Short Integer
* Validate contains field MID_, and field type is Short Integer
* Validate contains field INT_, and field type is Short Integer
* Validate contains field HIGH_, and field type is Short Integer
* Validate contains field CAPACITY, and field type is Short Integer
* Validate contains field PERM_CLRM, and field type is Short Integer (warning only)
* Validate contains field PORT_CLRM, and field type is Short Integer (warning only)
* Validate contains field ADDRESS,  field type is Text, and maximum length is 100
* Validate contains field CITY,  field type is Text, and maximum length is 50
* Validate contains field ZIP, and field type is Long Integer
* Validate contains field PHONE,  field type is Text, and maximum length is 12
* Validate contains field WEBSITE,  field type is Text, and maximum length is 150
* Validate contains field NOTES,  field type is Text, and maximum length is 150
* Validate contains field SCHL_TYPE and field type is Text
* Validate contains field SCHL_STATUS and field type is Text
* Check fields NAME, SCHL_CODE, ELEM_, MID_, INT_, HIGH_, CAPACITY, PERM_CLRM, PORT_CLRM, STRT_GRD, END_GRD, and GRD_RANGE
  * Validate no NULL values in these fields
* Check field NAME
  * Validate no record has special characters
* Check field SCHL_CODE
  * Validate no duplicate values
  * SCHL_CODE must = ELEM_, MID_, INT_, or HIGH_
* Check fields NAME, ELEM_, MID_, INT_, and HIGH_
  * Validate no duplicate values in each field
* Check field CAPACITY
  * Validate value > 0 (warning only)

 
