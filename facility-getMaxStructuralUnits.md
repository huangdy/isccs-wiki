# facility-getMaxStructuralUnits
### Description  
This API returns the maximum of the structural units based on the selected agency/bureau/facility list which is from the basic query section.
       
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getMaxStructuralUnits?list=70
```
### Example Response  
```
[
    {
        max: 822800
    }
]