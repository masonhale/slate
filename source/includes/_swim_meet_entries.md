# Swim meet entries

## All swim meet entries

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/swim_meet_entries"
```

> Example Response:

```json
[
 {
  "id": 91231,
  "created_at": "2012-04-12T12:26:47-05:00",
  "updated_at": "2012-04-12T12:26:47-05:00",
  "calendar_event_id": 66,
  "type": "I",
  "user_id": 2725,
  "seed_time_course": null,
  "seed_time_int": null,
  "is_exhibition": false,
  "swim_meet_event_id": 7901,
  "event_number": "13",
  "distance": 25,
  "stroke_code": 1,
  "event_sort_key": "013",
  "event_age_group_name": "Girls 6 & Under",
  "event_athlete_min_age": 0,
  "event_athlete_max_age": 6,
  "event_athlete_gender": "F",
  "heat": null,
  "lane": null,
  "is_swim_up": false
},  {
  "id": 1468914,
  "created_at": "2015-02-11T19:51:46-06:00",
  "updated_at": "2015-02-11T19:51:46-06:00",
  "calendar_event_id": 55,
  "type": "R",
  "user_id": 2725,
  "seed_time_course": "Y",
  "seed_time_int": 12689,
  "is_exhibition": false,
  "relay_team": "A",
  "relay_position": 4,
  "relay_leg_stroke_code": 1,
  "swim_meet_event_id": 6241,
  "event_number": "1",
  "distance": 100,
  "stroke_code": 6,
  "event_sort_key": "001",
  "event_age_group_name": "Girls 6 & Under",
  "event_athlete_min_age": 0,
  "event_athlete_max_age": 6,
  "event_athlete_gender": "F",
  "heat": null,
  "lane": null,
  "is_swim_up": false,
  "is_alternate": false
 }
]
```

Returns all swim_meet_entries for all members of the family associated with the current user.

**Note:** generally will want to only display entries from current season, using `/current` variant below.

### HTTP REQUEST
`GET /v2/accounts/:account_id/swim_meet_entries/`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only records that have been updated since this timestamp (UTC) in `ISO 8601` format.

### Response Data Fields

Field | Description
------|--------------
calendar_event_id | Id of event associated with this entry
type | Either "I" (Individual) or "R" (Relay)
user_id | Id of athlete associated with entry
seed_time_course | One of "S", "Y" or "L"
seed_time_int | Seed time in hundredths of seconds
is_exhibition | If true entry is exhibition entry
swim_meet_event_id | Id of associated swim meet event
event_number | (String) Number of event. Can be 0-99 plus one alpha character, e.g. "17B"
distance | Integer of distance of course
stroke_code | Numeric code identifying stroke for this event (see below)
event_sort_key | Lexically sortable key for event
event_age_group_name | Human-readable name of age-group for event
event_athlete_min_age | Minimum athlete age for event
event_athlete_max_age | Maximum athlete age for event
event_athlete_gender | Required athlete gender for event, one of 'M', 'F' or 'X'
heat | Assigned heat for this entry, if any
lane | Assigned lane for this entry, if any
is_swim_up | (boolean) If true, athlete is entered in event above actual age group

### Relay Entry Fields

Relay entries (identified by type = 'R') will have the additional fields

Field | Description
------|--------------
relay_team | A single alpha code identifying relay team, e.g. 'A'
relay_position | Integer between 1-8 identifying order in relay
relay_leg_stroke_code | Integer identifying the stroke for the assigned relay leg
is_alternate | (boolean) If true, athlete is entered as an alternate for the relay


## Entries for current season

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/swim_meet_entries/current"
```

Same as above `/v2/accounts/:account_id/swim_meet_entries` but limited to current season.

### HTTP Request
`GET /v2/accounts/:account_id/swim_meet_entries/current`

## Entries for calendar event

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events/66/swim_meet_entries"
```

> Example Response:

```json
[{
  "id": 91231,
  "created_at": "2012-04-12T13:26:47-04:00",
  "updated_at": "2012-04-12T13:26:47-04:00",
  "calendar_event_id": 66,
  "type": "I",
  "user_id": 2725,
  "seed_time_course": null,
  "seed_time_int": null,
  "is_exhibition": false,
  "swim_meet_event_id": 7901,
  "event_number": "13",
  "distance": 25,
  "stroke_code": 1,
  "event_sort_key": "013",
  "event_age_group_name": "Girls 6 & Under",
  "event_athlete_min_age": 0,
  "event_athlete_max_age": 6,
  "event_athlete_gender": "F",
  "heat": null,
  "lane": null,
  "is_swim_up": false
}, {
  "id": 1453760,
  "created_at": "2014-12-02T13:49:04-05:00",
  "updated_at": "2014-12-02T13:49:04-05:00",
  "calendar_event_id": 66,
  "type": "I",
  "user_id": 2725,
  "seed_time_course": null,
  "seed_time_int": null,
  "is_exhibition": false,
  "swim_meet_event_id": 7921,
  "event_number": "33",
  "distance": 25,
  "stroke_code": 2,
  "event_sort_key": "033",
  "event_age_group_name": "Girls 6 & Under",
  "event_athlete_min_age": 0,
  "event_athlete_max_age": 6,
  "event_athlete_gender": "F",
  "heat": null,
  "lane": null,
  "is_swim_up": false
}, {
  "id": 1466794,
  "created_at": "2015-02-03T20:46:58-05:00",
  "updated_at": "2015-02-03T20:46:58-05:00",
  "calendar_event_id": 66,
  "type": "I",
  "user_id": 2725,
  "seed_time_course": null,
  "seed_time_int": null,
  "is_exhibition": false,
  "swim_meet_event_id": 7945,
  "event_number": "57",
  "distance": 25,
  "stroke_code": 4,
  "event_sort_key": "057",
  "event_age_group_name": "Girls 6 & Under",
  "event_athlete_min_age": 0,
  "event_athlete_max_age": 6,
  "event_athlete_gender": "F",
  "heat": null,
  "lane": null,
  "is_swim_up": false
}]

```

### HTTP Request
`GET /v2/accounts/:account_id/calendar_events/:calendar_event_id/swim_meet_entries`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
calendar_event_id | int | Id of calendar event to scope query
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only that have been updated since this timestamp (UTC) in `ISO 8601` format.
