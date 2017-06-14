# 
### Description  
The API gets a list of complete/in-complete benchmark response forms submitted by the logged in user. This query result also depends on the login user agency and the role.
### Params
* list (*required*)
  * The standard query list, it shall only contain one bureau if the type is department, and only one facility if the type is facility.
  * type (*required*)

### Example Request
* type: department
http://localhost:8080/isccs/api/benchmark/query?list=70,7057&type=department

* type: facility
http://localhost:8080/isccs/api/benchmark/query?list=13,1314,1314:10&type=facility

### Example Response  
```javascript
[
    {
        name: "Submitted By: White, Snow @ "2016-03-14 14:19:00", Status: Complete",
        id: 54
    },
    {
        name: "Blank Form",
        id: 0
    }
]