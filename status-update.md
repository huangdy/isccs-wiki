# status - update
### Description
This API will accept two parameters which are id and active. This API will update the active field for the id specified. If the id is an agency id then all the bureau and facilities all be changed. If the id is a bureau then the bureau and all the facilities used by this bureau will be updated. Otherwise, only that facility will be updated with the active field.
       
### Params
* id (*required*)
  * Description: This id can be an agency which is two-digits, a bureau which is four-digits, or a facility id which is the asset id of the facility.
* active (*required*)
  * Description: The value could be either 1 or 0. When the type is department, the active flag will affect all the bureaus if the id is the agency id. Otherwise, only the selected bureau will be changed. When the type is facility, the active flag will affect all the bureaus and facilities if the id is an agency. If the id is bureau then all the facilities within this using agency will be affected/changed.

### Example Request
* update with type = department
http://localhost:8080/isccs/api/status/update?type=department&id=28&active=0

### Check Bureau Status
* To check the result, use the following link:
http://localhost:8080/isccs/api/status/tableview/bureau?type=department&list=28&start=0&end=9&showAll=1

### Check Bureau Response  
```javascript
{
   totalCount: 3,
   list: [
      {
         id: "2800",
         name: "Social Security Administration",
         active: 0
      },
      {
         id: "2804",
         name: "Social Security Administration",
         active: 0
      },
      {
         id: "2805",
         name: "SSA Office of the Inspector General (FTS Only)",
         active: 0
      }
   ]
}
```

### Check Facility Status
* To check the facility
http://localhost:8080/isccs/api/status/tableview/facility?type=facility&list=2804&start=0&end=9&showAll=1

### Check Facility Response
```javascript
{
   totalCount: 1407,
   list: [
      {
         id: "a08t0000000ka0nAAA",
         name: "Northern Lights(Social Security Administration:AK3473)",
         active: 0
      },
      {
         id: "a08t0000000kLGuAAM",
         name: "Federal Building-Courthouse(Social Security Administration:AL0010)",
         active: 0
      },
      .
      .
   [
}
```

### Toggle the Bureau Level Request
* udpate the bureau:
http://localhost:8080/isccs/api/status/update?id=2804&active=1

### Check Bureau Status
* To check the result, use the following link:
http://localhost:8080/isccs/api/status/tableview/bureau?type=department&list=28&start=0&end=9&showAll=1

### Check Bureau Response  
```javascript
{
   totalCount: 3,
   list: [
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

### Check Facility Status
* To check the facility
http://localhost:8080/isccs/api/status/tableview/facility?type=facility&list=2804&start=0&end=9&showAll=1

### Check Facility Response
```javascript
{
   totalCount: 1407,
   list: [
      {
         id: "a08t0000000ka0nAAA",
         name: "Northern Lights(Social Security Administration:AK3473)",
         active: 1
      },
      {
         id: "a08t0000000kLGuAAM",
         name: "Federal Building-Courthouse(Social Security Administration:AL0010)",
         active: 1
      },
      .
      .
   [
}
```