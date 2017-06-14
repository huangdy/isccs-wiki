# facility-# facility-getAssetStatus
### Description  
This API returns a list of asset status with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].


### Example Request  
http://localhost:8080/isccs/api/facility/getAssetStatus?list=70

```
### Example Response  
```javascript
[
    {
        name: "Current Mission Need",
        id: "A"
    },
    {
        name: "Report of Excess Accepted",
        id: "C"
    },
    {
        name: "Determination to Dispose",
        id: "F"
    },
    {
        name: "Cannot Currently be Disposed",
        id: "G"
    },
    {
        name: "Future Mission Need",
        id: "I"
    }
]
```