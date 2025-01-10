## Error message:

If SchoolSite Pro fails to export certain reports to Excel format, it might be caused by a corrupt installation of Excel on the workstation.
We have seen an error in the Event Log that indicates an invalid cast occurred or might refer to a QueryInterface related to: Unable to cast COM object of type ’Microsoft.Office.Interop.Excel.ApplicationClass


## Solution:
This post from Microsoft seems to track the issue to how Excel is installed on the workstation. You might find that other types of reports do work when exporting to Excel that the reason for this is because in certain cases in SchoolSite Pro, we use the TableToExcel tool from ArcToolbox which uses some Python library to create the Excel file so it does not seem to suffer from the same issues as the .Net library we use in other situations.

https://docs.microsoft.com/en-us/answers/questions/258475/unable-to-cast-com-object-of-type-39microsoftoffic.html

https://knowledge.autodesk.com/support/inventor/troubleshooting/caas/sfdcarticles/sfdcarticles/Error-in-rule-Unable-to-cast-COM-object-of-type-Micr...

https://docs.microsoft.com/en-us/answers/questions/258475/unable-to-cast-com-object-of-type-39microsoftoffic.html


