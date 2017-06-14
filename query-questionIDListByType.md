# query-questionIDListByType
### Description  
This API returns the list of question text and id based on the type.
       
### Params

* type (*required*)
  * Either "department" or "facility"

### Example Request  
http://localhost:8080/isccs/api/question/query/idList?type=department

### Example Response  
```javascript
[
    {
        "id": 1,
        "title": "Implementation of ISC compliance"
    },
    {
        "id": 2,
        "title": "ISC and Agency standards comparison"
    }, 
    .
    .
    .
]