Build 1.7.4 (Nov 2023)
* This build fixes an issue preventing the assignment of study areas to the target school in plans that have been copied and/or renamed.

Build 1.7.3 (Nov 2023)
Bugs fixed include issues with:
* labeling in plans
* symbolizing a forecast
* showing the data about the selected study areas in a plan when boundary planning
* changing which grade ranges are shown in the statistics table
* error messages that are shown when a forecast was first created

Build 1.7.2 (Oct 2023)
* Student yield factors have been expanded from just PK, K-6, 7-8, 9-12 to PK through 12 with all individual grades.
* New sorting of enrollment forecasts allows straight alphabetical sorting instead of grouping elementary first followed by middle and high and then listed alphabetically in those groups.
* Fixed bugs when using Remove Unassigned Schools and Plan Summary

Build 1.7.1 (Aug 2023)
* New feature: Reset Geodatabase allows the user to delete all imported data and maps that have plans or forecasts to start over with new data in the same project
* Plan statistics and forecast reports no longer have pre-defined grade ranges of K-6,7-8,9-12. It only has a grade range textbox for easier entry
* Layers that have definition expressions are flagged during Data Setup as warnings to alert the user
* Changed all references of Maturation to Buildout
* In Forecasts, under Appearance, you are now able to symbolize resident student change to have its end year as Buildout.
* Bug fixes related to data setup for historical students
* Bug fixes for when enrollment forecast would indicate changes were made to resident forecast when they had not been forcing an unneeded recalculation of the enrollment forecast
* Bug fixes when exporting mobility reports.

Build 1.7.0 (Feb 2023)
* Updated start page for improved ability to find previous Projects
* Fixed bugs found when working with specific datasets related to features such as:
* Exporting plans
* Warning when the license is about to expire
* Enrollment forecasts
* Reassign by current boundaries
* Improved rounding to avoid really long decimal values
* Plan Summary report
* Forecast report setup was missing grade ranges on occasion

Build 1.6.9 (Dec 2022)
* Fixed bugs when making a forecast

Build 1.6.8 (Dec 2022)
* Fixed bugs preventing the successful export of forecast reports to both text and Excel formats
* Improved the rounding of values in the plan stats window so they would not exceed two decimal points
* Updated the messaging around enrollment forecasts to make sure the report indicates that it needs to be refreshed after changes are made to residential forecast values. This message would previously disappear too soon. 
* Enrollment forecasts now show a warning when it detects that a school has had a significant gap in enrollment from year to year to indicate that the resulting forecasted values could be negatively impacted.
* When sorting the forecast enrollment report by grade to show elementary first, then middle, followed by high....it now considers PK and K to be the same value for sorting purposes so you don't get PK-6 followed by K-6. Those are both considered 'elementary' and are in the same grouping in the report.
* Better handling of ‘custom’ grade ranges in plan statistics and forecast report setup. Custom ranges no longer accepts grade ranges that are already available via checkbox (i.e. K-6 is not ‘custom’, just select it from the set of pre-defined grade ranges. Use ‘custom’ for things like K-4 or 6-8.

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
