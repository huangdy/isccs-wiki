# facility-getLatLonList
### Description  
This API returns the list of asset_id, latitude, and longitude from the facility based on the basic query and advanced query parameters.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].
    * The list can contain any advanced query parameters, such as county=003:01,001:01 or state=01,03.

### Example Request  
http://localhost:8080/isccs/api/facility/getLatLonList?list=&county=003:01
```
### Example Response  
```javascript
[
    {
        id: "a08t0000000khZVAAY",
        y: 30.5484,
        x: -87.8757,
        tt: "y"
    },
    {
        id: "a08t0000000kru3AAA",
        y: 30.2723,
        x: -87.7173,
        tt: "y"
    },
    {
        id: "a08t0000000nX39AAE",
        y: 30.2537,
        x: -87.8136,
        tt: "n"
    },
    .
    .
]