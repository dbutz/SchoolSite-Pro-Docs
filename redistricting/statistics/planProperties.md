# Plan Properties: Statistics Tab

The Plan Properties Statistics Tab allows you to analyze your boundary scenarios based on various student attributes such as grade, ethnicity, loading standards and projected student residence.

 

The statistics you choose in this window will be displayed in the plan report and in the statistics window.

 

To access the Statistics tab of the Plan Properties dialog box from the Redistricting Toolbar:

 

Choose Redistricting > Plan Properties > Statistics

![currentResidence](statImages/currentResidnce.png)

The Statistics Tab window is divided into four main sections: Select Schools, Select Grades, Select Grade Ranges, and Select Statistic Type.  

Select Schools
From the list, choose which schools to display statistics for by checking the box next to each school name.  To select all school names, click Select All.  To unselect all school names, click on Select None. These checked schools only affect the schools displayed in the resident tabs of the statistics window. If a plan is created based upon "Current Resident Students and Current Enrollment" the Estimated Enrollment tab will always display all schools including those without attendance boundaries. . 

Select Grades and Grades Ranges
Selecting grades only applies to the grades you wish to display in the Residence Tab of the statistics window. Residence  redistricting can theoretically encompass any grades or grade ranges you desire during the boundary planning process since residency is not concerned with the school of attendance. You can specify any number of grades or grade ranges you wish as you make resident boundary changes. If a plan is created based upon "Current Resident Students and Current Enrollment" the Estimated Enrollment tab will always display all grades for each school. 

 

Select one of the predefined grade ranges by clicking on the boxes or click on custom to create your own grade range to report on. Examples of custom grade ranges would include "K-5, 6-8" or "K-8".

Statistics Types
This section allows you to report the number of students in each of the selected schools based on various attributes.  The Grade Distribution option (default option) reports the number of students in each grade selected. Statistic types only display in the resident tabs of the statistics window. The Estimated Enrollment tab only displays individual grades and grade ranges.

 

Grade Distribution
This will allow you to select the individual grades and grade ranges (in the Select Grades section) to display in the statistics window.

Capacity
This is taken from the "CAPACITY" field in your Schools dataset.  It displays the current capacity for each school.

% Capacity
This reflects the percentage of capacity compared to summarized grade ranges.

Other Student Attribute
By default, the grade field is always summarized, but you can summarize on any field that you have in your student data such as ethnicity, school of enrollment, gender, ESL etc.).  Click on Other Student Attribute and select a field from your student data you want to summarize from the drop-down menu. Caution, though, should be taken.  You should not summarize on a field that has a lot of unique values, such as student ID.  If you have a fairly large size student data set it will take a very long time for it to summarize and the resulting report will not produce much usable information.  Fields such as ethnic and special education will give you valuable information and will take a minimal time to summarize.  You can deselect any additional attributes you may have selected by clicking on the grade distribution button again.  

Please Note: This section will be grayed out if the plan is based upon projected student data.

Show grades/Show ranges/Display percentage
These three options give you the option of how you want to summarize the "other student attributes". The statistics window will show the number of students by grade by the selected attribute or totaled by grade range or as a percent of that school's total population.

Please Note: This section will be grayed out if the plan is based upon projected student data.

Other Information
Forecast Year
If you created your plan based on forecast data, you can select the pull down menu in the Statistics tab, and select any year of the forecast to report (including maturation) to view it in the Statistics Window.  This is useful for creating one future boundary plan and quickly viewing the forecasted number of students for this plan in various future years.

![forecastPlan](../createPlan/planImages/forecastPlan.md)

When you select a specific projected year in the Statistics tab of Plan Properties, the Statistics Window will display the year of projection that you selected.

**Please note:** If your Plan Properties has no grade ranges specified, then the Projection Summary Report will display either PK-12 or K-12 by default, depending on whether or not you chose to include PK students during plan creation.
