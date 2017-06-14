# facility-getInfoList
### Description  
This API returns the list of facility's information from the facility based on the list of asset_id.
       
### Params
* list (*required*)
    * This is the list of asset_id.

### Example Request  
http://localhost:8080/isccs/api/facility/getInfoList?list=a08t0000000l07SAAQ,a08t0000000lDraAAE,a08t0000000lKGSAA2
```
### Example Response  
```javascript
[
    {
        "using_bureau": "Federal Law Enforcement Training Center (FLETC)",
        "address": "1300 W Richey Avenue, Artesia, Eddy, New Mexico, 88210",
        "acres": 0,
        "replacement_value": 175322,
        "square_feet": 2940,
        "tenant_type": "Benchmark Not Submit"
    },
    {
        "using_bureau": "Federal Law Enforcement Training Center (FLETC)",
        "address": "1131 Chapel Crossing Rd, Glynco, Glynn, Georgia, 31524",
        "acres": 0,
        "replacement_value": 6377590,
        "square_feet": 4684,
        "tenant_type": "Benchmark Not Submit"
    },
    {
        "using_bureau": "Federal Law Enforcement Training Center (FLETC)",
        "address": "1131 Chapel Crossing Rd, Glynco, Glynn, Georgia, 31524",
        "acres": 0,
        "replacement_value": 3669200,
        "square_feet": 23273,
        "tenant_type": "Benchmark Not Submit"
    }
]