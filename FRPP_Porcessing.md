# FRPP Processing
### Description
This page states how the original FRPP entry been interpreted and processed.     
### Modification
* padding the '0' in front of the following columns:
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
* when using agency is null, copy reporting agency to using agency.