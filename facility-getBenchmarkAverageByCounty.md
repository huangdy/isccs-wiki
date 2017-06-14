# getBenchmarkAverageByCounty
### Description  
The API gets a list of benchmark average of facility by county based on the basic query parameters.
 
### Params
* list (*required*)
  * Type: comma separated list of the state's ID.


### Example Request
http://localhost:8080/isccs/api/facility/getBenchmarkAverageByCounty?list=70&type=facility&state=01,02

### Example Response
```javascript
[
    {
        id: "097:01",
        name: "Mobile",
        average: 2.4
    },
    {
        id: "073:01",
        name: "Jefferson",
        average: 2.5
    },
    {
        id: "089:01",
        name: "Madison",
        average: 2.5
    },
    .
    .
]