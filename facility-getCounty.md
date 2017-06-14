# getCounty
### Description  
The API getCounty gets a list of county based on the basic query and a list of state as request parameters. Each returned county has name and id.
 
### Params
* list (*required*)
  * Type: comma separated list of the state's ID.
* start (*optional*)
  * Type: Integer. Beginning index for the return county list.
  * If none, the beginning index is zero.
* end (*optional*)
  * Type: Integer. Ending index for the return county list.
  * If none, the max count-1 is used as the end index.
* filter (*optional*)
  * Type: String.  Matching text (could be partial) to narrow the returned list of the county.


### Example Request
http://localhost:8080/isccs/api/facility/getCounty?list=01

### Example Response
```javascript
[
    {
        name: "AUTAUGA ",
        id: "01:001"
    },
    {
        name: "BALDWIN ",
        id: "01:003"
    },
    {
        name: "BARBOUR ",
        id: "01:005"
    },
    {
        name: "BIBB ",
        id: "01:007"
    },
    {
        name: "BLOUNT ",
        id: "01:009"
    },
    .
    .
]
