# Potential Development

## Calculating Potential Development
As part of the creation of the new projection, if you specified a tract dataset during projection 
creation, Years1 through 10 would be filled in with the data from new development projects.  In some 
cases, where certain residential tracts have completion dates beyond the ten year projection time frame,
those units will be indicated in Year11 (Year11 is a place holder for units to occur after Year10.
It does not indicate those units will be built in 11 years.). Depending upon which study areas have
vacant property, you may wish to add additional units into Year11 that you feel could potentially be
built based upon land use, zoning, etc.

 

1. Determine areas of the district that have the potential for additional housing by inspecting the 
aerial photographs and comparing those areas to land use and zoning maps to determine if they are
slated for residential development.

2. In ArcGIS, add your study area and street layers to the map display.  Zoom in to the areas you have
determined from aerial photography to have potential residential development.

3. From the Data Frame Properties window, choose the General Tab.  Be sure your map units are in the
 appropriate units. (The coordinates/map units for most data provided by DDP is in feet.)

4. Using the New Polygon tool , draw a polygon of the area of potential development.  Right-click on the polygon and choose properties. In the dialog window that appears click on the area tab and ArcMap will report the area in any map units you choose such as acres.  

By multiplying the number of acres by the number of units allowed per acre, you will arrive at the maximum potential number of residential units for that area.

5. You will then need to add these numbers into Year 11 for the appropriate study areas in the Projected Housing Units table.  

## Entering Potential Development
1. Once you have calculated the number of potential development units per study area, you will need to enter them in the Student Projection Properties table.  Open the projection to be modified. Then, from the SchoolSite Projection Toolbar, click the projection properties button
2. Under "Specify variable to modify", click the dropdown menu to Projected Housing Units.

3. Choose a method to specify the study areas to display. You can scroll to the study area data you wish to modify.

4. Enter the number of potential units in Year11. As you update any values for any study area in years 0 through 11, Year12 will automatically update to reflect the total number of housing units for that study area. Year12 cannot be directly edited. SchoolSite will take the values in Year12 for each study area and for each housing type and multiply the maturation student yield factors (MSYF) to create a student projection at maturation for each study area.

5. Development Summary By choosing "Create Development Summary" you will get the Residential Development Summary Report created automatically. You can "Export Development Summary" into Microsoft Excel format with ResidentialDevelopmentSummary.xls as default name.
