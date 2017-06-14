# Facility Demographic Parse Logic
### Description
This page describe how to parse the Facility Demographic spreadsheet after uploaded.

### How to parse each form/entry

* These information from header section are required:
    * Reporting Year
    * Submitter Name
    * Submitter Organization
    * Submitter Email
    * Submitter Phone

* For each entry the following column are required:
    * reporting agency
    * reporting bureau
    * using agency
    * using bureau
    * property type
    * property use
    * asset status
    * legal interest
    * historical status
    * utilization
    * street address
    * city
    * state
    * county
    * country
    * zip code
    * installation name
    * population

* For each entry, the column is required when:
    * the property type is
        * land, the acres cannot be empty.
        * building, the square-feet cannot be empty.
        * structure, the structural units and unit of measurement can not be empty.
    * the legal interest is
        * owned, the replacement value cannot be empty.
        * lease, the lease expiration date cannot be empty.

* The duplicate entries will be rejected in the spreadsheet where the entries have same reporting agency, reporting bureau, property unique ID, and reporting year.

* If there is no asset id specified, the new asset id will be generated with the value of 'ISCCS-' plus the reporting bureau name plus '-' plus the facility's property uid.

### Modification from the original spreadsheet
* padding the '0' in front of the following columns if needed:
    * reporting/using agency
    * reporting/using bureau
    * city code
    * county code
    * country code
    * property_type
    * property_use
* convert the column value into a float value, '0.0' if not specified or blank.
    * replacement value
    * structural units
    * acres
    * square feet
* when the country code is outside United States, such as Puerto Rico, Guam.
    * the state code will be assigned if the state code is empty.
    * the state will be replaced with proper state code based on the country code if the state is incorrect.
    * the county code will be ignored if the field value is not empty.
* when using agency/bureau is null, the reporting agency/bureau will be used for the using agency/bureau.