# facility-getCountry
### Description  
This API returns the list of name/id based on the basic query selection.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getCountry?list=12,28,70
```
### Example Response  
```
[
    {
        name: "AMERICAN SAMOA "
    },
    {
        name: "GUAM "
    },
    {
        name: "NORTHERN MARIANA IS "
    },
    {
        name: "PUERTO RICO "
    },
    {
        name: "UNITED STATES "
    },
    {
        name: "VIRGIN ISLANDS "
    }
]