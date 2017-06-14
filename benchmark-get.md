### Description  
The API gets the benchmark response forms based on the query parameters and the form ID.     
### Params
  * list (*required*)
    * The standard query list, it shall only contain one bureau if the type is department, and only one facility if the type is facility.
  * type (*required*)
    * either facility or department
  * id (*required*)
    * the form ID.

### Example Request
* type: facility
http://localhost:8080/isccs/api/benchmark/get?list=13,1314,1314:10&type=facility&id=54

### Example Response  
```javascript
{
    Sections: [{
        Section: "3.1 Application of a Risk Management Process Description of areas to be assessed: Evaluation of the facility’s application of the ISC Risk Management Process.",
        Questions: [{
            id: 30,
            num: 1,
            question: "How well has the tenant implemented the FSC standard for making decisions regarding security or do they use other internal procedures?",
            scale: "0=N/A 1=Very Poor 2=Poor 3=Satisfactory or Other Procedures 4=Good 5=Exceptional",
            reference: "The Risk Management Process: An ISC Standard, 1st Edition, August 2013, Appendix D: How to Conduct a Facility Security Committee, Section D.3, Page D-4"
        }, ....
    }],
    Score_Section: [{
        id: 30,
        score: 4
        },...
    }],
    Signature: {
        ReportingYear: "2015",
        DepartmentOrAgency: "Department of Commerce",
        Bureau: "National Oceanic and Atmospheric Administration",
        SubmitterName: "White, Snow",
        SubmitterOrg: "7000",
        SubmitterEmail: "snow.white@dhs.gov",
        SubmitterPhone: "(703) 123-4567"
    }
}