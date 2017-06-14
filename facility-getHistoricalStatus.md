# facility-# facility-getHistoricalStatus
### Description  
This API returns a list of historical status with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].


### Example Request  
http://localhost:8080/isccs/api/facility/getHistoricalStatus?list=70,7057

```
### Example Response  
```json response
[
    {
        name: "National Register Eligible (NRE)",
        id: "3"
    },
    {
        name: "Not Evaluated",
        id: "5"
    },
    {
        name: "Evaluated, Not Historic",
        id: "6"
    }
]
```