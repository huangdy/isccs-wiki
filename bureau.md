# bureau
### Description  
This API returns a list of Bureau based on the Department(s).     
### Params

* list (*required*)
  * List of one or more department/agency ids
* start (*optional*)
  * Type: Integer. Beginning index for the return Bureau list.
  * If none, the beginning index is zero.
* end (*optional*)
  * Type: Integer. Ending index for the return Bureau list.
  * If none, the max count-1 is used as the end index.
* filter (*optional*)
  * Type: String. Matching string (can be partial) to narrow the list of returned bureaus.


### Example Request

http://localhost:8080/isccs/api/bureau?list=70

### Example Response
````javascript
[
    {
        "id": "7051",
        "name": "Customs and Border Protection (CBP)"
    },
    {
        "id": "7000",
        "name": "Department of Homeland Security"
    },
    {
        "id": "7032",
        "name": "Environmental Measurements Laboratory (DOE)"
    },
    .
    .
    .
]
````

### Example Request

http://localhost:8080/isccs/api/bureau?list=70,49&start=10&end=20

### Example Response
````javascript
[
    {
        "id": "7052",
        "name": "National Law Enforcement Communications Center"
    },
    {
        "id": "7049",
        "name": "National Protection and Programs Directorate (NPPD)"
    },
    {
        "id": "4951",
        "name": "National Radio Astronomy Observatory"
    },
    .
    .
    .
]
````
