# facility-getPropertyUse
### Description  
This API returns a list of property use with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section and the list of selected property types.
              
### Params
    * list (*required*)
        * The list contains one or more selected id from the Property_type section.
        * The list uses comma as element's separator.
    * property_type (*required*)
        * The list of property_type will be used to get what kind of property_use can be selected.

### Example Request  
http://localhost:8080/isccs/api/facility/getPropertyUse?list=70,7057,7057:BA1,7057:BA1000&property_type=35
```
### Example Response  
```
[
    {
        name: "Building:Other Institutional Uses",
        id: "35:29"
    },
    {
        name: "Building:School",
        id: "35:23"
    }
]
```