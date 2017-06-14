### Description  
The API updates the facility demographic data based on the web form input, the uploader is the one logged in.

### Params
  * facility(*required*)
     * it contains all the necessary fields to create/update the facility demographic data.
  * signature(*required*)
     * It contains the reporting year and the submitter's information. The uploader information will be used based on the logging user.

#### The Facility Demographic Object
```javascript
facility:
{
   asset_id: "a08t0000000l76FAAQ",
   acres: 0,
   square_feet: 14000,
   latitude: "",
   longitude: "",
   zip_code: "88210",
   population: 0,
   replacement_value: 5807000,
   tenant_type: "Multi-Tenant",
   child_care_center: false,
   lease_expiration_date: "",
   using_agency: 70,
   using_bureau: 7057,
   property_type: 35,
   property_use: 29,
   legal_interest: "G",
   installation_name: "Artesia",
   street: "1300 W Richey Avenue",
   city: 0050,
   county: 015,
   state: 35
}
````
#### The Signature Object
````javascript
signature:
{
   fiscal_year: "2014",
   dept_agency: "Department of Homeland Security",
   bureau: "Federal Law Enforcement Training Center (FLETC)",
   submitter_org: "Department Of Homeland Security, ISCCS",
   submitter_name: "ISC, Admin"
   submitter_email: "isccs.admin@dhs.gov",
   submitter_phone: "(703) 123-4567",
   uploader_name: "Cs, Isc",
   uploader_email: "isccs.admin@dhs.gov",
   uploader_phone: ""
}
````

#### Example Request
* http://localhost:8080/isccs/api/facility/update?facility=fObject&signature=sObject
