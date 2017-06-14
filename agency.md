# agency
### Description  
This API returns a list of Department/Agency based on the login user's organization.     
### Params

* start (*optional*)
  * Type: Integer. Beginning index for the return facility list.
  * If none, the beginning index is zero.
* end (*optional*)
  * Type: Integer. Ending index for the return facility list.
  * If none, the max count-1 is used as the end index.
* filter (*optional*)
  * Type: String.  Matching string (can be partial) to narrow the returned list of agencies.


### Example Request  
**GET**
http://localhost:8080/isccs/api/agency

### Example Response
```javascript
[
    {
        "id": "55",
        "name": "Advisory Commission on Inter-governmental Relations"
    },
    {
        "id": "72",
        "name": "Agency for International Development"
    },
    {
        "id": "74",
        "name": "American Battle Monuments Commission"
    },
    .
    .
}
```