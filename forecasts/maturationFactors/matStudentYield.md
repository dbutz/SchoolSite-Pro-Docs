# Maturation Student Yield Factors
## Calculating Student Yield Factors

The Maturation Student Yield Factors (MSYFs), combined with the total number of housing units estimated
at build out for each study area will generate a student projection for each study area.  The MSYFs are
similar to student yield factors used in the ten year projections. However, MSYFs are calculated 
regardless of year of construction and are applied to year 12  in the projected housing variable table
for each study area.

 

Two sets of data are required to calculate Maturation Student Yield Factors: current geocoded student 
data by residence (provided by the District) and current housing unit data (from the District's local
County Tax Assessor files).  Each student record and tax assessor record is geocoded by their given
address.  You may then use ArcMap analysis tools to select a sampling of tax assessor/housing unit 
records and student records to determine student yields.  The samples should include different housing
types and the students being generated from those housing units. At maturation the sample of housing 
units should include houses of all ages both old and new so as not to skew the yield factors towards 
younger age children from newer homes.

## Entering Maturation Student Yield Factors
1. Once you have calculated the factors, you will need to enter them in the Student Projection Properties
 table.  Open the projection to be modified. Then, from the SchoolSite Projection Toolbar, click the 
 projection properties button , Residential Projections > Modify Variables.


Under "Specify variable to modify", click the dropdown menu to Maturation Yields. Be sure to select Maturation Yields rather than student yields.

Choose the house type to apply maturation yield factors.  Remember, Types 1 through 4 correspond to the types as defined in your tract and assessor datasets.

Next, specify study areas to display by choosing one of three choices:  

The first is to display study areas that are “Currently selected on the map”.  If you have selected study areas from the map display, this option will be available.
If chosen, only the selected study areas will display for modification.  If you have no study areas selected, this option will not be available.  

The second option is “Select by attendance area”.  With this option, choose the grade range you wish 
to assign maturation yield factors. Then choose the specific school from the drop down menu as 
illustrated below.  This will display only the study areas that are currently assigned to that school attendance area. You can then modify maturation yield factors for just those study areas.  
Use this option when a specific area of the district is known to experience significantly higher or lower build out rates than surrounding areas.

The third (and most common) option is “Select all” which displays all study areas.  It is important to understand that when you make changes to the variables with the Select All option,
that changes will affect all study areas in the district.

The Maturation Yields are stored in the table on the right hand side of the form.  Once the study areas to display option is selected, you can modify each individual cell, 
changing the factor for each year and each study area.  
