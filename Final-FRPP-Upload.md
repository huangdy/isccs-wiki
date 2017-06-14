# Final FRPP Upload
### Description
This page describe how to upload the final FRPP data from DHS.

### Normalized the cell data
* padding with '0' for city, county, country, agency, and bureau code if needed.
* filled the state code for all the cities from territory/outside U.S.

### look-up tables changed

* Agency table
   * Updated the agency name if difference occurred.
   * Updated data is from the column 'Using Bureau Name' from the Final FRPP spreadsheet.
   * Do we need to update one more time with the column 'Reporting Agency Name' ???

* Bureau table:
   * Updated the bureau names if different from previous version.
   * Updated data is from the column 'Using Bureau Name' from the Final FRPP spreadsheet.

* Installation Name:
   * rebuild the lookup table.

* City/County lookup
   * Updated the lookup based on the final FRPP.