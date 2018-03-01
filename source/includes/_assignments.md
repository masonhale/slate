
# Assignments

## All assignments (for family)

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/assignments"
```

> Example Response:

```json
[
 {
  "id": 101210,
  "user_id": 2726,
  "calendar_event_id": 66,
  "shift_id": 108,
  "job_id": 62,
  "job_name": "Timer",
  "shift_name": "Shift B",
  "created_at": "2013-10-23T17:52:24-05:00",
  "updated_at": "2013-10-23T17:52:24-05:00",
  "registration_id": null,
  "points": 2.5,
  "scheduled_by": "event_number",
  "start_at": null,
  "end_at": null,
  "start_event_number": "33",
  "end_event_number": "78",
  "start_description": "#33 Girls 6 & Under 25 Backstroke",
  "end_description": "#78 Men 15-18 200 Freestyle Relay",
  "start_description_short": "Event #33",
  "end_description_short": "Event #78",
  "sort_key": "E033:078"
}, {
  "id": 3077,
  "user_id": 2723,
  "calendar_event_id": 955,
  "shift_id": 1172,
  "job_id": 731,
  "job_name": "Clean-up",
  "shift_name": "Second Shift",
  "created_at": "2012-02-09T13:32:46-06:00",
  "updated_at": "2012-02-09T13:32:46-06:00",
  "registration_id": null,
  "points": 2.0,
  "scheduled_by": "time",
  "start_at": "2011-06-25T02:00:00-05:00",
  "end_at": "2011-06-25T02:00:00-05:00",
  "start_event_number": null,
  "end_event_number": null,
  "start_description": " 2:00 AM",
  "end_description": " 3:00 AM",
  "start_description_short": " 2:00 AM",
  "end_description_short": " 3:00 AM",
  "sort_key": "T0200:0300"
 }
]
```

Returns all job/shift assignments for current user (and family) in current account.
Note: generally you would want to limit this to assignments for the current season using the ```/assignments/current``` variation below.

### HTTP REQUEST
`GET /v2/accounts/:account_id/assignments`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope assignment query
limit | int | Number of results to return. Default/maximum = 100
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only assignments that have been updated since this timestamp (UTC) in `ISO 8601` format.

### Result Data Fields
Field | Description
------|------------
user_id | Id of user assigned to job/shift
calendar_event_id | Id of parent event for job/shift
job_name | Name of Job, e.g. "Timer"
shift_name | Name of shift, e.g. "Shift B"
registration_id | Id of registration (if job was assigned during registration)
points | Number of points associated with shift (float)
scheduled_by | Can be either 'event_number' or 'time'.
start_at | Start of shift (if scheduled_by = 'time')
end_at | Start of shift (if scheduled_by = 'time')
start_event_number | Start of shift (if scheduled_by = 'event_number')
end_event_number | End of shift (if scheduled_by = 'event_number')
start_description | Description of shift start
end_description | Description of shift end
start_description_short | Short variant description of shift start
end_description_short | Short variant description of shift end
sort_key | Value that can be used to sort assignments lexically



## Assignments for current season

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/assignments/current"
```

Same as `/assignments` above, but returns only assignments for the **current season**.

### HTTP REQUEST
`GET /v2/accounts/:account_id/assignments/current`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope assignment query
limit | int | Number of results to return. Default/maximum = 100
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only assignments that have been updated since this timestamp (UTC) in `ISO 8601` format.


## Assignments for calendar event

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events/66/assignments"
```

> Example Response:

```json
[{
  "id": 101210,
  "user_id": 2726,
  "calendar_event_id": 66,
  "shift_id": 108,
  "job_id": 62,
  "job_name": "Timer",
  "shift_name": "Shift B",
  "created_at": "2013-10-23T17:52:24-05:00",
  "updated_at": "2013-10-23T17:52:24-05:00",
  "registration_id": null,
  "points": 2.5,
  "scheduled_by": "event_number",
  "start_at": null,
  "end_at": null,
  "start_event_number": "33",
  "end_event_number": "78",
  "start_description": "#33 Girls 6 & Under 25 Backstroke",
  "end_description": "#78 Men 15-18 200 Freestyle Relay",
  "start_description_short": "Event #33",
  "end_description_short": "Event #78",
  "sort_key": "E033:078"
}]
```


### HTTP Request
`GET /v2/accounts/:account_id/calendar_events/:calendar_event_id/assignments`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope assignment query
calendar_event_id | int | Id of calendar event to scope assignment query
limit | int | Number of results to return. Default/maximum 100.
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only assignments that have been updated since this timestamp (UTC) in `ISO 8601` format.
