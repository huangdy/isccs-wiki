# User - Add
### Description  
This API saves user's information including user_id, username, email, phone, agency, role to the user table.
       
### Params
* user

### Example Request
http://localhost:8080/isccs/api/user/add?user=userJsonObject

```javascript
userJsonObject
{
   username: "isccs.admin@dhs.gov",
   email: "isccs.admin@dhs.gov",
   phone: null,
   agency: "6666",
   lastname: "Cs",
   firstname: "Isc",
   role: "a",
}
```
### Example Response  
```javascript
{
      user_id: 1
}