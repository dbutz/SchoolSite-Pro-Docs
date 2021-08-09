# Creating Tracts
## Tract - a polygon dataset
The tract dataset describes the location and phasing for planned residential development within the district. Each residential project can be represented by either a point or polygon feature. However, polygons are the preferred method since it more accurately depicts the size and location of the projects.  

 

The tract dataset is not required if your district has little or no development planned. However, if your district has a number of planned projects, it is useful to maintain those projects and their descriptive data in a map dataset. SchoolSite will extract this information for use in the projection model if desired. Districts with little or no planned development may not need a tract map dataset, but may wish to enter the few housing units planned directly into the Projection Properties dialog box for SchoolSite.  

## Source:
This type of housing information is available through most local city and county planning agencies.  In most areas, developers are required to submit tract map applications for any residential housing construction.  Copies of tentative tract maps can be obtained at little or no cost.  Some districts have city and county agencies automatically send a copy of the tentative tract map to the facilities planning department.  Contact your local planning agency for further information on receiving copies or notices of tract map applications.

## Required Fields:
1. **STDYAREA** – a "Text" field.  This should be the study area where the tract is located. The TRACT field should be defined as data type "Text" with a length of 6.

2. **TYPE** – a "Text" field with a length of  3.  The value in this field represents the general description of the housing type for the tract. SchoolSite allows up to four housing categories which can be defined by the user. For example, if your district has substantial differences in numbers of students generated from various socioeconomic areas, you could assign Type 1 as low income housing and Type 2 as high income housing. However, in general DDP uses and recommends the following categories:  

* SFD – Single Family Detached

* MFA – Multi-Family Attached (such as condos, town homes, duplexes or owned attached units)

* APT – Apartment Complexes (rental units)

* MBL – Mobile Home Parks (In some districts, mobile home parks generate students at a substantially higher rate than typical detached homes)

* AFD – Affordable Housing
**Please Note:** When creating a projection, the Student Yield Factors (SYFs) are applied to each of the four types. If the housing types for the SYFs are defined differently than is used in the tract dataset, the projections will be incorrect.  For this reason, once the housing types have been defined in the tract dataset, the same definitions should be used to define the housing types in the assessor dataset.  

 

3. **PH1_** – a "Short Integer" data type. With SchoolSite, you can break the scheduling of housing construction into as many as 10 phases.  This field, along with the fields Ph2_, Ph3_, Ph4_, Ph5_, Ph6_, Ph7_, Ph8_, Ph9_, and Ph10_, stand for phase 1, phase 2, phase 3, etc..  Each of these 10 fields are defined the same.  It is not necessary to use all 10 phases when you are breaking up the phasing of a development, but they should always be entered starting with Ph1_.  Some developments may be scheduled to finish in a relatively short period of time (such as a few months), while others may take years to complete.  The numbers in these fields (such as 35, 50, 100, etc.) represent the number of units to be completed in that phase. Remember: The Ph1_ field corresponds to the first phasing schedule of the project regardless of when the project actually begins. It does not correspond to the first year of student population projections. If you have project phasing, regardless of what year construction begins, always enter the first phase in the Ph1_ field.

4. **PH1_COMP** – a "Date" field.  This field works in conjunction with the phasing number field described above.  Enter the expected date of the corresponding phase completion.  As there can be up to 10 phase numbers, there can be up to 10 phase completion dates (i.e. Ph2_comp, Ph3_comp etc.).

## Suggested Fields:
Various other fields – There are a variety of fields you may want to include on the tract dataset.  They can be defined anyway you choose.  These are completely optional and are not required by SchoolSite.  

* Name of developer

* Name of project

* Tract Number (or Parcel Number)

* Name of contact

* Phone number of contact

* Comments

* Total number of dwelling units planned

* Number of acres

* Description of location - enter location by cross streets

* Status - indicate if the tract is tentative or approved
  * Suggested Status Codes:
    * ACT - Active
    * BLT - Built Out
    * INAC - Inactive
    * UNKN - Unknown

## Points to Remember:
Careful consideration should be given when deciding whether or not a tract dataset is needed. If there are only a few active projects in your district, it may be easier to enter new housing directly into a projection rather than creating a tract dataset. In general it makes more sense for larger districts with many active development projects to maintain the data in a tract layer.

 

Also, care should be taken when considering what projects to include.  Developments that are planned to cater to senior citizens or as second homes, although they are residential in nature, will generate few students.  If they are included, they will falsely inflate your projections because those unit numbers will be multiplied by student yield factors and will generate students that will mostly likely not appear.  Likewise, residential projects with less than 10 housing units may generate so few students that it may not be worth updating since the number of students generated by such housing is negligible.

 

It is important to note that residential construction schedules change constantly, depending on current economic trends. Consequently, districts should contact developers at least once a year to get an update on the status of the project.  This new information can be entered into the tract dataset attribute table and can be used in subsequent projections.
 
