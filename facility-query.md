# 
### Description  
The API will return one and only one facility id (asset_id) based on the query parameters.
### Params
* list (*required*)
  * The standard query list, it shall only contain one agency, one bureau and one facility.

### Example Request
http://localhost:8080/isccs/api/facility/query?list=70,7057,7057:BA1

### Example Response  
```javascript
{

    "id": "a08t0000000l76FAAQ",
    "name": "Artesia(Federal Law Enforcement Training Center (FLETC):BA1)",
    "submitter_uploader": "Submitted By: [ISC, Admin], Uploaded By: [Cs, Isc]"

}