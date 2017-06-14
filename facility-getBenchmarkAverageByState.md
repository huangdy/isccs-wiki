# getBenchmarkAverageByState
### Description  
The API gets a list of benchmark average for the facility by state based on the basic query parameters.
 
### Params
* list (*required*)
  * The basic query parameters.

### Example Request
http://localhost:8080/isccs/api/facility/getBenchmarkAverageByState?list=7057&type=facility

### Example Response
```javascript
[
    {
        id: "10",
        name: "Delaware",
        average: 2.5
    },
    {
        id: "12",
        name: "Florida",
        average: 2.5
    },
    {
        id: "13",
        name: "Georgia",
        average: 2.5
    },
    .
    .
]