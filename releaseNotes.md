### Build 1.8.7 Oct 1st Q1 release
#### New Automated Attendance Matrix feature
*  Create an attendance matrix using GE "General Education" students by defining the grade ranges for each of the grade levels present in the study area data.

#### Data enrichment tool upgrade
* This tool will now enrich both current study areas as well as now plans so you can attach forecasted student counts to proposed attendance boundaries from plans you create.

#### Misc changes
* Imported historical student data is now enriched (just like current year student data already was) with three additional fields of data: school name of residence, school code of residence, and school name of enrollment
* New data validation rule that will check to determine grades served district wide (that make up the attendance boundaries) and make sure all students are in grades served by those schools
* Minor UI updates, tooltips, etc.

### Build 1.8.6
#### New Program Re-assignment feature
* Import programs (special ed, music, dual language, etc. Each program has a number of reserved classroom seats)
* Add new programs/delete programs
* Reassign programs from one school to another
* Stats window now shows a modified capacity column that reduces the overall capacity based on the number of seats of programs assigned to that school

#### New data validation rules
* Detect if a study area is assigned to schools that create gaps in grade range coverage
* Detect if a student is enrolled in a school that does not serve their grade (8th grader enrolled in a 9-12 school)
* Detect if a school serves a grade that has no students enrolled (school serves K-6 but only has K-5 enrolled)

#### Misc changes
* Several improvments and bugs addressed for plans with enrollment
* Minor UI updates, tooltips, etc.

  
### Build 1.8.5 Pre-Fall revisions
* Bug fixes to plans with enrollment
* Student enrichment to imported data and original source to add fields defining school of enrollment and school of residence
* More help information
* New background on load
* New 'Copy' button for plans/forecasts
* Changes to capacity can be saved back to imported schools for future plans
* Updates to rendering a forecast to alter alias of DISPLAY for Map Contents window
* Bypass warning message option enabled
* New schools in a plan automatically becomes target school for assignment

### Build 1.8.4 Pre-Fall upgrades (March 2025)
* Updates and bug fixes to plans with enrollment
* Read-only mode for forecasts to lock in factors
* Forecast appearance labeled to describe current settings
* New and updated help and tooltip icons and information
* Address directory upgrades for more compatibility across different Student Information Systems
* Reset Project tool now offers just to reset address directory information instead of all data

### Build 1.8.3 Plans with enrollment (April 2025 - internal only release for testing)
* First release that will create plans showing both residence and enrollment counts
* Minor UI updates and improvements
* Fixed issue when closing SchoolSite Pro from start page which caused it the hang requiring a force close
* New buttons to show plan/forecast comments to review how they were setup/configured
* Update help icons for better, more consistent look across tools

Additional changes:
* Excel reports prompt the user to open them after export, which auto launches Excel and opens the report

### Build 1.8.2 Address Directory updates (March 2025)
* Updated address directory output to include: MID_, prefix direction, prefix type, suffix direction
  
### Build 1.8.1 Street/Address Directory release (February 2025)
* Updated error checking to prevent issues in various tools by limiting special characters used in plan and forecast names
* Updated tooltips and help links with more to come across the application
* Updates, UI tweaks, and bug fixes to Street/Address Directories based on feedback from the beta released at 1.8.0
  
### Build 1.8.0 - Internal only release (February 2025)
* Beta release of street/address directory tools for internal testing
* MGT branding updates
* New help button and contextual help icons to help users navigate to https://ssphelp.mgt.us/
* Various UI updates, alignments, layout improvements especially on the Start Page
* Enrollment forecast Excel formatting updates for better consistency

### Build 1.7.9 - August release (August 2024)
* Fixed bug introduced with ArcGIS Pro 3.3 when using Plan Impact Summary report

### Build 1.7.8 - August release (August 2024)
* Fixed bug when copying a forecast
* Updated format for enrollment forecasts and Excel export to be more consistent with residence forecasts and align with template guidelines

### Build 1.7.7 - ArcGIS Pro 3.3+ only (July 2024)
* Fixed additional bugs related to limited field names in ArcGIS Pro 3.3 causing exporting reports/tables to Excel to fail such as the statistics window and causing importing of historical student to fail when calulating mobility
* Added ability to import street data in preparation for street directory tool

### Build 1.7.6 - ArcGIS Pro 3.3+ only (July 2024)
* Minor UI updates
* Data Enrichment Tools released to enrich tract data with estimated number of students based on units and SYF. Also creates enriched study area data with numbers of forecasted students in each area.
* Reset Project bug fixed that lead to missing TYPE2 units being imported
* Added Capacity for each school in forecast report when reporting on attendance areas and formatted for output in Excel

