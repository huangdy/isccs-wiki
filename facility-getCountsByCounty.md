# getCountsByCounty
### Description  
The API gets a list of counts of facility by county based on the basic query parameters.
 
### Params
* list (*required*)
  * Type: comma separated list of the state's ID.


### Example Request
http://localhost:8080/isccs/api/facility/getCountsByCounty?list=&type=facility&state=01,02

### Example Response
```javascript
[
    {
        id: "001:01",
        name: "Autauga",
        count: 2
    },
    {
        id: "003:01",
        name: "Baldwin",
        count: 237
    },
    {
        id: "005:01",
        name: "Barbour",
        count: 111
    },    
    .
    .
    {
        id: "013:02",
        name: "Aleutians East",
        count: 265
    },
    {
        id: "016:02",
        name: "Aleutians West",
        count: 259
    },
    {
        id: "020:02",
        name: "Anchorage",
        count: 403
    },
    .
    .
]