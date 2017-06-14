# facility-getDetails
### Description  
This API returns the facility demographic object based on the requested list which contains one and only one facility.
       
### Params
* list(*required*)
    * This is the query parameter which leads to one and only one facility

### Example Request  
http://localhost:8080/isccs/api/facility/getDetails?list=70,7057,7057:BA1
```
### Example Response  
```javascript
{
   facility: {
      asset_id: "a08t0000000l76FAAQ",
      acres: 0,
      square_feet: 14000,
      latitude: "",
      longitude: "",
      zipcode: "88210",
      population: 0,
      replacement_value: 5807000,
      child_care_center: false,
      lease_expiration_date: "",
      using_agency_name: "Department of Homeland Security",
      using_agency: "70",
      using_bureau_name: "Federal Law Enforcement Training Center (FLETC)",
      using_bureau: "7057",
      property_type_name: "Building",
      property_uid: "BA1",
      property_type: "35",
      property_use_name: "Other Institutional Uses",
      property_use: "29",
      legal_interest_name: "Owned",
      legal_interest: "G",
      installation_name: "Artesia",
      street_address: "1300 W Richey Avenue",
      city_name: "Artesia",
      city: "0050",
      county_name: "Eddy",
      county: "015",
      state_name: "New Mexico",
      state: "35"
   },
   signature: {
      fiscal_year: "2014",
      dept_agency: "Department of Homeland Security",
      bureau: "Federal Law Enforcement Training Center (FLETC)",
      submitter_org: "Department Of Homeland Security, ISCCS",
      submitter_name: "ISC, Admin",
      submitter_email: "isccs.admin@dhs.gov",
      submitter_phone: "(703) 123-4567",
      uploader_name: "Cs, Isc",
      uploader_email: "isccs.admin@dhs.gov",
      uploader_phone: ""
   }
}
```