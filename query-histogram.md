# query-histogram
### Description  
This API returns the Summary section and the Histogram section for the Statistics Page. The query result will be based on the type, the basic query, and the advanced query sections.
       
### Params
* type (*required*)
  * Either "department" or "facility"
  * Description: this will determine whether the Department/Agency benchmark questionnaire results or the Facility Benchmark questionnaire results are returned.
* list (*required*)
  * Type: String
  * Description: This is the list of basic query selections, the list is the combination from the agency/department, bureau, and facility if the type is facility.
  * Example: list=[agency1, agency2[,bureau1, bureau2[,facility1, facility2]]], if there is no selection then it looks like list=.
* realPropertyType (*optional*)
  * Description: The list of property_type will be used to filter, the list is separated by comma.
  * Example: realPropertyType=20,35
* realPropertyType(*optional*)
  * Description: The list of property_use will be used to filter, the list is separated by comma.
  * Example: realPropertyType=20:20,35:29
* squareFeet(*optional*)
  * Description: The range of the square feet shall be used to filter, the range is separated by comma as (min, max).
  * Example: squareFeet=1000,100000
* replacementValue(*optional*)
  * Description: The range of the replacement value will be used to filter, the range is separated by comma as (min, max).
  * Example: replacementValue=0,10000
* acres(*optional*)
  * Description: The range of the acres will be used to filter, the range is separated by comma as (min, max).
  * Example: acres=0,100
* structuralUnits(*optional*)
  * Description: The range of the structural units will be used to filter, the range is separated by comma as (min, max).
  * Example: structuralUnits=0,100
* legalInterestIndicator (*optional*)
  * Description: The list of legal interest will be used to filter, the list is separated by comma.
  * Example: legalInterestIndicator=G
* utilization (*optional*)
  * Description: The list of utilization code will be used to filter, the list is separated by comma.
  * Example: utilization=5,6
* statusIndicator (*optional*)
  * Description: The list of assets status will be used to filter, the list is separated by comma.
  * Example: statusIndicator=A,I
* historicalStatus (*optional*)
  * Description: The list of historicals status will be used to filter, the list is separated by comma.
  * Example: historicalStatus=3,5
* city (*optional*)
   * Description: This is the list of city selected.
   * Example: city=0240:003:01,0423:003:01
* county (*optional*)
    * Description: This is the list of couty selected.
    * Example: county=003:01,005:01,001:01
* state (*optional*)
   * Description: This is the list of state selected.
   * Example: state=01,05
* tenantType (*optional*)
   * Description: This is either Single-Tenant, Multi-Tenant, or both.
   * Example: tenantType=1,2
* qIds (*optional*)
   * Description: This is the question id of a specific histogram.  This param is used with conjunction with the "scale" param.
   * Example: qIds=31,35
* qScores (*optional*)
   * Description: This is the scale(s) of a histogram.  This param is used in conjunction with the "qid" param.  Together, user can select a question and one or more scores as further filter to re-draw all the histograms.
   * Example: qScores=0,3
* leaseExpirationDate (*optional*)
   * Description: The is the lease expiration year.
   * Example: leaseExpirationDate=2016

### Example Request  
**GET**
* For the Department Questionnaire:
http://localhost:8080/isccs/api/query/statistics?type=department&list=10,1001,1002,70,7001,7002,7057

* For the Facility Questionnaire:
http://localhost:8080/isccs/api/query/statistics?type=facility&list=7057&historical_status=3,5&asset_status=A,I&utilization=5,6&legal_interest=G&property_type=20,35,40&property_use=20:20,35:31&square_feet=1000,100000&acres=0,1000
```
* To get the statistics page for the above department example that answered question id 1 with score 4 and 5
```
/api/query/statistics?type=facility&list=7001,7002,7004&qid=1&score=4,5
```

**POST** 
curl --data "type=department&list=7057,7000,0000,0003" http://localhost:8080/isccs/api/query/statistics 
___
### Example Response  
```javascript

* For type=department:
origin/development branch /data/json_samples/query.dept.json
* For type=facility:
origin/development branch /data/json_samples/query.facility.json

___
### Example Error Response (TBD)
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