# Creating Students

## Students - a point feature class
The student point feature class is created by geocoding a table of student information to a street centerline layer, address point layer or other reference data typically used for geocoding.  When geocoding students to street centerlines, it is important to use offset parameters to be sure that student points are not placed directly on a street and they fall within a distinct study area and attendance boundary.  It should be noted that in order to effectively develop enrollment forecasts, you will need a minimum of three years (preferably four years) of geocoded students all extracted from the SIS at, or close, to the same date each year.  That date is usually the fall reporting period each year for fall-generated forecasts.

## Source:
This data comes directly from the District’s student information system (SIS) and is downloaded in one of the following formats and imported into a geodatabase table ready for geocoding.  The downloaded data should be exported from the SIS into either Excel (.xlsx), comma or tab-delimited text (.csv) or dbase (.dbf).

## Required Fields:
There are three required fields that must be added to the geocoded student attribute table in order for SchoolSite Pro to properly identify students to be excluded or optionally included in the enrollment projections or various types of redistricting plans.

 

1. **GRD** - This field is defined in ArcGIS as a “short integer” field and should only contain numeric values, typically ranging from 0 through 12, and sometimes -1 and/or -2.  0 represents kindergarten, -1 or -2 would represent TK or PK (see discussion below).  The District’s student data downloaded from the SIS may include a Grade or other named field, but the values in that field many times include characters other than numbers such as KA or KP, PK, or some other value of the District’s choosing. This type of data is not recognized for use with SchoolSite Pro and those values must be transferred or interpreted to include only numeric values in the GRD field.  The GRD field with standardized grade values is critical to both the forecasting model and redistricting plans.

2. **SCHL_CODE** - This field is defined as a “short integer” and contains the school ID or program ID number of the student’s school or program of attendance.  It is critical that the ID number in the student table matches a corresponding point with the school ID in the schools point feature class (i.e. there needs to be a location where the student is attending school).

3. **STUTYPE** - This field is used to identify certain types of students that will be excluded or optionally included in the enrollment projection model as well as students that will be excluded from boundary planning (i.e. a particular group of students don’t move during a boundary change).  The STUTYPE field is defined as a “text” field of 2 characters in length.

# STUTYPE Field Explained:
The STUTYPE field contains numerous two-letter code values to identify and standardize various types of students, whether they are special education, pre-kindergarten, home study, etc.  The reason these students are identified with a STUTYPE code is because certain students may or may not take classroom space which is relevant to the discussion of projections and facility needs, and in other instances certain types of students may need to be identified as not being moved in certain redistricting scenarios (i.e. special day class in self-contained classrooms).

 

Student type classifications are prioritized where some student classifications take precedence over others.  This can happen when a student can be classified under two or more different codes.  For example, if a student lives outside the district but is also a special education student.

 

It is also critical that STUTYPE classifications be consistent between different year’s student geocoded data.  If certain students are being excluded in development of enrollment projections from the most current student data file, those same students, based upon the codes, will be excluded from previous years in the projection calculations.  The mathematical calculations in the projections may be in error if there is no consistency in coding different student types from year to year.

 

The two-letter STUTYPE codes used by SchoolSite Pro are explained below and are listed in order of precedence for coding each student record:

 
* <ins> Charter School student </ins> (CH)- Students residing within the District boundary attending a charter school.  These students usually do not take classroom space in one of the District’s regular public schools.  These types of students can be <ins>optionally included</ins> in resident projections and resident redistricting plans and are <ins>always included</ins> in reports for staffing projections and redistricting plans based upon enrollment.

* <ins> Adult Education student </ins>  (AD)- Adult education students are usually not included in a student data file, however if they are they are coded with AD.  Typically these students do not require a seat in the public schools. They are <ins>automatically excluded</ins> from both enrollment projections and all types of redistricting plans.

* <ins> Non-Public student </ins> (NP)- Students attending a program or school not typically provided by the school district.  These may be students in a county program or other situation where classroom space is not used. They are <ins>automatically excluded</ins> from both enrollment projections and all types of redistricting plans.

