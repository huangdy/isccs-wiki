# getCountsByState
### Description  
The API gets a list of counts of facility by state based on the basic query parameters.
 
### Params
* list (*required*)
  * Type: comma separated list of the state's ID.


### Example Request
http://localhost:8080/isccs/api/facility/getCountsByState?list=&type=facility

### Example Response
```javascript
[
    {
        id: "01",
        name: "Alabama",
        count: 3360
    },
    {
        id: "02",
        name: "Alaska",
        count: 10809
    },
    {
        id: "04",
        name: "Arizona",
        count: 12257
    }, 
    .
    .
]