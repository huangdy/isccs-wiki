# getCity
### Description  
The API gets a list of city based on the basic query and a list of state as request parameters. Each returned city has name and id.
 
### Params
* list (*required*)
  * Type: comma separated list of the the basic query.
* state(*required*)
  * The list of states selected from the state box.
* start (*optional*)
  * Type: Integer. Beginning index for the return city list.
  * If none, the beginning index is zero.
* end (*optional*)
  * Type: Integer. Ending index for the return city list.
  * If none, the max count-1 is used as the end index.
* filter (*optional*)
  * Type: String. Matching text (could be partial) to narrow the returned list of city.  


### Example Request
http://localhost:8080/isccs/api/facility/getCity?list=70,7057&state=13

### Example Response
```
[
    {
        name: "GLYNCO, GLYNN, GEORGIA",
        id: "2394:127:13"
    }
]