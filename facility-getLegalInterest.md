# facility-getLegalInterest
### Description  
This API returns a list of legal interest with the format of name/id based on the selected agency/bureau/facility list which is from the basic query section.
       
### Params
* list (*required*)
    * This is the basic query's selection, the format is as list=[agency1, agency2[,bureau1, bureau2[,facility1,facility2,...]]].

### Example Request  
http://localhost:8080/isccs/api/facility/getLegalInterest?list=70
```
### Example Response  
```
[
    {
        name: "Owned",
        id: "G"
    },
    {
        name: "Leased",
        id: "L"
    },
    {
        name: "State Goverment-Owned",
        id: "S"
    }
]
```