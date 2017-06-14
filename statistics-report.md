# statistics-report
### Description  
This API returns the Query parameters, a Summary section and the Histogram section for the report. The query result will be based on the type, the basic query, and the advanced query sections.
       
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

* For the Department request:
http://localhost:8080/isccs/api/statistics/report?type=department&list=00,28,13,70
````
{
    query: {
        Agency/Department: "Department of Commerce, Department of Homeland Security, Social Security Administration, United States Congress",
        Bureau: "All bureaus of Department of Commerce, All bureaus of Department of Homeland Security, All bureaus of Social Security Administration, All bureaus of United States Congress"
    },
    summary: {
        # Dept/Agency: 4,
        # Dept/Agency Reporting : 3,
        % Dept/Agency Reporting : 75,
        # Bureaus: 108,
        # Bureaus Reporting : 52,
        % Bureaus Reporting : 48.15,
        Benchmark Avg. Score: 3,
        2.1 Dept./Agency ISC Implementation Guidance Avg. Score: 3.1,
        2.2 Utilization of the ISC RMP Avg. Score: 3,
        2.3 Compliance Metrics Avg. Score: 3.1
    },
    histogram: {
    maxY: {
        start: 0,
        length: 17
    },
    maxX: {
        start: 0,
        length: 5
    },
    list: [
    {
        qid: 1,
        scale: [
            6,
            10,
            7,
            12,
            12,
            5
        ],
    question: {
````

* For the Facility request:
http://localhost:8080/isccs/api/statistics/report?type=facility&list=00,13,28,70,7057,7051,1314,7057:BA1&state=01,05&tenantType=1,2&qIds=31,36&qScores=0,2,4&county=003:01,005:01,001:01&city=0240:003:01,0423:003:01&realPropertyType=20,35&realPropertyUse=01:20,04:20&acres=100,5000
```
{
    query: {
        Agency/Department: "Department of Commerce, Department of Homeland Security, Social Security Administration, United States Congress",
        Bureau: "All bureaus of Social Security Administration, All bureaus of United States Congress, Customs and Border Protection (CBP), Federal Law Enforcement Training Center (FLETC), National Oceanic and Atmospheric Administration",
        Facility: "All facilities of Social Security Administration, All facilities of United States Congress, All facilities of Customs and Border Protection (CBP), All facilities of National Oceanic and Atmospheric Administration, Artesia(7057:BA1)",
        Question Scores: [
            "0",
            "2",
            "4"
        ],
        Tenant Type: "Single-Tenant, Multi-Tenant",
        Acres in between: [
            "100",
            "5000"
        ],
        Questions: "Adequacy of FSL determination, FSL rating=highest facility rating",
        Property Use: "Agriculture, Grazing",
        Property Type: "Building",
        City: [
            "Bay Minette, Baldwin, Alabama",
            "Bon Secour, Baldwin, Alabama"
        ],
        County: [
            "Autauga, Alabama",
            "Baldwin, Alabama",
            "Barbour, Alabama"
        ],
        State: [
            "Arkansas"
        ]
    },
    summary: {
        # Dept/Agency: 4,
        # Bureaus: 54,
        # Bureaus Reporting : 0,
        % Bureaus Reporting : 0,
        # Facilities: 306910,
        # Facilities Reporting: 0,
        % Facilities Reporting: 0,
        Benchmark Avg. Score: 0,
        % Land: 0,
        % Building: 0,
        % Structure: 0,
        Square Feet: 0,
        Acres: 0,
        Replacement Value: "$0",
        # Multi-Tenant: 0,
        % Multi-Tenant Reporting: 0,
        # Single-Tenant: 0,
        % Single-Tenant Reporting: 0
    },
    histogram: {
        maxY: {
            start: 0,
            length: 0
    },
    maxX: {
        start: 0,
        length: 5
    },
    list: [ ]
}
```