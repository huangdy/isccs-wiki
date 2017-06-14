# getStreetAddress
### Description  
The API gets a list of street address based on the basic query and a list of city as request parameters. Each returned street address has format of name and id.
 
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

* city (*required*)
  * The list of city will be used to filter.


### Example Request
http://localhost:8080/isccs/api/facility/getStreetAddress?list=70,7057&city=2394:127:13

### Example Response
```
[
    {
        name: "1131 Chapel Crossing Rd, Glynco, Glynn, Georgia",
        id: 43032
    },
    {
        name: "1132 Chapel Crossing Rd, Glynco, Glynn, Georgia",
    id: 43036
    }
]