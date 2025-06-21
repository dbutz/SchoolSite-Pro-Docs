# Calculating Projected Housing Units
Closely related to Student Yield Factors are projected housing units.  Projected housing development data along with student yield factors (SYFs) are used to estimate (add in) the number of students generated from new housing developments.

 

**Housing information entered in the tract dataset can be automatically entered into the Projection Properties table if specified in the Create Projection Wizard.**

 

### See Also:
Creating Tracts

## Entering Projected Housing Units
1. Click on the drop down menu for Modify Factors in the Forecasting ribbon.
2. Choose Projected Housing Units
3. This Projected Hosuing Units Pane is automatically populated if you choose to include a tract layer as part of the projection.  From this form you can alter the housing counts for each year of the projection by study area if necessary.  For each study area there are 12 years or records.  

Year 0 represents existing housing units and is automatically filled in if you specified an assessor file in the initial projection wizard.  Year 0 is only necessary or used if you are creating maturation forecasts.  

Records for years 1 through 10 are filled in from your tract dataset (if you specified a tract dataset in the Create Projection Wizard).  Year 11 is referred to as “after units”; it has no specific time frame.  It is actually an accumulation of units from all phases whose completion dates are scheduled after the 10 year projection time frame.  In addition, if you are running maturation projections, you may want to enter additional future housing into this table which represent potential housing units on vacant land that is not currently under a subdivision map or in the planning process.  These future units would be added onto those in year 11.

Year 12 is the total of years 0 – 11 and is automatically calculated as you make changes to years 0 through 11.  You cannot click directly in year 12 and change it.  It will always mirror the total of years 0 – 11.  Year 12 is only used in maturation calculations.  It represents the summary of all current, projected, and potential housing units that could occur in each study area if all the land is developed/built out. (For a discussion of how to calculate future housing for maturation, please see topic Maturation Factors.)

## Modify Projected Housing Unit Numbers
If you need to modify the number you can edit each value directly in its cell on the Projected Housing Units table. You can do this by double clicking the value you want to change, typing the new value, and hitting Enter on your keyboard. 
Once you have made your changes, you can click the "Update Year 12" to reflect the total of years 0-11. 

## Re-Calculate Projected Housing Units
**Please note: Re-calculating projected housing units table from tract or assessor data will cause all projected housing unit data you have previously entered to be overwritten!

## Create Development Summary 
By choosing "Create Development Summary" you will get the Residential Development Summary Report created automatically. You can "Export Development Summary" into Microsoft Excel format with ResidentialDevelopmentSummary.xls as default name. You can also export Projects Summary.
