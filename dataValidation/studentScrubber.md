# Using the Student Scrubber
The Student Scrubber utility cleans your student data file prior to geocoding and use in SchoolSite Pro by removing all special characters from the file and (optionally) standardizing the address field.

 

**Please Note:**  This tool is integrated into the SchoolSite Pro Geocoding Tool—it is provided on the SchoolSite Pro toolbar for users who wish to clean their student data file before geocoding directly within ArcGIS (i.e. without the SchoolSite Geocoding Tool).

 

You can access the Student Scrubber through the SchoolSite Pro toolbar. To open the SchoolSite Pro toolbar, go to Customize > Toolbars > SchoolSite Pro Toolbar.

The SchoolSite Pro Toolbar is visible now. Click on the SchoolSite Pro Student Scrubber tool to open the wizard

The SchoolSite Pro Student Scrubber will open:

## Step 1: Input File
Use the browse button to select the student file you want to Scrub. The file must be located in a file geodatabase.  The Student Scrubber can be used to clean any file geodatabase table.

## Step 2: Remove Special Characters
Choose the fields you would like Scrubbed and the special characters to be removed.  By default all fields and symbols– with the exception of the pound symbol (#)–are checked on.  This is the recommended method to Scrub the data.

Click OK to Scrub the student file, or go to Step 3 to standardize the student file.

 

After the Scrubbing is complete a report will appear in the bottom of the wizard and the file you selected will be clean.

**Pro Tip:** If you want to copy the end result of the fields that were scrubbed, drag your cursor from one corner of the grid to another so that all the entries are selected. Then, on your keyboard press Ctrl+C to copy the entries onto your clipboard. Now, you can paste the end results into any text editor.

 

## Step 3: Standardize Student Data (optional)
To prepare the student file for the geocoding process you can standardize the student data with this tool.

 

Check the box next to "This is a student file I want to geocode (optional)".

 

Choose the standardization method:

 

* Standardize and split address components into individual fields
Use this option when you are using DDP's custom address locator style to geocode the student file.  Most commonly used when geocoding to a street centerline data source.

* Standardize and keep address components in a single field
Use this option when you are using one of ESRI's standard address locator styles to geocode the student file.  Most commonly used when geocoding to address parcel points or polygons.

 

Choose the address field you would like to standardize.

Click Run when you are finished setting up the wizard. After the Scrubbing and standardization has completed a report will appear in the bottom of the wizard, a clean and standardized output file will be produced, and a success message will appear.

The output file will be located in the same location as your original file with _Standardized appended to the name.

## The Remove Nulls dialog box
NULL values in data files may cause unwanted results or problems. You can use the Student Scrubber to replace the NULL values in your student file by clicking Yes. By clicking Yes, the NULL values found in your student file will be replaced with an empty string.

 

If you would like to find out where the NULL values are for yourself, you can do the following:

 

1. Open ArcMap

2. Add the data file to ArcMap

3. Open the data file attribute table

4. Click on each field header and choose Sort Ascending. If there are any NULL values, they will be brought to the top of each field (see example):

## Fixing NULL values
Please contact Davis Demographics for detailed instructions on how to replace NULL values.
