### Description  
The API updates the benchmark response forms.
### Params
  * list (*required*)
    * The standard query list, it shall only contain one bureau if the type is department, and only one facility if the type is facility.
  * type (*required*)
    * either facility or department
  * Scores (*required*)
    * the json object name is Scores, it contains:
      * tenant: if type is facility, it is either 'single' or 'multi'. It's null if type is department.
      * Value: the array of id/score.
      * Signature: the object to represent the submitter.

#### Example Request
* type: facility
http://localhost:8080/isccs/api/benchmark/update?list=13,1314,1314:10&type=facility&Scores=jsonObject

#### Scores Json Object
```javascript
{
  "tenant": "single",
  "Values": [{
    "id":    1,
    "score": 3
    },...
  }],
  "Signature": {
    ReportingYear: "2015",
    DepartmentOrAgency: "Department of Commerce",
    Bureau: "National Oceanic and Atmospheric Administration",
    SubmitterName: "White, Snow",
    SubmitterOrg: "7000",
    SubmitterEmail: "snow.white@dhs.gov",
    SubmitterPhone: "(703) 123-4567"
  }
}
