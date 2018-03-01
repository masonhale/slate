# Swim results

## All swim results (for user)

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/users/2724/swim_results"
```

> Example Response:

```json
[
 {
  "id": 6256,
  "created_at": "2010-05-20T12:41:53-05:00",
  "updated_at": "2012-07-22T17:53:10-05:00",
  "type": "I",
  "athlete_id": 2724, // user_id instead here?
  "team_id": 14,
  "completed_on": "2010-05-19",
  "athlete_compete_age": 8,
  "swim_meet_id": 54,
  "swim_meet_name": "Summer 2010 (Meters)",
  "swim_meet_location": null,
  "swim_meet_altitude": null,
  "result_type": null,
  "distance": 25,
  "event_number": "15",
  "event_sort_key": "015",
  "event_age_group_name": "Girls 7-8",
  "event_athlete_min_age": 7,
  "event_athlete_max_age": 8,
  "event_gender": null,
  "stroke_code": 1,
  "heat": null,
  "lane": null,
  "place": null,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": true,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": null,
  "seed_time_int": null,
  "result_time_course": "S",
  "result_time_as_scm_int": 3225,
  "result_time_as_scy_int": 2905,
  "result_time_as_lcm_int": 3290
}, {
  "id": 6465,
  "created_at": "2010-05-20T13:57:19-05:00",
  "updated_at": "2012-07-22T17:53:10-05:00",
  "type": "I",
  "athlete_id": 2724,
  "team_id": 14,
  "completed_on": "2010-05-19",
  "athlete_compete_age": 8,
  "swim_meet_id": 54,
  "swim_meet_name": "Summer 2010 (Meters)",
  "swim_meet_location": null,
  "swim_meet_altitude": null,
  "result_type": null,
  "distance": 25,
  "event_number": "35",
  "event_sort_key": "035",
  "event_age_group_name": "Girls 7-8",
  "event_athlete_min_age": 7,
  "event_athlete_max_age": 8,
  "event_gender": null,
  "stroke_code": 2,
  "heat": null,
  "lane": null,
  "place": null,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": true,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": null,
  "seed_time_int": null,
  "result_time_course": "S",
  "result_time_as_scm_int": 5002,
  "result_time_as_scy_int": 4506,
  "result_time_as_lcm_int": 5102
 }
]
```

### HTTP Request
`GET /v2/accounts/:account_id/users/:user_id/swim_results`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
user_id | int | Id of user (athlete) results belong to
since | timestamp | Returns only results for swims since specified date
stroke | int | Returns only results of specified stroke code
distance | int | Returns only results of specified distance
course | string | Returns only results with specified course, one of 'S', 'Y' or 'L'
official | boolean | If true, only returns results marked as 'official'
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only results that have been updated since this timestamp (UTC) in `ISO 8601` format.

### Result Data Fields

Field | Type | Description
------|------|------------
type | string | Either "I" (individual) or "R" (relay)
completed_on | date | Date of swim
athlete_compete_age | int | Age of athlete at time of swim
result_type | string | F (finals), P (prelims) or S (swimoff)
distance | int | Distance of swim
event_number | string |
event_sort_key | string |
stroke_code | int |
heat | int |
lane | int |
place | int | Overall place
points | float | Points awarded for swim
is_invalid | boolean |
is_exhibition | boolean |
is_unofficial | boolean |
is_splash | boolean | If true, counts as a 'swim' for participation purposes
is_swim_up | boolean | If true, swimmer competed against older swimmers
invalid_code | |
dq_code | |
dq_description | |
seed_time_course | string | Swim course for seed time
seed_time_int | int | Seed time in hundredths of seconds
result_time_course | string | Swim course for result time
result_time_as_scm_int | int | Result time converted to SCM
result_time_as_scy_int | int | Result time converted to SCY
result_time_as_lcm_int | int | Result time converted to LCM

## Best swim results (for user)

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/users/2724/swim_results/best"
```

> Example Response:

