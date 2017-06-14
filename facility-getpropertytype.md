# facility-getPropertyType
### Description  
This API returns a list of property type with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getPropertyType?list=70,7057,7057:BA1,7057:BA1000
```
### Example Response  
```
[
    {
        name: "Building",
        id: "35"
    }
]
```