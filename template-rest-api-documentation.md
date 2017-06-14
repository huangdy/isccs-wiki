# getList
### Description  
This is a description of the getList request blah blah blah  
### Params
* param1 (*required*)
  * Type: comma seperated list. Or the word `all`.
* param2 (*optional*)
  * Type: Id of...


___
### Example Request  
**GET**
```
/api/facility/getList?param1=blahblah&param2=blahblah
```

**POST** ` /api/facility/getList`
```javascript
{
    "param1":"",
    "param2":""
}
```
___
### Example Response  
```javascript
{
    "data":[
        {
            "name":"",
            "value":""
        },
        ...
    ]
}
```

___
### Example Error Response
Server error code: `404`
```javascript
{
    "error":{
        "msg":"",
    }
}
```
**Or**
```javascript
{
    "error":[
        {
            "msg":"",
        },
        ...
    ]
}
```