```json
[{
  "id": 7171,
  "created_at": "2010-06-14T09:20:20-04:00",
  "updated_at": "2010-06-14T09:20:20-04:00",
  "type": "I",
  "athlete_id": 2724,
  "team_id": 14,
  "completed_on": "2010-06-12",
  "athlete_compete_age": 7,
  "swim_meet_id": 57,
  "swim_meet_name": "@Twin Creeks",
  "swim_meet_location": null,
  "swim_meet_altitude": null,
  "result_type": "F",
  "distance": 25,
  "event_number": "15",
  "event_sort_key": "015",
  "event_age_group_name": "Girls 7-8",
  "event_athlete_min_age": 7,
  "event_athlete_max_age": 8,
  "event_gender": "F",
  "stroke_code": 1,
  "heat": 3,
  "lane": 3,
  "place": 18,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": false,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": "S",
  "seed_time_int": 2947,
  "result_time_course": "S",
  "result_time_as_scm_int": 2878,
  "result_time_as_scy_int": 2593,
  "result_time_as_lcm_int": 2936
}, {
  "id": 4102996,
  "created_at": "2014-06-19T21:28:46-04:00",
  "updated_at": "2014-06-19T21:28:46-04:00",
  "type": "I",
  "athlete_id": 2724,
  "team_id": 14,
  "completed_on": "2014-06-09",
  "athlete_compete_age": 11,
  "swim_meet_id": 17014,
  "swim_meet_name": "Sharks at Dolphins",
  "swim_meet_location": "Dolphin Pool",
  "swim_meet_altitude": null,
  "result_type": null,
  "distance": 50,
  "event_number": "19",
  "event_sort_key": "019",
  "event_age_group_name": "Girls 11-12",
  "event_athlete_min_age": 11,
  "event_athlete_max_age": 12,
  "event_gender": "F",
  "stroke_code": 1,
  "heat": null,
  "lane": null,
  "place": null,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": false,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": null,
  "seed_time_int": null,
  "result_time_course": "S",
  "result_time_as_scm_int": 3180,
  "result_time_as_scy_int": 2865,
  "result_time_as_lcm_int": 3244
}, {
  "id": 7718,
  "created_at": "2010-05-27T16:00:24-04:00",
  "updated_at": "2010-05-27T16:00:24-04:00",
  "type": "I",
  "athlete_id": 2724,
  "team_id": 14,
  "completed_on": "2010-05-22",
  "athlete_compete_age": 7,
  "swim_meet_id": 58,
  "swim_meet_name": "Balcones Woods @ Great Hills",
  "swim_meet_location": "",
  "swim_meet_altitude": null,
  "result_type": "F",
  "distance": 25,
  "event_number": "35",
  "event_sort_key": "035",
  "event_age_group_name": "Girls 7-8",
  "event_athlete_min_age": 7,
  "event_athlete_max_age": 8,
  "event_gender": "F",
  "stroke_code": 2,
  "heat": 2,
  "lane": 4,
  "place": 17,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": true,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": "S",
  "seed_time_int": 5002,
  "result_time_course": "S",
  "result_time_as_scm_int": 3643,
  "result_time_as_scy_int": 3282,
  "result_time_as_lcm_int": 3716
}, {
  "id": 4102997,
  "created_at": "2014-06-19T21:28:46-04:00",
  "updated_at": "2014-06-19T21:28:46-04:00",
  "type": "I",
  "athlete_id": 2724,
  "team_id": 14,
  "completed_on": "2014-06-09",
  "athlete_compete_age": 11,
  "swim_meet_id": 17014,
  "swim_meet_name": "Sharks at Dolphins",
  "swim_meet_location": "Dolphin Pool",
  "swim_meet_altitude": null,
  "result_type": null,
  "distance": 50,
  "event_number": "39",
  "event_sort_key": "039",
  "event_age_group_name": "Girls 11-12",
  "event_athlete_min_age": 11,
  "event_athlete_max_age": 12,
  "event_gender": "F",
  "stroke_code": 2,
  "heat": null,
  "lane": null,
  "place": null,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": false,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": null,
  "seed_time_int": null,
  "result_time_course": "S",
  "result_time_as_scm_int": 3810,
  "result_time_as_scy_int": 3432,
  "result_time_as_lcm_int": 3886
}, {
  "id": 6605,
  "created_at": "2010-05-20T16:16:18-04:00",
  "updated_at": "2012-07-22T18:53:10-04:00",
  "type": "I",
  "athlete_id": 2724,
  "team_id": 14,
  "completed_on": "2010-05-19",
  "athlete_compete_age": 8,
  "swim_meet_id": 54,
  "swim_meet_name": "Summer 2010 (Meters)",
  "swim_meet_location": null,
  "swim_meet_altitude": null,
  "result_type": null,
  "distance": 25,
  "event_number": "47",
  "event_sort_key": "047",
  "event_age_group_name": "Girls 7-8",
  "event_athlete_min_age": 7,
  "event_athlete_max_age": 8,
  "event_gender": null,
  "stroke_code": 3,
  "heat": null,
  "lane": null,
  "place": null,
  "points": 0.0,
  "is_invalid": false,
  "is_exhibition": false,
  "is_unofficial": true,
  "is_splash": true,
  "is_swim_up": false,
  "invalid_code": null,
  "dq_code": null,
  "dq_description": null,
  "seed_time_course": null,
  "seed_time_int": null,
  "result_time_course": "S",
  "result_time_as_scm_int": 5894,
  "result_time_as_scy_int": 5310,
  "result_time_as_lcm_int": 6012
}]

```

Returns only the single best (fastest) times for the selected swimmer for each stroke/distance combination.

### HTTP Request
`GET /v2/accounts/:account_id/users/:user_id/swim_results/best`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
user_id | int | Id of user (athlete) results belong to
since | timestamp | Returns only results for swims since specified date
stroke | int | Returns only results of specified stroke code
distance | int | Returns only results of specified distance
course | string | Returns only results with specified course, one of 'S', 'Y' or 'L'
official | boolean | If true, only returns results marked as 'official'
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only results that have been updated since this timestamp (UTC) in `ISO 8601` format.

## Swim results for calendar event

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_event/2360/swim_results"
```

Returns all results for the family in the selected calendar event (swim meet).

### HTTP Request
`GET /v2/accounts/:account_id/calendar_events/:calendar_event_id/swim_results`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
calendar_event_id | int | Id of calendar event (swim meet) associated with the results
stroke | int | Returns only results of specified stroke code
distance | int | Returns only results of specified distance
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only results that have been updated since this timestamp (UTC) in `ISO 8601` format.

