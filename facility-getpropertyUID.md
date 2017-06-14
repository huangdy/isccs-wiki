# facility-getPropertyUID
### Description  
This API returns a list of property UID with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getPropertyUID?list=70,7057
```
### Example Response  
```
[
    {
        property_uid: "BA1"
    },
    {
        property_uid: "BA10"
    },
    {
        property_uid: "BA1000"
    },
    {
        property_uid: "BA1001"
    },
    {
        property_uid: "BA1002"
    },
    .
    .
]
```