* <ins> Other student </ins> (OT)- This is a miscellaneous student type to be used in cases where no other student type is appropriate.  Identifying students as ‘other’ can be useful to identify special groups of students who you may wish to include or exclude from projections or redistricting plans.  These types of students can be <ins>optionally included</ins> in resident projections and resident redistricting plans and are always included in reports for staffing projections and redistricting plans based upon enrollment.

* <ins> Alternative Education student </ins> (AE)- This is a blanket term utilized for students not enrolled in a traditional form of education.  This may be online classes, vocational programs or programs for students with social or behavior problems.  They are usually identified separately from other students as they do not take traditional classroom space.  They are <ins>automatically excluded</ins> from both enrollment projections and all types of redistricting plans.

* <ins> Home/Hospital student </ins> (HH)- Home schooled or students located in hospitals don’t traditionally take classroom space. They are <ins>automatically excluded</ins> from both enrollment projections and all types of redistricting plans.

* <ins>Special Education student</ins> (SE)- Special education programs can take many forms, from remedial reading and part-day pull out programs to severely disabled students who require special classroom facilities.  For use in SchoolSite Pro, the SE code is reserved for the later types of students; those who require special facilities and therefore are not involved in boundary changes and for which you may not wish to include in traditional enrollment forecasting methodologies.  Students in part-time resource specialist types of programs who are usually mainstreamed with other students in the schools are not considered SE.  Special education usually represents approximately 2-3% of the District’s student population.  These types of students can be <ins>optionally included</ins> in resident projections and resident redistricting plans and are <ins>always included</ins> in reports for staffing projections and redistricting plans based upon enrollment.

* Independent Study student (IS)-  Students guided by a teacher but usually does not take classes with other students every day.  These could also be online students.  These students may or may not require a seat in a public school.  These types of students can be optionally included in resident projections and resident redistricting plans and are always included in reports for staffing projections and redistricting plans based upon enrollment.

* <ins>General Education K-12 student</ins> (GE)- Regular students in kindergarten through 12th grade residing within the District’s boundaries and is not classified as being in any of the programs above.  These students are the bulk of your student population and are always included in redistricting plans and projections.

## How Classification Codes are used in SchoolSite Pro Redistricting Plans:
There are three types of redistricting plans that can be created in SchoolSite Pro:

 

1. Plan by Current Resident Students
1. Plan by Projected Resident Students (i.e. forecasted students)
1. Plan by Current Resident and Enrollment
 

There are slight variations in how classification codes are used in creating each type of plan.

 

## Current Resident Students Plan
During setup for Current Resident Students, non-K12 students as well as the following classes of students are automatically excluded from boundary planning as well as reporting in the plan statistics window:  AD, NP, AE, HH, OD, UM

 

During setup for Current Resident Students, in addition to students coded as GE, you have the option of <ins>including<ins> the following classes of students:  CH, OT, SE, and IS.

 

Including any of these five classes of students will involve those students being moved during the boundary planning process and they will be included in the statistics window under the appropriate grade levels.

 

## Projected Resident Students Plan
The students moved as well as reported in the statistics window are those that were included or not included by choice in the development of the enrollment projections being referenced in the plan.  For example, if special education students were excluded from the projections, they will not be in the forecasted numbers used in the boundary plan.

 

## Current Enrollment Plan
During setup for plans based upon Current Enrollment, the software will determine which students are outside the District (OD) or non-geocoded (UM).  Those students will not be moved during the boundary planning process.  In the statistics window, OD and UM students will be listed by their school of enrollment under a separate OD_UM column.   Of the remining geocoded students residing in the District, those students outside of grades -1 through 12 are automatically excluded from the boundary planning process but are reported with their enrolled school under the Non_PK12 column in the statistics window.

 

Once the out of District, unmatched and non-PK12 students have been identified, you have an option to choose a field in your student data to identify which of the remaining -1 through 12th grade students you may wish to exclude from boundary planning and reporting.  The default field is STUTYPE.  Using the STUTYPE field, you have the <ins>option of excluding</ins> any of the remaining classes of students, such as SE, OT, IS, CH, etc.  For those that you choose to exclude, they will not be moved during the boundary planning process, however, they will appear as part of the enrollment at their school under a separate column in the statistics window similar to Non_PK12 and OD_UM.

 

