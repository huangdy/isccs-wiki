# facility-getMaxSqFt
### Description  
This API returns the maximum of the square feet based on the selected agency/bureau/facility list which is from the basic query section.
       
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getMaxSqFt?list=70

```
### Example Response  
```javascript
[
    {
        max: 1192629
    }
]