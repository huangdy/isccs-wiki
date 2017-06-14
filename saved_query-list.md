# saved_qery - list
### Description  
This API returns a list of saved query parameters based on logged in user.
       
### Params
* No parameter needed to make the query.

### Example Request  
http://localhost:8080/isccs/api/saved_query/list
```
### Example Response  
```json response
[
    {
        name: "ISCCS-Everything",
        owner_name: "Cs, Isc",
        shared: true,
        query: "{"mode":"department","fields":{"department":[],"bureau":[],"facility":[],"state":[],"city":[],"county":[],"tenantType":[],"realPropertyType":[],"realPropertyUse":[],"legalInterestIndicator":[],"statusIndicator":[],"historicalStatus":[],"usingOrganization":[],"qid":[],"score":[],"acres":[],"replacementValue":[],"structuralUnits":[],"squareFeet":[],"leaseExpirationDate":[],"type":"department","qScores":[],"qIds":[]}}"
    },
    {
        name: "DHS-Agency-Everything",
        owner_name: "Doe, Mary",
        shared: true,
        query: "{"mode":"department","fields":{"department":[],"bureau":[],"facility":[],"state":[],"city":[],"county":[],"tenantType":[],"realPropertyType":[],"realPropertyUse":[],"legalInterestIndicator":[],"statusIndicator":[],"historicalStatus":[],"usingOrganization":[],"qid":[],"score":[],"acres":[],"replacementValue":[],"structuralUnits":[],"squareFeet":[],"leaseExpirationDate":[],"type":"department","qScores":[],"qIds":[]}}"
    },
    {
        name: "DHS-FLETC",
        owner_name: "DHS, User",
        shared: true,
        query: "{"mode":"department","fields":{"department":["70"],"bureau":["7057"],"facility":[],"state":[],"city":[],"county":[],"tenantType":[],"realPropertyType":[],"realPropertyUse":[],"legalInterestIndicator":[],"statusIndicator":[],"historicalStatus":[],"usingOrganization":[],"qid":[],"score":[],"acres":[],"replacementValue":[],"structuralUnits":[],"squareFeet":[],"leaseExpirationDate":[],"type":"department","qScores":[],"qIds":[]}}"
    }
]
```