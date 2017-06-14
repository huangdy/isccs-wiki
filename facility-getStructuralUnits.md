# facility-getUtilization
### Description  
This API returns a list of structural units with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getStructuralUnits?list=70,7057
```
### Example Response  
```
[
    {
        name: "Unknown Type",
        id: ""
    },
    {
        name: "Unutilized",
        id: "5"
    },
    {
        name: "Utilized",
        id: "6"
    },
    {
        name: "Underutilized",
        id: "7"
    }
]
```