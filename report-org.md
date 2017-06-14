# report - organizational
### Description  
This API returns the benchmark average scores for dept./agency and facility for the specific agency.
       
### Params
* list
  * the list shall contain one and only one agency ID.

### Example Department Request  
http://localhost:8080/isccs/api/report/organizational?list=70,7041

### Example Department Request  
http://localhost:8080/isccs/api/report/organizational?list=70

```
### Example Department Response  
```json response
{
    Organization Name: "Department of Homeland Security",
    Scorecard: {
        department: {
            reportingGoals: [
            {
                2016: {
                    reporting: 25,
                    Full/Siganificant: 15,
                    At Least Partial/Limited: 70,
                    Unacceptable: 15
                }
            }
            ],
            national: {
                totalCount: 1177,
                ytdReporting: 75,
                ytdCompliance: {
                    siganificant: 14,
                    partial: 48,
                    unacceptable: 13
                }
            },
            compliance: {
                totalCount: 24,
                ytdReporting: 24,
                ytdCompliance: {
                    siganificant: 14,
                    partial: 0,
                    unacceptable: 10
                }
            }
        },
        facility: {
            reportingGoals: [
            {
                2016: {
                    reporting: 25,
                    Full/Siganificant: 15,
                    At Least Partial/Limited: 70,
                    Unacceptable: 15
                }
            }
            ],
        national: {
            totalCount: 328731,
            ytdReporting: 7062,
            ytdCompliance: {
                siganificant: 22,
                partial: 6839,
                unacceptable: 201
            }
         },
        compliance: {
            totalCount: 50470,
            ytdReporting: 4838,
            ytdCompliance: {
                siganificant: 22,
                partial: 4669,
                unacceptable: 147
            }
        }
    },
   Benchmark Scores: [
    {
        Reporting Organization Name: "United States Congress",
        2.1: 1.4,
        2.2: 2.2,
        2.3: 2.2,
        Dept./Agency Avg. Benchmark Score: 1.9,
        3.1: "-",
        3.2: "-",
        3.3: "-",
        4.1: "-",
        Facility Avg. Benchmark Score: "-"
    },
    {
        Reporting Organization Name: "Congressional Committees and     Subcommittees",
        2.1: 3.4,
        2.2: 2.7,
        2.3: 3.3,
        Dept./Agency Avg. Benchmark Score: 3.1,
        3.1: "-",
        3.2: "-",
        3.3: "-",
        4.1: "-",
        Facility Avg. Benchmark Score: "-"
    },
    .
    .
    {
        Reporting Organization Name: "United Nations World Food Program",
        2.1: 1.8,
        2.2: 2.7,
        2.3: 2.3,
        Dept./Agency Avg. Benchmark Score: 2.3,
        3.1: "-",
        3.2: "-",
        3.3: "-",
        4.1: "-",
        Facility Avg. Benchmark Score: "-"
    }
    ],
    Benchmark Trend: {
        2016: {
            2.1: 2.7,
            2.2: 2.4,
            2.3: 2.6,
            Dept./Agency Avg. Benchmark Score: 2.6,
            3.1: "-",
            3.2: "-",
            3.3: "-",
            4.1: "-",
            Facility Avg. Benchmark Score: "-"
        }
    }
}