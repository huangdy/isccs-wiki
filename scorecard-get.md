# scorecard - get
### Description  
This API returns the compliance/goal for the scorecard.
       
### Params

* type (*required*)
  * Either "department" or "facility"
  * Description: this will determine whether the Department/Agency benchmark questionnaire results or the Facility Benchmark questionnaire results are returned.
* list (*required*)
  * Type: String
  * Description: This is the list of basic query selections, the list is the combination from the agency/department, bureau, and facility if the type is 'facility'.
  * Example: 'list=[agency1, agency2[,bureau1, bureau2[,facility1, facility2]]], if there is no selection then it looks like 'list='.
* property_type (*optional*)
  * Description: The list of property_type will be used to filter, the list is separated by comma.
  * Example: 'property_type=20,35'
* property_use (*optional*)
  * Description: The list of property_use will be used to filter, the list is separated by comma.
  * Example: 'property_use=20:20,35:29'
* square_feet(*optional*)
  * Description: The range of the square feet shall be used to filter, the range is separated by comma as (min, max).
  * Example: 'square_feet=1000,100000'
* replacement_value(*optional*)
  * Description: The range of the replacement value will be used to filter, the range is separated by comma as (min, max).
  * Example: replacement_value=0,10000
* acres(*optional*)
  * Description: The range of the acres will be used to filter, the range is separated by comma as (min, max).
  * Example: acres=0,100
* structural_units(*optional*)
  * Description: The range of the structural units will be used to filter, the range is separated by comma as (min, max).
  * Example: structural_units=0,100
* legal_interest (*optional*)
  * Description: The list of legal interest will be used to filter, the list is separated by comma.
  * Example: 'legal_interest=G'
* utilization (*optional*)
  * Description: The list of utilization code will be used to filter, the list is separated by comma.
  * Example: 'utilization=5,6'
* asset_status (*optional*)
  * Description: The list of asset's status will be used to filter, the list is separated by comma.
  * Example: 'asset_status=A,I'
* historical_status (*optional*)
  * Description: The list of historical's status will be used to filter, the list is separated by comma.
  * Example: 'historical_status=3,5'
* qid (*optional*)
   * Description: This is the question id of a specific histogram.  This param is used with conjunction with the "scale" param.  
* scale (*optional*)
   * Description: This is the scale(s) of a histogram.  This param is used in conjunction with the "qid" param.  Together, user can select a question and one or more scores as further filter to re-draw all the histograms.

### Example Department Request  
http://localhost:8080/isccs/api/scorecard/get?type=department&list=70,13
```
### Example Department Response  
```json response
{
    reportingGoals: [{
        2015: {
            reporting: 25,
            Full/Siganificant: 15,
            At Least Partial/Limited: 70,
            Unacceptable: 15
        }
    }],
    query: {
        totalCount: 57,
        ytdReporting: 1,
        ytdCompliance: {
            siganificant: 0,
            partial: 1,
            unacceptable: 0
        }
    },
    national: {
        totalCount: 1179,
        ytdReporting: 53,
        ytdCompliance: {
            siganificant: 0,
            partial: 53,
            unacceptable: 0
        }
    }
}
```

### Example Facility Request  
http://localhost:8080/isccs/api/scorecard/get?type=facility&list=70
```
### Example Facility Response  
```json response
{
    reportingGoals: [{
        2015: {
            reporting: 25,
            Full/Siganificant: 15,
            At Least Partial/Limited: 70,
            Unacceptable: 15
            }
        }
    ],
    facility: {
        query: {
            totalCount: 4833,
            ytdReporting: 4833,
            ytdCompliance: {
                siganificant: 0,
                partial: 4833,
                unacceptable: 0
            }
        },
        national: {
            totalCount: 306910,
            ytdReporting: 7057,
            ytdCompliance: {
                siganificant: 0,
                partial: 7056,
                unacceptable: 1
            }
        }
    },
    single: {
        query: {
            totalCount: 2415,
            ytdReporting: 2415,
            ytdCompliance: {
                siganificant: 0,
                partial: 2415,
                unacceptable: 0
            }
        },
        national: {
            totalCount: 3524,
            ytdReporting: 3524,
            ytdCompliance: {
                siganificant: 0,
                partial: 3523,
                unacceptable: 1
            }
        }
    },
    multi: {
        query: {
            totalCount: 2418,
            ytdReporting: 2418,
            ytdCompliance: {
                siganificant: 0,
                partial: 2418,
                unacceptable: 0
            }
        },
        national: {
            totalCount: 3533,
            ytdReporting: 3533,
            ytdCompliance: {
                siganificant: 0,
                partial: 3533,
                unacceptable: 0
            }
        }
    }
}
```