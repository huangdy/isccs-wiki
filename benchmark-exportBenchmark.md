# exportBenchmark
### Description  
This API returns the benchmark for either Department or Facility based on the basic and advanced query selection.
       
### Params

* type (*required*)
  * Either "department" or "facility"
  * Description: this will determine whether the Department/Agency benchmark questionnaire results or the Facility Benchmark questionnaire results are returned.
* list (*required*)
  * Type: String
  * Description: This is the list of basic query selections, the list is the combination from the agency/department, bureau, and facility if the type is 'facility'.
  * Example: 'list=[agency1, [,bureau1, [,facility1, facility2]]]. If the type is department, at most one agency can be selected. For the facility, at most one bureau can be selected.
  * score (Optional)
     * Description: set to true to generate random scores for each question.

### Example Request
* For the Department Benchmark Export:
http://localhost:8080/isccs/api/benchmark/export?type=department&list=70,7001,7002,7057

* For the Facility Bechmark Export:
http://localhost:8080/isccs/api/benchmark/export?type=facility&list=7057

### Example Response  