# The Statistics Window

The Statistics Window is a powerful tool that can help you generate reports about your district and view the changes that you’ve made during redistricting. 

## Configure the statistics table

The Statistics Window allows you to analyze your boundary scenarios based on various student attributes such as grade, ethnicity, loading standards, and projected student residence. 

The settings you choose will be displayed in the statistics table.

To access the Statistics Window, go to the redistricting ribbon and click Statistics Window.

![image](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/46aae42f-ab78-4470-b6e1-c8b076d87266)


The Statistics Tab window is divided into four main sections: Select Schools, Select Grades, Select Grade Ranges, and Select Statistic Type.  

## Select Schools

From the list, choose which schools to display statistics for by checking the box next to each school name.  To select all school names, click Select All.  To unselect all school names, click on Select None. These checked schools only affect the schools displayed in the resident tabs of the statistics window. If a plan is created based upon "Current Resident Students and Current Enrollment" the Estimated Enrollment tab will always display all schools including those without attendance boundaries.

## Select Grades and Grades Ranges

Selecting grades only applies to the grades you wish to display in the Residence Tab of the statistics window. Residence  redistricting can theoretically encompass any grades or grade ranges you desire during the boundary planning process since residency is not concerned with the school of attendance. You can specify any number of grades or grade ranges you wish as you make resident boundary changes. If a plan is created based upon "Current Resident Students and Current Enrollment" the Estimated Enrollment tab will always display all grades for each school. 

Enter the grade ranges you wish to see summarized. Examples of grade ranges would include "K-5, 6-8" or "K-8".

## Statistics Types
This section allows you to report the number of students in each of the selected schools based on various attributes.  The Grade Distribution option (default option) reports the number of students in each grade selected. Statistic types only display in the resident tabs of the statistics window. The Estimated Enrollment tab only displays individual grades and grade ranges.

* __Grade Distribution__
This will allow you to select the individual grades and grade ranges (in the Select Grades section) to display in the statistics window.

* __Capacity__
This is taken from the "CAPACITY" field in your Schools dataset.  It displays the current capacity for each school.

* __% Capacity__
This reflects the percentage of capacity compared to summarized grade ranges.

* __Student Attribute__
By default, the grade field is always summarized, but you can summarize any field that you have in your student data such as ethnicity, school of enrollment, gender, ESL, etc.).  Click on Other Student Attribute and select a field from the student data you want to summarize from the drop-down menu. Caution, though, should be taken.  You should not summarize a field that has a lot of unique values, such as student ID. __Currently, the limit to the maximum number of unique values allowed in a field to summarize is 150.__  If you have a fairly large size student data set it will take a very long time for it to summarize and the resulting report will not produce much usable information.  Fields such as ethnic and special education will give you valuable information and will take minimal time to summarize.  You can deselect any additional attributes you may have selected by clicking on the grade distribution button again.
__Please Note:__ This section will be grayed out if the plan is based on forecasted student data.


 * __Show grades/Show ranges/Display percentage__
   These three options give you the option of how you want to summarize the "other student attributes". The statistics window    will show the number of students by grade by the selected attribute or totaled by grade range or as a percent of that school's total population.
   __Please Note:__ This section will be unavailable if the plan is based upon forecasted student data.

## Other Information

### Forecast Year

If you created your plan based on forecast data, you can select the pull-down menu in the Statistics tab, and select any year of the forecast to report (including maturation) to view it in the Statistics Window.  This is useful for creating one future boundary plan and quickly viewing the forecasted number of students for this plan in various future years.

![image](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/d6a3c5d4-78c9-4aa4-b5cc-02b0b6be37f5)

**Please note:** If your Statistics Window has no grade ranges specified, then the Projection Summary Report will display either PK-12 or K-12 by default, depending on whether or not you chose to include PK students during plan creation.
