# Non-FRPP Processing
### Description
This page states how the Non-FRPP Form been parsed.

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

* For each entry, the column is required when:
    * the property type is
        * land, the acres cannot be empty.
        * building, the square-feet cannot be empty.
        * structure, the structural units and unit of measurement can not be empty.
    * the legal interest is
        * owned, the replacement value cannot be empty.
        * lease, the lease expiration date cannot be empty.

* The duplicate entries will be rejected in the spreadsheet where the entries have same reporting agency, reporting bureau, property unique ID, and reporting year.