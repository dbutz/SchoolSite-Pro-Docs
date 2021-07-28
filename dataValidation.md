# Installation
## test
This documentation is intended for the software developers of Davis Demographics. This is to help you associate SchoolSite functionalities with their associated code.

The following checks need to be made and passed by the Data Validation tool in order to be recognized as a Students feature class. Their associated functions are written in each description also:

**1. A schools feature class must have the following required fields:**

* NAME - The name of the school.
* SCHL_CODE - The school's associated and unique school code.
* STRT_GRD - The earliest grade the school serves.
* END_GRD - The latest grade the school serves.
* ELEM_ - This field should contain the same value found in SCHL_CODE if the school is an elementary school. 
* MID_ - This field should contain the same value found in SCHL_CODE if the school is a middle school. 
* INT_ - This field should contain the same value found in SCHL_CODE if the school is an intermediate school. 
* HIGH_ - This field should contain the same value found in SCHL_CODE if the school is a high school. 
* CAPACITY - The suggested maximum number of students that can attend this school.
* PERM_CLRM - The number of permanent classrooms at the school. (Warning)
* PORT_CLRM - The number of portable classrooms at the school. (Warning)

`CheckIfFeatClassContainsRequiredFieldAsync()`

**2. Each of the required fields must be the correct field type. Since NAME is a text field, then it must also have the correct length:**

* NAME - Text, length 50
* SCHL_CODE - Integer
* STRT_GRD - Integer
* END_GRD - Integer
* ELEM_ - Integer
* MID_ - Integer
* INT_ - Integer
* HIGH_ - Integer
* CAPACITY - Integer
* PERM_CLRM - Integer
* PORT_CLRM - Integer

`CheckIfCorrectFieldTypesAsync()` 
`CheckIfTextFieldsAreCorrectLengthsAsync()`

**3. There should be no null values under each of the required fields.**

`CheckIfFieldDoesNotHaveNullValuesAsync()`

**4. There should be no special characters in any value under the NAME field.** (Please see topic on special characters.)

`CheckIfFieldDoesNotHaveSpecialCharactersAsync()`

**5. Values under field NAME must be unique.**

`CheckNoDuplicateValuesAsync()`

**6. Values under field SCHL_CODE, ELEM_, MID_, INT_, and HIGH_ must be unique, unless a value is 0.**

`CheckNoDuplicateValuesExceptZeroAsync()`

**7. Values in ELEM_, MID_, INT_, and HIGH_ must be either 0, or match the value under SCHL_CODE.**

`CheckMatchingSchoolCodesInSchoolFeatClassAsync()`

**8. Values under field STRT_GRD and END_GRD must be within values -1 and 12.**

`CheckIfGradeRangesAreWithinPK12Async()`

**9. Values under the field CAPACITY must be greater than 0.** (Warning)

`CheckIfValuesAreGreaterThanZeroAsync()`
