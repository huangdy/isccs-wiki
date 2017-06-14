# status - facility
### Description
This API returns a total count of the facilities and a list of facility based on selected bureau, the required range which is the start and end parameters, the advanced query parameters.
       
### Params
* type (*required*)
  * Either "department" or "facility"
  * Description: this will determine whether for the Department/Agency or the Facility.
* list (*required*)
  * Type: String
  * Description: This is the selected agency to return the range of the bureau belonging to this agency.
* start (*required)
   * the starting element of the whole returned list
* end (*required)
   * the ending element of the whole returned list
* showAll (*optional*)
  * Description: if not existed, default value is false/0. If it's true/1, all the items will be returned, otherwise, only the active items will be returned.
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
http://localhost:8080/isccs/api/status/tableview/facility?type=facility&list=7051&end=29&start=20&showAll=1

### Example Response  
```javascript
{
   totalCount: 4023,
   list: [
      {
         id: "a08t0000000lAKSAA2",
         name: "Ak0001 Lpoe/Housing-Alcan(Customs and Border Protection (CBP):AKAK09)",
         active: 1
      },
      {
         id: "a08t0000000l6vIAAQ",
         name: "Ak0001 Lpoe/Housing-Alcan(Customs and Border Protection (CBP):AKAK10)",
         active: 1
      },
   .
   .
   ]
}
```