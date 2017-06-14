# status - bureau
### Description
This API returns a total count of the bureaus and a list of bureau object based on selected agency and the required range which is the start and end parameters. If the type is department then each agency object contains a field, active which can be toggled per user's choice. If the type is facility, the return object will not contain active field.
       
### Params
* type (*required*)
  * Either "department" or "facility"
  * Description: this will determine whether for the Department/Agency or the Facility.
* list (*required*)
  * Type: String
  * Description: This is the selected agency to return the range of the bureau belonging to this agency.
* start (*required)
   * the starting element of the whole returned list
* end (*required)
   * the ending element of the whole returned list
* showAll (*optional*)
  * Description: if not existed, default value is false/0. If it's true/1, all the items will be returned, otherwise, only the active items will be returned.

### Example Request
http://localhost:8080/isccs/api/status/tableview/bureau?type=department&list=28&start=0&end=9&showAll=true

### Example Response  
```javascript
{
   totalCount: 3,
   [
      {
         id: "2800",
         name: "Social Security Administration",
         active: 0
      },
      {
         id: "2804",
         name: "Social Security Administration",
         active: 1
      },
      {
         id: "2805",
         name: "SSA Office of the Inspector General (FTS Only)",
         active: 0
      }
   ]
}
```

### Example Request
http://localhost:8080/isccs/api/status/tableview/bureau?type=department&list=28&start=0&end=9

### Example Response
```javascript
{
   totalCount: 1,
   list: [
      {
         id: "2804",
         name: "Social Security Administration",
         active: 1
      }
   ]
}
```

### Example Request
http://localhost:8080/isccs/api/status/tableview/bureau?type=facility&list=70&start=0&end=9

### Example Response  
```javascript
{
   totalCount: 24,
   list: [
      {
         id: "7000",
         name: "Department of Homeland Security",
         active: 1
      },
      {
         id: "7001",
         name: "United States Secret Service (USSS)",
         active: 1
      },
   .
   .
   ]
}
```