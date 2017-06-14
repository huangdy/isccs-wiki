### Description  
The API creates or updates the user's agency and role.

### Params
  * user json object(*required*)
     * it contains username, agency (id) and the role (id).

#### The user Object
```javascript
user:
{
  username: huagnda,
  agency: 6666,
  role: a,
  email: first.last@dhs.gov,
  phone: 123-456-7890,
  lastname: Last,
  firstname: First
}
````

#### Example Request
* http://localhost:8080/isccs/api/user/update?user=userObject