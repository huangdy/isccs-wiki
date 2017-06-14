* User
  * /api/user
        * /[list] (user-list)
        * /[update] (user-update)
* Agency
  * [/api/agency] (agency)
  * [/api/bureau] (bureau)
* Benchmark
  * /[api/facility_benchmark/export](facility_benchmark-export)
  * /[api/benchmark/export](benchmark-exportBenchmark)
  * /[api/benchmark/query](benchmark-query)
  * /[api/benchmark/get](benchmark-get)
  * /[api/benchmark/update](benchmark-update)
* Facility
  * /[api/facility]  (facility-getList)
     * /[update](facility-update)
     * /[getDetails](facility-getDetails)
     * /[getStreetAddress](facility-getStreetAddress)
     * /[getPropertyType](facility-getpropertytype)
     * /[getPropertyUse](facility-getpropertyuse)
     * /[getState](facility-getState)
     * /[getCity](factility-getCity)
     * /[getCounty](facility-getCounty)
     * /[getCountry](facility-getCountry)
     * /[getMaxAcres](facility-getMaxAcre)
     * /[getMaxSqFt](facility-getMaxSqFt)
     * /[getMaxStructuralUnits](facility-getMaxStructuralUnits)
     * /[getMaxRplValue](facility-getMaxRplValue)
     * /[getMaxPop](facility-getMaxPop)
     * /[getLegalInterest](facility-getLegalInterest)
     * /[getAssetStatus](facility-getAssetStatus)
     * /[getHistoricalStatus](facility-getHistoricalStatus)
     * /[getUtilization](facility-getUtilization)
     * /[getCountsByState](facility-getCountsByState)
     * /[getCountsByCounty](facility-getCountsByCounty)
     * /[getBenchmarkAverageByState](facility-getBenchmarkAverageByState)
     * /[getBenchmarkAverageByCounty](facility-getBenchmarkAverageByCounty)
     * /[getLatLonList](facility-getLatLonList)
     * /[getInfoList](facility-getInfoList)
* Query
  * /api/query
     * /[statistics] (query-histogram)
  * /api/statistics
     * /[report] (statistics-report)
* Saved Query
    * /api/saved_query
         * /[list] (saved_query-list)
         * /[save] (saved_query-save)
         * /[delete] (saved_query-delete)
* Question
  * /api/question
     * /[questionIDListByType] (query-questionIDListByType)

* Scorecard
  * /api/scorecard
     * /[get] (scorecard-get)
* Report
  * /api/report
     * /[program] (report-program)
     * /[organizational] (report-org)
* Status
   * /api/status/tableview
      * /[agency] (status-agency)
      * /[bureau] (status-bureau)
      * /[facility] (status-facility)
      * /[update] (status-update)
* Util
   * /api/util
      * /[geocoder] (util-geocoder)