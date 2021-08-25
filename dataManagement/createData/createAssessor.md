# Creating Assessor Data - REVIEWED

## Assessor - a point dataset
The assessor point dataset is created by geocoding a table of parcel information to a street network.  Assessor data can be used to determine student yield factors by housing type.  (See: Student Yield Factors)  Assessor point data is also used in estimating the number of existing dwelling units by study area for optional maturation projections (See: Maturation Concept).  Parcel polygon data that contains the required information can also be used by converting the polygons to a point feature class.

## Source:  
The best source for housing information is your local County Tax Assessor office.  Most Tax Assessors maintain a Property Characteristics file, which is available to the public for a nominal fee.  

## Required Fields:
1. **TYPE** – a "Text" field.  It is a description of the type of housing unit contained in the assessor record.  Be sure to use the same type definitions as discussed in the tract dataset. No NULL values or special characters in these fields.

 Suggested "Type" Codes:

 * SFD - Single family Detached

 * MFA - Multi-Family Attached

 * APT - Apartments

 * MLB - Mobile Homes

 * SFA - Single Family Attached

 * AFD - Affordable Housing
2. **UNITS** – a "Short Integer" field.  This field will contain the number of units located at a particular assessor point.  For example, a single family detached would be one unit and an apartment complex could be anywhere from one to several hundred units. No NULL values or special characters in these fields.

3. **ADDRESS** (or SITUS) - a "Text" field. This field gives the address location of each parcel.  This field is used to geocode the assessor data to the street data.

 __Suggested Field:__
1. **YearBuilt** – a "Short Integer" field.  This field will contain the year the unit was built and can be used to create student yield factors.


See topic Maturation Methodology to learn how assessor data is used in Maturation Projections.

 
