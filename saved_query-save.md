# saved_qery - save
### Description  
This API saves the query with the login user.
       
### Params
* queryName (*required*)
    * the name for the query object.
* shared (*required*)
    * the boolean value either true or false.
* queryParams (*required*)
    * the JSON object to represent the query object.


### Example Request
* HTTP POST
    * http://localhost:8080/isccs/api/saved_query/save?queryName="AnyName"&shared=true&queryParams=queryJSONObject
* The curl POST command-prompt 
    * curl -H "Content-Type: application/json" -X POST -d "{\"queryParams\": {\"type\":\"facility\",\"list\":\"13,1314\"},\"queryName\":\"Daniel's Testing Saved Query\"}" http://localhost:8080/isccs/api/saved_query/save

```
### Example Response  
```json response
[]
```