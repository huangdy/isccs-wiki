# util - geocoder
### Description
This API will an address and return JSON object of address and latitude/longitude.
       
### Params
* address (*required*)
  * Description: This is the address needs to be geocoded.

### Example Request
* geocode the address
http://localhost:8080/isccs/api/util/geocoder?address=4001%20North%20Fairfax%20Drive,%20Arlington,%20VA

### Check Bureau Response  
```javascript
{
   address: "4001 Fairfax Dr, Arlington, VA 22203, USA",
   latlon: {
      lat: 38.8828135,
      lng: -77.1080753
   }
}
```