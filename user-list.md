# User - List
### Description  
This API returns the list of the user's information including user_id, username, email, phone, agency, role.
       
### Params
* dept_id: (Optional)
    * Type: interger. It can be 2 digits for agency id or 4 digits for bureau.
* role: (Optional)
    * Type: String.
    * Value:
      * 'a': Administrator
      * 'l': Uploader
      * 'u': User

### Example Request
http://localhost:8080/isccs/api/user/list

### Example Response  
```javascript
[
  {
    username: "isccs.admin@dhs.gov",
    dept_id: "6666",
    role: " Administrator",
    role_id: "a",
    dept_name: "ISC-CS"
  },
  {
    username: "dhs.fema",
    dept_id: "7041",
    role: " Uploader",
    role_id: "l",
    dept_name: "Federal Emergency Management Agency (FEMA)"
  },
  {
    username: "dhs.agency",
    dept_id: "70",
    role: " Administrator",
    role_id: "a",
    dept_name: "Department of Homeland Security"
  },
  {
    username: "dhs.fletc",
    dept_id: "7057",
    role: " User",
    role_id: "u",
    dept_name: "Federal Law Enforcement Training Center (FLETC)"
  }
]
````
### Example Request
http://localhost:8080/isccs/api/user/list?role=a

### Example Response  
```javascript
[
  {
    username: "isccs.admin@dhs.gov",
    dept_id: "6666",
    role: " Administrator",
    role_id: "a",
    dept_name: "ISC-CS"
  },
  {
    username: "dhs.agency",
    dept_id: "70",
    role: " Administrator",
    role_id: "a",
    dept_name: "Department of Homeland Security"
  }
]
````
### Example Request
http://localhost:8080/isccs/api/user/list?dept_id=70&role=a

### Example Response  
```javascript
[
  {
    username: "dhs.agency",
    dept_id: "70",
    role: " Administrator",
    role_id: "a",
    dept_name: "Department of Homeland Security"
  }
]
````