* Error Report:
   * There are 87 entries missing City Code. To fix it, I used 'City Name' and County Code + State Code. 85 entries are resolved.
      * Two entries still unresolved. There asset_id are the following:
         * a08t0000000DscmAAC: City Name is District of Columbia in County/District of Cloumbia and State/District of Columbia
         * a08t0000000zFfyAAE: City Name is North Slope in County/North Slope and State/Alaska
   * There is one facility, asset ID is a08t0000000y1JeAAI without property UID

* Resolution:
   * To use the city name + county code + state code to figure the missing city code.
      * Two unresolved cities:
         * To use '9999'/Unknown for facility: a08t0000000zFfyAAE
         * To use '0010'/Washington for the facility: a08t0000000DscmAAC
   * To use asset_id as property UID for the facility: a08t0000000y1JeAAI

### Detailed information
```javascript
/facility/upload: frpp-2015-1.xlsx, path: uploads\frpp-2015-1.xlsx_1_1491591155167
[1870]: missing using_bureau
[26825]: missing City
[27802]: missing City
[31906]: missing City
[33960]: missing property UID
[33961]: missing City
[42450]: missing City
[48001]: missing City
[48003]: missing City
[48004]: missing City
[48006]: missing City
[48022]: missing City
[48023]: missing City
[48043]: missing City
[48046]: missing City
[48049]: missing City
[48062]: missing City
[48064]: missing City
[48066]: missing City
[48077]: missing City
[48086]: missing City
[48097]: missing City
[48098]: missing City
[48101]: missing City
[48102]: missing City
[48103]: missing City
[48104]: missing City
[48105]: missing City
[48155]: missing City
[48183]: missing City
[48195]: missing City
[48204]: missing City
````

### Error for Sheet 2
```javascript
[13395]: missing City
[16567]: missing City
[16572]: missing City
[24698]: missing City
[35093]: missing City
[35097]: missing City
[40322]: missing City
[40323]: missing City
````

### Sheet 3 Error Page
```javascript
[2375]: missing City
[2376]: missing City
[2392]: missing City
[41144]: missing City
[41168]: missing City
[41219]: missing City
[42587]: missing City
````
### Error for sheet 4
```javascript
/facility/upload: frpp-2015-4.xlsx, path: uploads\frpp-2015-4.xlsx_1_1491591478497
[751]: missing City
[752]: missing City
[753]: missing City
[754]: missing City
[755]: missing City
[756]: missing City
[757]: missing City
[758]: missing City
[18073]: missing City
[18074]: missing City
[18075]: missing City
[34388]: missing City
[37170]: missing City
[37177]: missing City
[37180]: missing City
[37193]: missing City
[38318]: missing City
[38380]: missing City
[39938]: missing City
[40940]: missing City
[40941]: missing City
[40942]: missing City
[40943]: missing City
[40947]: missing City
[40948]: missing City
[40950]: missing City
[40951]: missing City
````

### Error for sheet 5
```javascript
/facility/upload: frpp-2015-5.xlsx, path: uploads\frpp-2015-5.xlsx_1_1491591567251
[92]: missing City
[16222]: missing City
[16238]: missing City
[16246]: missing City
[16247]: missing City
[16248]: missing City
[16251]: missing City
[16258]: missing City
[16259]: missing City
[16261]: missing City
[16263]: missing City
[16270]: missing City
[34165]: missing City
[36849]: missing City
[39263]: missing City
````