If you choose <ins>not to exclude</ins> them from boundary planning, they will be treated as a regular student and will be subject to moving during the boundary planning process and will be reported under the appropriate grade level in the statistics window.

 

<ins>If you choose an optional field other than STUTYPE to identify classes of students</ins>, you can create any classification codes you wish to identify students to be excluded from the boundary planning process.  The out of District, unmatched and non-PK12 tests will still be performed, but you are provided unlimited flexibility as to how to code and select the remaining resident PK/TK through 12th grade students for boundary planning.  For example, you could code a group of students in a specific program such as dual language program offered only at specific schools to be excluded from the boundary planning process so they remain at the program school.  Or you may choose more specific codes for handling special education classes.

 

## How Classification Codes are used in SchoolSite Pro Enrollment Forecasting:
There are essentially two types of projections that can be created in SchoolSite Pro:  student residence and optionally school of enrollment.

 

The standard projection model within SchoolSite Pro includes projections by residence at the study area level.  Utilizing those projections by residence is the basis for setting up any redistricting plans based upon Projection Resident Students. So if there any students excluded from a projection based upon a STUTYPE classification, those same students will be excluded from any Projected Resident Student redistricting plan.

 

An option is available to create school of enrollment projections (i.e. staffing projections) which are derived from the resident projections. 

 

## Resident Projections
The use of the STUTYPE field and the classification of students for creating a resident projection operates similar to the setup of a redistricting plan using resident students.

 

During setup for resident projections, grades 0 through 12 are automatically included for forecasting and the following classes of students are automatically excluded from the projection calculations as well as any reports based upon the projections:  AD, NP, AE, HH, OD and UM.

 

During setup for resident projections, in addition to grades 0-12 GE students, you have the option of including the following classes of students:  CH, OT, SE, and/or IS.  If you include these students they will be incorporated in the projections along with all other students at their appropriate grade level. If you choose not to include them, they will not appear in the projections or any reports.

 

## School of Enrollment (Staffing) Projections
Since projections by school of enrollment are based upon the underlying resident projections, the choices you have made regarding including or excluding students for your resident projections carries over into the school of enrollment projections.  For example, excluding special education (SE) from your resident projections excludes them from school of enrollment projections.  There are a few exceptions in that out-of-district and unmatched students are included in the school of enrollment projections.  To learn more about how school of enrollment projections are calculated, see the following help topic.
 
 ## Davis Demographics' Student Type Classifications in order of priority: 
 
<table>
<TR>
      <TH COLSPAN="5"><H3>Student Types used in Redistricting Plans (for students with grades -1 through 12)</H3>
      </TH>
   </TR>
  <tr>
    <th>Code</th>
    <th>Student Type</th>
    <th>Plans by Residence</th>
    <th> Plans by Enrollment </th>
    <th> Plans by Projected Students </th>
  </tr>
  <tr>
    <td>NP</td>
    <td>Non-public student</td>
    <td color="#0000ff">Excluded</td>
    <td>Included</td>
    <td>Excluded</td>     
  </tr>
  <tr>
    <td>AD</td>
    <td>Adult education</td>
    <td>Excluded</td>
    <td>Included</td>
    <td>Excluded</td> 
  </tr>
  <tr>
    <td>AE</td>
    <td>Alternative education student</td>
    <td>Excluded</td>
    <td>Included</td>
    <td>Excluded</td> 
  </tr>
  <tr>
    <td>HH</td>
    <td>Home/hospital student</td>
    <td>Excluded</td>
    <td>Included</td>
    <td>Excluded</td> 
  </tr>
  <tr>
    <td>OT</td>
    <td>Other student</td>
    <td>Optional</td>
    <td>Included</td>
    <td>*Inherited</td> 
  </tr>
  <tr>
    <td>CH</td>
    <td>Charter school student</td>
    <td>Optional</td>
    <td>Included</td>
    <td>*Inherited</td> 
  </tr>
  <tr>
    <td>IS</td>
    <td>Independent school student</td>
    <td>Optional</td>
    <td>Included</td>
    <td>*Inherited</td> 
  </tr>
  <tr>
    <td>SE</td>
    <td>Special education student</td>
    <td>Optional</td>
    <td>Included</td>
    <td>*Inherited</td> 
  </tr> 
  <tr>
    <td>GE</td>
    <td>Resident K-12 student</td>
    <td>Included</td>
    <td>Included</td>
    <td>Included</td> 
  </tr>