#### Build 1.7.5 (Nov 2023)
* Fixed problem when importing historical students

#### Build 1.7.4 (Nov 2023)
* This build fixes an issue preventing the assignment of study areas to the target school in plans that have been copied and/or renamed.

#### Build 1.7.3 (Nov 2023)
* Bugs fixed for labeling in plans
* Bugs fixed for symbolizing a forecast
* Bugs fixed for showing the data about the selected study areas in a plan when boundary planning
* Bugs fixed for changing which grade ranges are shown in the statistics table
* Bugs fixed for error messages that are shown when a forecast was first created

#### Build 1.7.2 (Oct 2023)
* Student yield factors have been expanded from just PK, K-6, 7-8, 9-12 to PK through 12 with all individual grades.
* New sorting of enrollment forecasts allows straight alphabetical sorting instead of grouping elementary first followed by middle and high and then listed alphabetically in those groups.
* Fixed bugs when using Remove Unassigned Schools and Plan Summary

#### Build 1.7.1 (Aug 2023)
* New feature: Reset Geodatabase allows the user to delete all imported data and maps that have plans or forecasts to start over with new data in the same project
* Plan statistics and forecast reports no longer have pre-defined grade ranges of K-6,7-8,9-12. It only has a grade range textbox for easier entry
* Layers that have definition expressions are flagged during Data Setup as warnings to alert the user
* Changed all references of Maturation to Buildout
* In Forecasts, under Appearance, you are now able to symbolize resident student change to have its end year as Buildout.
* Bug fixes related to data setup for historical students
* Bug fixes for when enrollment forecast would indicate changes were made to resident forecast when they had not been forcing an unneeded recalculation of the enrollment forecast
* Bug fixes when exporting mobility reports.

#### Build 1.7.0 (Feb 2023)
* Updated start page for improved ability to find previous Projects
* Fixed bugs found when working with specific datasets related to features such as:
* Exporting plans
* Warning when the license is about to expire
* Enrollment forecasts
* Reassign by current boundaries
* Improved rounding to avoid really long decimal values
* Plan Summary report
* Forecast report setup was missing grade ranges on occasion

#### Build 1.6.9 (Dec 2022)
* Fixed bugs when making a forecast

#### Build 1.6.8 (Dec 2022)
* Fixed bugs preventing the successful export of forecast reports to both text and Excel formats
* Improved the rounding of values in the plan stats window so they would not exceed two decimal points
* Updated the messaging around enrollment forecasts to make sure the report indicates that it needs to be refreshed after changes are made to residential forecast values. This message would previously disappear too soon. 
* Enrollment forecasts now show a warning when it detects that a school has had a significant gap in enrollment from year to year to indicate that the resulting forecasted values could be negatively impacted.
* When sorting the forecast enrollment report by grade to show elementary first, then middle, followed by high....it now considers PK and K to be the same value for sorting purposes so you don't get PK-6 followed by K-6. Those are both considered 'elementary' and are in the same grouping in the report.
* Better handling of ‘custom’ grade ranges in plan statistics and forecast report setup. Custom ranges no longer accepts grade ranges that are already available via checkbox (i.e. K-6 is not ‘custom’, just select it from the set of pre-defined grade ranges. Use ‘custom’ for things like K-4 or 6-8.

#### Build 1.6.7 (Dec 2022)
* Schools are ordered in the report first by grade, then by name so the elementary schools are grouped alphabetically followed by middle schools, etc…
* Messages when schools are excluded from reports are re-worded to make more sense as to why they could not be forecasted
* Added total enrollment summary line to the top of the report

#### Build 1.6.6 (Nov 2022)
* Various enhancements to formatting of reports both on screen and when exported to Excel
* Bug fix for staffing forecast when calculating the students transferring out of the PK grade in boundary schools
* Fixed bug in the Project Summary report that caused it to not find the required DEVELOPER field
* Fixed issue where maturation units were not included in a development summary excel report in cases where a studyarea had zero development in years one thru ten but then had development beyond that.
* Updated Student Report to summarize an accounting of student data to give insight into what students were in the file, which were in district, and which were used in the plan or forecast broken down by STUTYPE and GRD

Build 1.6.5 (Oct 2022)
* Built for ArcGIS Pro 3.0
* First release out of beta
