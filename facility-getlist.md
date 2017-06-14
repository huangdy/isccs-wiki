# 
### Description  
The API gets a list of facilities using the Bureau ID as request parameters.  Each facility contains the name of facility and the facility unique id.     
### Params
* list (*required*)
  * Type: comma separated list of the Bureau ID.
* start (*optional*)
  * Type: Integer. Beginning index for the return facility list.
  * If none, the beginning index is zero.
* end (*optional*)
  * Type: Integer. Ending index for the return facility list.
  * If none, the max count-1 is used as the end index.
* filter (*optional*)
  * Type: String. Matching string (can be partial) to narrow the returned list of facilities.


### Example Request  
**GET**
http://localhost:8080/isccs/api/facility?list=7057

**POST** 
```
http://localhost:8080/isccs/api/facility?list=7057
___
### Example Response  
```javascript
[
    {
        name: "Artesia(7057:BA1)",
        id: "7057:BA1"
    },
    {
        name: "Artesia(7057:BA10)",
        id: "7057:BA10"
    },
    {
        name: "Artesia(7057:BA1000)",
        id: "7057:BA1000"
    },
    {
        name: "Artesia(7057:BA1001)",
        id: "7057:BA1001"
    },
    .
    .
]
```