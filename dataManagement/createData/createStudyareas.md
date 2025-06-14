# Creating Study Areas
## Study Areas - a polygon feature class
Study Areas are the building blocks of a school district. Study areas grouped together (and coded to specific school ID numbers) form attendance boundaries. Study Areas are geographically defined, following logical boundaries of a neighborhood, and are used for boundary planning and generating small area enrollment forecasts. SchoolSite Pro does not use separate feature classes for each set of school attendance areas.  Using a unique field coding method, all attendance areas are stored within the Study Area feature class attribute table.

## Source:
Districts with established Study Areas need to map and enter the information into a geodatabase feature class or a shapefile. If your district does not have existing Study Areas, create a Study Area feature class or shapefile based on the criteria described in the next topic, ["What Are Study Areas?"](../../faq/studyAreas.md). Once the district is divided into Study Areas, populate the attribute table. This involves coding each Study Area to an elementary, middle,  intermediate and high school of assignment.

## Required Fields:
1. **STDYAREA** - A field containing the unique number of the study area, defined as data type "Text" with a length of 6. No duplicate values and no special characters.

1. **ELEM_** - A field containing the Elementary School number the study area is assigned to, defined as data type "Short Integer" or "Long Integer". If one record has ELEM_ > 0, then all records must have ELEM_ > 0

1. **MID_** - A field containing the number of the Middle School number the study area is assigned to, defined as data type "Short Integer" or "Long Integer". If one record has MID_ > 0, then all records must have MID_ > 0
1. **INT_** - A field containing the number of the Intermediate School number the study area is assigned to, defined as data type "Short Integer" or "Long Integer". If one record has INT_ > 0, then all records must have INT_ > 0

1. **HIGH_** - A field containing the High School number the study area is assigned to, defined as data type "Short Integer" or "Long Integer". If one record has HIGH_ > 0, then all records must have HIGH_ > 0

1. **DISTRICT** - A field containing a six-letter code used to report and summarize portions of the District, defined as data type "Text".  Examples are: Elementary district code for a Union High School district, School Board or Trustee area or any other values for which you wish to summarize projections by area. The DISTRICT field should be defined as data type "Text" with a maximum length of 50.

1. **MOBILITY** - A field containing a 1-letter code used to indicate the Study Areas inclusion in the Mobility calculation.  A value of 'Y' indicates that the study area should be included in the Mobility calculation and a value of 'N' indicates that study area should NOT be included in the Mobility calculations.  The MOBILITY field should be defined as data type "Text" with a length of 1.

 **Please note:** If a record has 9999 in one of these fields (ELEM_, MID_, INT_, and HIGH_) then all of these fields must be 9999 for that record.

## Coding Study Areas:
Any area that is created must be coded.  If you have a polygon within the district that is not assigned to any school, such as an area for a lake, you need to code the ELEM_, MID_, INT_, and HIGH_ fields with the number 9999.  This will avoid receiving an error for an un-coded polygon as the software will recognize it as a properly unassigned polygon.  

## Additional Fields:
The following fields are **required for SchoolSite Locator** , but **not required for redistricting plans and forecasts.**

 

8. **REGION1**  - A field containing the name of a region the study area is assigned to that a user would like to be able to report on, i.e. Board Trustee Areas, Transportation Service Areas, Zip Code, etc. The REGION1 field should be defined as data type "Text" with a length of 50.

9. **REGION2**  - A field containing the name of a second region the study area is assigned to that a user would like to be able to report on, i.e. Board Trustee Areas, Transportation Service Areas, Zip Code,  etc. The REGION2 field should be defined as data type "Text" with a length of 50.

10. **ELEM_DESC** - A field containing the name of the Elementary School that the study area is assigned to. The ELEM_DESC field should be defined as data type "Text" with a length of 50.

11. **MID_DESC**  - A field containing the name of the Middle School that the study area is assigned to. The MID_DESC field should be defined as data type "Text" with a length of 50.

12. **INT_DESC**  - A field containing the name of the Intermediate School that the study area is assigned to. The INT_DESC field should be defined as data type "Text" with a length of 50.

13. **HIGH_DESC**  - A field containing the name of the High School that the study area is assigned to. The HIGH_DESC field should be defined as data type "Text" with a length of 50.

14. **TRUSTEE** - A field containing the Trustee area the Study Area is in. The TRUSTEE field should be defined as a "Short Integer" or "Long Integer".

The following fields are **required for SchoolSite Pro Locator**, but are only used for Study Areas that are in split attendance areas or optional areas.  

 

15. **ADD_SCHL1** - "Short Integer" or "Long Integer" and not null

16. **ADD_SCHL2** - "Short Integer" or "Long Integer" and not null

17. **ADD_SCHL3** - "Short Integer" or "Long Integer" and not null

18. **ADD_SCHL4** - "Short Integer" or "Long Integer" and not null

19. **ADD_SCHL5** - "Short Integer" or "Long Integer" and not null
