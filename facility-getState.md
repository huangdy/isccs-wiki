# facility-getState
### Description  
This API returns the list of name/id from the state_lookup table. This list includes all the territory, such as Puerto Rico, Guam.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].
* start (*optional*)
    * Type: Integer. Starting index.
* end (*optional*)
    * Type: Integer. Ending index.
* filter (*optional*)
    * Type: String.  Matching text (or partial) to narrow the returned list of the states.

### Example Request  
http://localhost:8080/isccs/api/facility/getState?list=70,7057,7057:BA1,7057:BA1000
```
### Example Response  
```javascript
[
    .
    .
    {
        name: "WISCONSIN",
        id: "55"
    },
    {
        name: "WYOMING",
        id: "56"
    },
    {
        name: "AMERICAN SAMOA",
    id: "AQ"
    },
    {
        name: "NORTHERN MARIANA IS",
        id: "CQ"
    },
    {
        name: "GUAM",
        id: "GQ"
    },
    {
        name: "PAULAU REPUBLIC OF",
        id: "PS"
    },
    {
        name: "MARSHALL ISLANDS",
        id: "RM"
    },
    {
        name: "PUERTO RICO",
        id: "RQ"
    },
    {
        name: "U.S. MINOR OUTLYING ISL",
        id: "UM"
    },
    {
        name: "VIRGIN ISLANDS",
        id: "VQ"
    }
]