# COMP 3040 Assignment 3

### API Description
- This API enables you to receive imformation about COVID-19 in Manitoba

### Description of Resources and Available Endpoints

> The **mb_stats** resource is how you receive Coivd-19 stats for Manitoba. Use the mb_stats API calls to return various stats on the current covid-19 situation in Manitoba.

##### Available Endpoints
---
````GET /mb_cases````  
**Description:**  
-- Get the number of covid-19 cases currently active in Manitoba
---
````GET /wpg_Cases````  
**Description:**  
-- Get the number of covid-19 cases currently active in Winnipeg
---
````GET /mb_positive/{num_days}````  
**Description:**  
-- Get the test-positive percentage in Manitoba for a number of days

**Parameters:**  
num_days ````integer````  
example: ````GET /mb_positive/{7}````  
---

### Sample Request
````curl -u "username:password" -H "Content-Type:application/json" -X GET "https://api.mbcovid.com/mb_stats/mb_positive?num_days=7"````
### Sample Response
````
{
    "percent_positive": 13.1
}
````
