### Description  
The API get the benchmark question section average by the query parameters.
### Params
  * list (*required*)
    * The standard query list, it shall only contain one bureau if the type is department, and only one facility if the type is facility.
  * type (*required*)
    * either facility or department
  * advanced query parameters, such as state, county, ...

#### Example Request by state
http://localhost:8080/isccs/api/benchmark/average?list=7057&type=facility&state=13

#### Example Response by state
```javascript
{
    Risk Management Process: 2.5,
    Active Shooter Guidance: 2.5,
    Prohibited Items Guidance: 2.5,
    Facility Security Committees: 2.5
}
````

#### Example Request by county
http://localhost:8080/isccs/api/benchmark/average?list=1314&type=facility&county=003:01

#### Example Response by county
```javascript
{
    Risk Management Process: 2.3,
    Active Shooter Guidance: 2.7,
    Prohibited Items Guidance: 2.4,
    Facility Security Committees: 2.8
}