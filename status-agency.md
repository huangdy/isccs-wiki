# status - agency
### Description
This API returns a total count of agencies and a list of agency list based on the query parameters. If the type is department then each agency object contains a field, active which can be toggled per user's choice. If the type is facility, the return object will not contain active field.
       
### Params
* type (*required*)
  * Either "department" or "facility"
  * Description: this will determine whether for the Department/Agency or the Facility.
* list (*required*)
  * Type: String
  * Description: This is the list of basic query selections, the list is the combination from the agency/department, bureau, and facility if the type is facility.
  * Example: list=[agency1, agency2[,bureau1, bureau2[,facility1, facility2]]], if there is no selection then it looks like list=.
* start (*required*)
  * Description: the starting index of the whole selected list.
* end (*required*)
  * Description: the ending index of the whole selected list.
* showAll (*optional*)
  * Description: if not existed, default value is false/0. If it's true/1, all the items will be returned, otherwise, only the active items will be returned.

### Example Request
* For the Department/Agency:
http://localhost:8080/isccs/api/status/tableview/agency?type=department&list=&end=29&start=20&showAll=1

### Example Response  
```javascript
{
   totalCount: 86,
   list: [
      {
         id: "15",
         name: "Department of Justice",
         active: 1
      },
      {
         id: "16",
         name: "Department of Labor",
         active: 1
      },
   .
   .
]
```

* For the Facility Questionnaire:
http://localhost:8080/isccs/api/status/tableview/agency?type=facility&list=7057&start=0&end=9

### Example Response  
```javascript
{
   totalCount: 1,
   list: [
      {
         id: "70",
         name: "Department of Homeland Security",
         active: 1
      }
   ]
}