</table>

 *Inherited indicates that student type will be included if the residential projection included that optional type during setup. 
 
 <table>
<TR>
      <TH COLSPAN="5"><H3>Student Types used in Projections
(for students with grades -1 through 12)</H3>
      </TH>
   </TR>
  <tr>
    <th>Code</th>
    <th>Student Type</th>
    <th>Resident Projections</th>
    <th>Staffing Projections</th>
    <th>Mobility Calculation</th>
  </tr>
  <tr>
    <td>NP</td>
    <td>Non-public student</td>
    <td>Excluded</td>
    <td>Excluded</td>
    <td>Excluded</td>     
  </tr>
  <tr>
    <td>AD</td>
    <td>Adult education</td>
    <td>Excluded</td>
    <td>Excluded</td>
    <td>Excluded</td> 
  </tr>
  <tr>
    <td>AE</td>
    <td>Alternative education student</td>
    <td>Excluded</td>
    <td>Excluded</td>
    <td>Excluded</td> 
  </tr>
  <tr>
    <td>HH</td>
    <td>Home/hospital student</td>
    <td>Excluded</td>
    <td>Excluded</td>
    <td>Excluded</td> 
  </tr>
  <tr>
    <td>OT</td>
    <td>Other student</td>
    <td>Optional</td>
    <td>*Inherited</td>
    <td>*Inherited</td> 
  </tr>
  <tr>
    <td>CH</td>
    <td>Charter school student</td>
    <td>Optional</td>
    <td>*Inherited</td>
    <td>*Inherited</td> 
  </tr>
  <tr>
    <td>IS</td>
    <td>Independent school student</td>
    <td>Optional</td>
    <td>*Inherited</td>
    <td>*Inherited</td> 
  </tr>
  <tr>
    <td>SE</td>
    <td>Special education student</td>
    <td>Optional</td>
    <td>*Inherited</td>
    <td>*Inherited</td> 
  </tr> 
  <tr>
    <td>GE</td>
    <td>Resident K-12 student</td>
    <td>Included</td>
    <td>Included</td>
    <td>Included</td> 
  </tr>


</table>
 
 *Inherited indicates that student type will be included if the residential projection included that optional type during setup.
 
## Suggested Additional Fields:
The District will have to decide what information would be most useful in your planning efforts. The more information on the file, the more alternatives you will have to query and graphically display your student data. You may want to include additional attributes such as:

 

* Ethnicity

* Language Proficiency

* Track (if your district is on a year round schedule)

* Homeroom

* Parent or Guardian

* Inter/Intra-district transfer

* Unique student ID code

* Address (actual residence, no P.O. Box addresses)

* City

* Zip

## Excluding students from the redistricting process:
During the creation of a plan by current students and current enrollment you will be asked to select a field from which you can choose one or more categories of students that can be excluded from the redistricting process. The identified students will remain at their current school of attendance regardless of any boundary changes. These students usually belong to a campus specific program such as special needs, magnet school, or academy etc.  

## Points to Remember:
* All fields you wish to have available for reporting in the Redistricting Extension, must be included in the student table before geocoding is started

* Data from related tables must be physically joined to the geocoded student table prior to using the student data in the Redistricting Extension.

* No null values or special characters can be in these fields before attempting to create a new redistricting plan.

## For More Information:
Students must be geocoded by residence in order to perform redistricting and to obtain realistic projections (using the SchoolSite Pro Projection Extension). For more information on how to geocode, see the ArcGIS help file or the Getting to Know ArcGIS manual.
 

 
