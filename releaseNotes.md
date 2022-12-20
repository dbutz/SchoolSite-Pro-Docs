Build 1.6.8 (Dec 2022)
* Fixed bugs preventing the successful export of forecast reports to both text and Excel formats
* Improved the rounding of values in the plan stats window so they would not exceed two decimal points
* Updated the messaging around enrollment forecasts to make sure the report indicates that it needs to be refreshed after changes are made to residential forecast values. This message would previously disappear too soon. 
* Enrollment forecasts now show a warning when it detects that a school has had a significant gap in enrollment from year to year to indicate that the resulting forecasted values could be negatively impacted.
* When sorting the forecast enrollment report by grade to show elementary first, then middle, followed by high....it now considers PK and K to be the same value for sorting purposes so you don't get PK-6 followed by K-6. Those are both considered 'elementary' and are in the same grouping in the report.

Build 1.6.7 (Dec 2022)
* Schools are ordered in the report first by grade, then by name so the elementary schools are grouped alphabetically followed by middle schools, etc…
* Messages when schools are excluded from reports are re-worded to make more sense as to why they could not be forecasted
* Added total enrollment summary line to the top of the report

Build 1.6.6 (Nov 2022)
* Various enhancements to formatting of reports both on screen and when exported to Excel
* Bug fix for staffing forecast when calculating the students transferring out of the PK grade in boundary schools
* Fixed bug in the Project Summary report that caused it to not find the required DEVELOPER field
* Fixed issue where maturation units were not included in a development summary excel report in cases where a studyarea had zero development in years one thru ten but then had development beyond that.
* Updated Student Report to summarize an accounting of student data to give insight into what students were in the file, which were in district, and which were used in the plan or forecast broken down by STUTYPE and GRD

Build 1.6.5 (Oct 2022)
* Built for ArcGIS Pro 3.0
* First release out of beta
