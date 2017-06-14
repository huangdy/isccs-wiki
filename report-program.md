# report - program
### Description  
This API returns the benchmark average scores for dept./agency and facility program-wise.
       
### Params
No parameter needed since it's for every agnecy.

### Example Department Request  
http://localhost:8080/isccs/api/report/program
```
### Example Department Response  
```json response
{
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
            compliance: {
                totalCount: 1179,
                ytdReporting: 77,
                ytdCompliance: {
                    siganificant: 14,
                    partial: 50,
                    unacceptable: 13
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
            compliance: {
                totalCount: 306910,
                ytdReporting: 7063,
                ytdCompliance: {
                    siganificant: 22,
                    partial: 6858,
                    unacceptable: 183
                }
            }
        }
    },
    Benchmark Scores: [
    {
        Reporting Organization Name: "Department of Commerce",
        2.1: 2.2,
        2.2: 2.6,
        2.3: 2.2,
        Dept./Agency Avg. Benchmark Score: 2.3,
        3.1: 2.5,
        3.2: 2.5,
        3.3: 2.5,
        4.1: 2.5,
        Facility Avg. Benchmark Score: 2.5
    },
    {
        Reporting Organization Name: "Social Security Administration",
        2.1: 1.7,
        2.2: 2.6,
        2.3: 2.3,
        Dept./Agency Avg. Benchmark Score: 2.2,
        3.1: "-",
        3.2: "-",
        3.3: "-",
        4.1: "-",
        Facility Avg. Benchmark Score: "-"
    },
    .
    .
    {
        Reporting Organization Name: "Architect of the Capitol",
        2.1: "-",
        2.2: "-",
        2.3: "-",
        Dept./Agency Avg. Benchmark Score: "-",
        3.1: "-",
        3.2: "-",
        3.3: "-",
        4.1: "-",
        Facility Avg. Benchmark Score: "-"
    },
    ],
    Benchmark Trend: {
        2016: {
            2.1: 2.6,
            2.2: 2.7,
            2.3: 2.8,
            Dept./Agency Avg. Benchmark Score: 2.7,
            3.1: 2.5,
            3.2: 2.5,
            3.3: 2.5,
            4.1: 2.4,
            Facility Avg. Benchmark Score: 2.5
        }
    }
}