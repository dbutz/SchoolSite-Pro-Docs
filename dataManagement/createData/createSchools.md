# Creating Schools

## Schools - a point feature class
## Source:
The District is the only source for this information.

## Required Fields:
**Important: The school code numbers in the ELEM_, MID_, INT_, and HIGH_ fields below have to match the school codes entered into the corresponding fields in the study areas.**

 

1. **NAME** - A field containing the unique name of the school, defined as data type "Text" with a length of 50. Each school name should be unique. For example, if you have a Main Street Elementary and Main Street High, do not enter "Main Street" for both schools.

2. **SCHL_CODE** - A field containing the school code of each school, must match codes used to populate the ELEM_, MID_, INT_, and HIGH_ fields defined as data type "Short Integer".

3. **CAPACITY** - A field containing the maximum capacity of the school, defined as data type "Short Integer".

4. **STRT_GRD** - A field containing the start grade served at the school, defined as data type "Short Integer".

5. **END_GRD** - A field containing the end grade served at the school, defined as data type "Short Integer".

## Additional Fields:
The following fields are **required only for SchoolSite Locator, but are not required for redistricting plans or projections.**

 

12. **GRD_RANGE** - A field containing the grade range of the school, defined as data type "Text".

13. **ADDRESS** - The street address of the school, defined as type "Text" with a length of 100.

14. **CITY** - The city of address of the school, defined as type "Text" with a length of 50.

15. **ZIP** - The zip code of the school, defined as type "Long Integer".

16. **PHONE** - The phone number of the school, defined as type "Text" with a length of 12.

17. **WEBSITE** - The web address of the school, defined as type "Text" with a length of 150 and must have prefix http://

18. **NOTES** - Any additional notes, defined as type "Text" with a length of 150.

19. **SCHL_TYPE** - School Type, defined as type "Text"
* Suggested School Type Codes:
  * ES - Elementary School
  * MS - Middle School
  * IS - Intermediate School
  * JHS - Junior High School
  * HS - High School
  * K8 - K-8 School
  * 712 - 1-12 School
  * OTH - Other School

20. **SCHL_STATUS** - School Status, defined as type "Text"
* Suggested School Status Codes:
  * DIST - District Office
  * SPED - Special Education
  * MAGN - Magnet
  * ACDY - Academy
  * CONT - Continuation
  * ALTN - Alternate
  * RGLR - Regular
  * FUTR - Future
  * CLSD - Closer
  * OTHR - Other

## Points to Remember:
* Individual school codes must be unique

* For elementary schools, the ELEM_ field would be filled in with an ID value while the MID_, INT_ and HIGH_ fields will usually contain 0.

* For middle or junior high schools, ELEM_ and HIGH_ will be 0 and the INT or MID_ field contain the schools id number (i.e. will have a value other than 0).  The same general rule applies if you are working with a high school

* In the cases of K-8 schools where a site might house what is normally considered both elementary and intermediate school students, the ELEM_ and INT_ fields would have the same ID number and HIGH_ would be 0. See the highlighted row below for an example:

