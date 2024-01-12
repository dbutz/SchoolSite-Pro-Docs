# Creating Tracts
## Tract - a polygon dataset
The tract dataset describes the location and phasing for planned residential development within the district. Each residential project can be represented by either a point or polygon feature. However, polygons are the preferred method since they more accurately depict the size and location of the projects.  

 

The tract dataset is not required if your district has little or no residential development planned. However, if your district has several planned projects, it is useful to maintain those projects and their descriptive data in a map dataset. SchoolSite Pro will extract this information for use in the forecast model if desired. Districts with little or no planned development may not need a tract map dataset, but may wish to enter the few housing units planned directly into the Forecast Properties dialog box for SchoolSite Pro.  

## Source:
This type of housing information is available through most local city and county planning agencies.  In most areas, developers are required to submit tract map applications for any residential housing construction.  Copies of tentative tract maps can be obtained at little or no cost.  Some districts have city and county agencies automatically send a copy of the tentative tract map to the facilities planning department.  Contact your local planning agency for further information on receiving copies or notices of tract map applications.

## Required Fields:
1. **STDYAREA** – a "Text" field.  This should be the study area where the tract is located. The TRACT field should be defined as data type "Text" with a length of 6. No NULL values or special characters in these fields.

2. **TYPE** – a "Text" field with a length of  3.  The value in this field represents the general description of the housing type for the tract. SchoolSite Pro allows up to six housing categories shared between all tract and assessor data which can be defined by the user. For example, if your district has substantial differences in number of students generated from various socioeconomic areas, you could assign Type 1 as low-income housing and Type 2 as high-income housing. However, in general DDP uses and recommends the following categories:  

   Suggested "Type" Codes:
   * SFD - Single-family Detached
   * MFA - Multi-Family Attached (such as condos, townhomes, duplexes or owned attached units)
   * APT - Apartments (rental units)
   * MLB - Mobile Homes (In some districts, mobile home parks generate students at a substantially higher rate than typical detached homes)
   * SFA - Single Family Attached
   * AFD - Affordable Housing

**Please Note:** When creating a forecast, the Student Yield Factors (SYFs) are applied to each of the six types. If the housing types for the SYFs are defined differently than is used in the tract dataset, the forecasts will be incorrect.  For this reason, once the housing types have been defined in the tract dataset, the same definitions should be used to define the housing types in the assessor dataset.  

 

3. __PH1___ – a "Short Integer" or "Long Integer" data type. With SchoolSite Pro, you can break the scheduling of housing construction into as many as 10 phases.  This field, along with the fields Ph2_, Ph3_, Ph4_, Ph5_, Ph6_, Ph7_, Ph8_, Ph9_, and Ph10_, stand for phase 1, phase 2, phase 3, etc..  Each of these 10 fields are defined the same.  It is not necessary to use all 10 phases when you are breaking up the phasing of a development, but they should always be entered starting with Ph1_.  Some developments may be scheduled to finish in a relatively short period of time (such as a few months), while others may take years to complete.  The numbers in these fields (such as 35, 50, 100, etc.) represent the number of units to be completed in that phase. Remember: The Ph1_ field corresponds to the first phasing schedule of the project regardless of when the project actually begins. It does not correspond to the first year of student population forecasts. If you have project phasing, regardless of what year construction begins, always enter the first phase in the Ph1_ field. No NULL values or special characters in these fields.

4. **PH1_COMP** – a "Date" field.  This field works in conjunction with the phasing number field described above.  Enter the expected date of the corresponding phase completion.  As there can be up to 10 phase numbers, there can be up to 10 phase completion dates (i.e. Ph2_comp, Ph3_comp, etc.).

## Optional fields for certain reports:
**DEVELOPER** - a string field containing the name of the housing developer for the given tract. This is only used when making a project summary report and is not required for making a residential forecast with tract development data.

**PROJECT** - a string field containing the name of the housing project for the given tract. This is only used when making a project summary report and is not required for making a residential forecast with tract development data.

## Suggested Fields:
Various other fields – There are a variety of fields you may want to include on the tract dataset.  They can be defined any way you choose.  These are completely optional and are not required by SchoolSite Pro.  

* Name of developer

* Name of project

* Tract Number (or Parcel Number)

* Name of contact

* Phone number of contact

* Comments

* Total number of dwelling units planned

* Number of acres

* Description of location - enter a location by cross streets

* Status - indicate if the tract is tentative or approved
  * Suggested Status Codes:
    * ACT - Active
    * BLT - Built Out
    * INAC - Inactive
    * UNKN - Unknown

## Points to Remember:
Careful consideration should be given when deciding whether or not a tract dataset is needed. If there are only a few active projects in your district, it may be easier to enter new housing directly into a forecast rather than creating a tract dataset. In general, it makes more sense for larger districts with many active development projects to maintain the data in a tract layer.

 

Also, care should be taken when considering what projects to include.  Developments that are planned to cater to senior citizens or as second homes, although they are residential, will generate few students.  If they are included, they will falsely inflate your forecasts because those unit numbers will be multiplied by student yield factors and will generate students who will most likely not appear.  Likewise, residential projects with less than 10 housing units may generate so few students that it may not be worth updating since the number of students generated by such housing is negligible.

 

It is important to note that residential construction schedules change constantly, depending on current economic trends. Consequently, districts should contact developers at least once a year to get an update on the status of the project.  This new information can be entered into the tract dataset attribute table and can be used in subsequent forecasts.

## Phasing Example:
Here we are going to walk through a simple example of how phasing works from creating the tract data to the final resident forecast report. This example specifically highlights certain dates to illustrate in which year of the forecast those units will appear. The **base date** of this example will be **Oct 1 2023**. The tract data has units purposefully phased for 9/30/23, 10/2/23, and 10/1/24 to show how units phased a day before, a day after, and one year after the base date appear in the forecast years.

![tractInputData](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/ad9f320f-d0d0-4fbf-a6f1-37d962102dd9)

Once you have done your development research and created the tract data, you will import it into SchoolSite Pro. During the import process, you will be asked to map each unique value found in the TYPE field to one of six types, TYPE1 through TYPE6. The result is a table in SchoolSite Pro that will store this mapping that looks like this.

![housingTypes](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/86a19422-39a3-46e4-811e-a39c2d768f1d)

Once you have imported all the data and you begin to make a forecast, you will want to make sure to indicate you want to use available tract data.

![image](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/395c1194-0572-43ed-a4ed-fc54180b9c71)

Doing so will go through a process in which SchoolSite Pro will evaluate the phasing dates in the tract data compared to the base date of the forecast and place the units into the correct year of the forecast. 

Let's start with the first phase from PH1_ and PH1_COMP which has one unit phased for completion on 9/30/23. This unit does not appear in your forecast as it is phased before the Oct 1 2023 base date.

The second phase shows two units phased for completion on 10/2/23 and the third phase shows three units phased for 10/1/24, exactly one year from the base date of 10/1/23. Note that as a result, we see **five units** appear in year one of the forecast. This means that year one will include all units phased between the day **after** the base date until one full year later. The three units that hit Oct 1 2024 are added to the three units from Oct 2 2023 and they all fall within that first forecast year.

![projHousingUnits_orig](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/72ba2d1c-6502-4afa-b6ee-df5236c69c28)

At this point, we are going to manually make a change to our Projected Units table by inserting a **negative number of units** in year 9 where there was previously a zero. This can be done to model special cases such as an apartment building being demolished or some other reason why existing units would result in a loss of students. There are many additional factors to consider in these cases, so please proceed with the advice and counsel of a senior school planner.

![projHousingUnits](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/9ad7d6ab-85b1-4995-b292-33b50e5e3f4a)

![SYF](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/137306ed-ea9a-4d0a-9e3c-3e3c77de4177)


![image](https://github.com/dbutz/SchoolSite-Pro-Docs/assets/5185948/635857f2-8d5e-4dd5-a130-47596f0ed1ba)

