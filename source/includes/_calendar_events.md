
# Calendar Events

## All calendar events

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events"
```

> Example Response:

```json
[
 {
  "id": 55,
  "type": "SwimMeet",
  "name": "Championship Meet",
  "description": "",
  "created_at": "2010-05-09T15:14:04-05:00",
  "updated_at": "2015-02-11T19:58:39-06:00",
  "season_name": "2011",
  "start_at": "2011-07-02T09:00:00-05:00",
  "start_timestamp": 1309615200,
  "start_date": "2011-07-02",
  "start_time": "09:00:00",
  "end_at": "2011-07-02T23:59:59-05:00",
  "end_timestamp": 1309669199,
  "end_date": "2011-07-02",
  "end_time": null,
  "time_zone_abbreviation": "CDT",
  "time_zone_identifier": "America/Chicago",
  "time_zone_offset": "-05:00",
  "location": "",
  "altitude": null,
  "is_job_signup_enabled": true,
  "job_signup_status": "open",
  "is_online_meet_entry_enabled": true,
  "online_meet_entry_status": "open",
  "is_home_meet": false,
  "is_unofficial": false,
  "age_up_date": "2011-06-01",
  "swim_course": "Y",
  "commitment_summaries": [{
    "commitment_counts": [{
      "type": "SwimMeetAthleteRsvp",
      "count": 1
    }, {
      "type": "SwimMeetRelayEntry",
      "count": 1
    }, {
      "type": "SwimMeetIndividualEntry",
      "count": 2
    }],
    "user_id": 2724
  }, {
    "commitment_counts": [{
      "type": "SwimMeetAthleteRsvp",
      "count": 1
    }, {
      "type": "SwimMeetRelayEntry",
      "count": 2
    }, {
      "type": "SwimMeetIndividualEntry",
      "count": 3
    }],
    "user_id": 2725
  }, {
    "commitment_counts": [{
      "type": "CalendarEventJobShiftAssignment",
      "count": 3
    }],
    "user_id": 2726
  }, {
    "commitment_counts": [{
      "type": "CalendarEventJobShiftAssignment",
      "count": 4
    }],
    "user_id": 2723
  }],
  "is_event_heat_updater": false,
  "event_heat_visitor_code": "67KMSL9",
  "event_heat_update": {
    "is_enabled": false,
    "event": null,
    "heat": null,
    "updated_at": null,
    "channel_name": "7b6c35dfb3a3f77c32e5d27413e980542a1b18bb",
    "host_meet_date": "2011-07-02",
    "host_meet_name": "Championship Meet",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "67KMSL9",
    "update_mode": 0
  }
}, {
  "id": 955,
  "type": "SwimMeet",
  "name": "Dolphins vs. Hammers",
  "description": "<p>\r\n\t  Epic battle between mammals and fish!</p>",
  "created_at": "2011-04-08T16:30:51-05:00",
  "updated_at": "2015-02-04T14:08:30-06:00",
  "season_name": "2011",
  "start_at": "2011-06-25T08:30:00-05:00",
  "start_timestamp": 1309008600,
  "start_date": "2011-06-25",
  "start_time": "08:30:00",
  "end_at": "2011-06-25T23:59:59-05:00",
  "end_timestamp": 1309064399,
  "end_date": "2011-06-25",
  "end_time": null,
  "time_zone_abbreviation": "CDT",
  "time_zone_identifier": "America/Chicago",
  "time_zone_offset": "-05:00",
  "location": "Hammers Pool",
  "altitude": null,
  "is_job_signup_enabled": true,
  "job_signup_status": "open",
  "is_online_meet_entry_enabled": true,
  "online_meet_entry_status": "open",
  "is_home_meet": false,
  "is_unofficial": false,
  "age_up_date": "2011-06-01",
  "swim_course": "S",
  "commitment_summaries": [{
    "commitment_counts": [{
      "type": "CalendarEventJobShiftAssignment",
      "count": 1
    }],
    "user_id": 2723
  }],
  "is_event_heat_updater": false,
  "event_heat_visitor_code": "MQY2WB4",
  "event_heat_update": {
    "is_enabled": false,
    "event": null,
    "heat": null,
    "updated_at": null,
    "channel_name": "48cea5db39499ed4a2477f3341494d027fe91123",
    "host_meet_date": "2011-06-25",
    "host_meet_name": "Dolphins vs. Hammers",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "MQY2WB4",
    "update_mode": 0
  }
}, {
  "id": 66,
  "type": "SwimMeet",
  "name": "Dolphins vs. Gators",
  "description": "",
  "created_at": "2011-04-08T16:30:51-05:00",
  "updated_at": "2015-02-04T14:07:22-06:00",
  "season_name": "2011",
  "start_at": "2011-06-18T08:30:00-05:00",
  "start_timestamp": 1308403800,
  "start_date": "2011-06-18",
  "start_time": "08:30:00",
  "end_at": "2011-06-18T23:59:59-05:00",
  "end_timestamp": 1308459599,
  "end_date": "2011-06-18",
  "end_time": null,
  "time_zone_abbreviation": "CDT",
  "time_zone_identifier": "America/Chicago",
  "time_zone_offset": "-05:00",
  "location": "Gators Pool",
  "altitude": null,
  "is_job_signup_enabled": true,
  "job_signup_status": "open",
  "is_online_meet_entry_enabled": true,
  "online_meet_entry_status": "open",
  "is_home_meet": false,
  "is_unofficial": false,
  "age_up_date": "2011-06-01",
  "swim_course": "S",
  "commitment_summaries": [{
    "commitment_counts": [{
      "type": "SwimMeetAthleteRsvp",
      "count": 1
    }, {
      "type": "SwimMeetRelayEntry",
      "count": 1
    }, {
      "type": "SwimMeetIndividualEntry",
      "count": 3
    }],
    "user_id": 2725
  }, {
    "commitment_counts": [{
      "type": "SwimMeetRelayEntry",
      "count": 2
    }],
    "user_id": 2724
  }, {
    "commitment_counts": [{
      "type": "CalendarEventJobShiftAssignment",
      "count": 1
    }],
    "user_id": 2726
  }],
  "is_event_heat_updater": false,
  "event_heat_visitor_code": "94C6457",
  "event_heat_update": {
    "is_enabled": true,
    "event": "2C",
    "heat": 4,
    "updated_at": "2014-06-04T14:27:31-05:00",
    "channel_name": "df5795950a3215a55cf7267679ce8cb62b653d56",
    "host_meet_date": "2011-06-18",
    "host_meet_name": "Dolphins vs. Gators",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "94C6457",
    "update_mode": 1
  }
}, {
  "id": 2294,
  "type": "GenericEvent",
  "name": "Ice Cream Social",
  "description": null,
  "created_at": "2012-04-23T16:54:01-05:00",
  "updated_at": "2015-02-04T14:05:56-06:00",
  "season_name": "2011",
  "start_at": "2011-06-15T19:00:00-05:00",
  "start_timestamp": 1308182400,
  "start_date": "2011-06-15",
  "start_time": "19:00:00",
  "end_at": "2011-06-15T23:59:59-05:00",
  "end_timestamp": 1308200399,
  "end_date": "2011-06-15",
  "end_time": null,
  "time_zone_abbreviation": "CDT",
  "time_zone_identifier": "America/Chicago",
  "time_zone_offset": "-05:00",
  "location": "Club House",
  "is_job_signup_enabled": true,
  "job_signup_status": "open",
  "commitment_summaries": []
 }
]
```

Returns all calendar events for a given account.
**NOTE:** Generally you do *not* want all calendar data going back in time.
Thus probably should not use this API call.

### HTTP REQUEST
`GET /v2/accounts/:account_id/calendar_events`

### URL Parameters

Parameter | type | Description
----------|------|-------------
before | timestamp  | Returns events that begin before the specified date/time
after  | timestamp | Returns events that begin after the specified date/time
limit | int | Number of results to return. Default/maximum = 100.
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only results that have been updated since this timestamp (UTC) in `ISO 8601` format.

### Response Data Fields

Field | Type | Description
------|------|---------------
id | int | Unique ID of calendar event
type | string | Type of calendar event. See Calendar Event Type lookup codes.
name | string | Name of event
description | string | Description of event, may include HTML code.
created_at | timestamp | Date and time this record was created.
updated_at | timestamp | Date and time this record as last updated.
season_name | string | The name of the season associated with this event.
start_at | timestamp | Date and time of the start of this event.
start_timestamp | int | Unix timestamp for start date and time of event.
start_date | date | Date of the start of the event.
start_time | time | Time the event starts. May be null if event is "all day"
end_at | timestamp | Date and time of the end of this event. If end time is not specified, it is normalized to 23:59:59
end_timestamp | int | Unix timestamp for end date and time of event
end_date | date | Date of start of event
end_time | time | Time the event ends. May be null if end time is unspecified (common for swim meets).
time_zone_abbreviation | string | Standard abbreviation for time zone used for specified start/end times and timestamps, e.g. "CDT"
time_zone_identifier | string | Standard unix time zone identifier, e.g. "America/Chicago"
time_zone_offset | string | time zone offset from UTC in hours and minutes, e.g. "-5:00"
location | string | Name of location for event
altitude | int | Altitude in feet of event if specified. Can be null. (This is necessary for swim meet at high altitude).
is_job_signup_enabled | boolean | If true, then job signup is available for this event. It may or may not be open at this time.
job_signup_status | string | Indicates current status for job signup for this event. Can be one of "Pending", "Open" or "Closed".
is_online_meet_entry_enabled | boolean | If true, indicates online meet entry feature is enabled for this swim meet.
online_meet_entry_status | string | Indicates current status for swim meet entries for this event. Can be one of "Pending", "Open" or "Closed".
is_home_meet | boolean | If true, this swim meet is a home meet.
is_unofficial | boolean | If true, this meet is considered "unofficial" -- the times associated with this meet may not be considered valid for subsequent meets.
age_up_date | date | The date to be used to calculate athlete competition ages for this meet.
swim_course | string | Indicates the swim course associated with this meet. One of "S", "Y" or "L". See lookup codes for details.
commitment_summaries | Array | An array of JSON objects summarizing the commitments for the current users family in this event. Each object contains two values: <ul><li>`user_id` - The id of the user (a family member) who has some commitment associated with this event. In general, the avatars for any user_id's listed in the commitment summaries should be shown in the interface</li><li>`commitment_counts` -- An arry of JSON objects indicating the `count` of each `type` of commitment a user has for this specific event. See commitment types under lookup codes for details.</li></ul>
is_event_heat_updater | boolean | If true, the current user is authorized to update the event and heat information for this swim meet.
event_heat_visitor_code | string | Unique identifier that can be used to 'subscribe' to event/heat updates for this event. (Swim Meets only)
event_heat_update | object | An object describing current/latest event/heat data for this meet. See Event Heat Update for details.



## Calendar events for current season

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events/current"
```

Returns only calendar events for the current season for the given account.

### HTTP REQUEST
`GET /v2/accounts/:account_id/calendar_events/current`


## Specific calendar event

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events/66"
```

> Example Response:

```json
{
  "id": 66,
  "type": "SwimMeet",
  "name": "Dolphins vs. Gators",
  "description": "",
  "created_at": "2011-04-08T17:30:51-04:00",
  "updated_at": "2015-02-04T15:07:22-05:00",
  "season_name": "2011",
  "start_at": "2011-06-18T08:30:00-05:00",
  "start_timestamp": 1308403800,
  "start_date": "2011-06-18",
  "start_time": "08:30:00",
  "end_at": "2011-06-18T23:59:59-05:00",
  "end_timestamp": 1308459599,
  "end_date": "2011-06-18",
  "end_time": null,
  "time_zone_abbreviation": "CDT",
  "time_zone_identifier": "America/Chicago",
  "time_zone_offset": "-05:00",
  "location": "Gators Pool",
  "altitude": null,
  "is_job_signup_enabled": true,
  "job_signup_status": "open",
  "is_online_meet_entry_enabled": true,
  "online_meet_entry_status": "open",
  "is_home_meet": false,
  "is_unofficial": false,
  "age_up_date": "2011-06-01",
  "swim_course": "S",
  "commitment_summaries": [{
    "commitment_counts": [{
      "type": "SwimMeetAthleteRsvp",
      "count": 1
    }, {
      "type": "SwimMeetRelayEntry",
      "count": 1
    }, {
      "type": "SwimMeetIndividualEntry",
      "count": 3
    }],
    "user_id": 2725
  }, {
    "commitment_counts": [{
      "type": "SwimMeetRelayEntry",
      "count": 2
    }],
    "user_id": 2724
  }, {
    "commitment_counts": [{
      "type": "CalendarEventJobShiftAssignment",
      "count": 1
    }],
    "user_id": 2726
  }],
  "is_event_heat_updater": false,
  "event_heat_visitor_code": "94C6457",
  "event_heat_update": {
    "is_enabled": true,
    "event": "2C",
    "heat": 4,
    "updated_at": "2014-06-04T15:27:31-04:00",
    "channel_name": "df5795950a3215a55cf7267679ce8cb62b653d56",
    "host_meet_date": "2011-06-18",
    "host_meet_name": "Dolphins vs. Gators",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "94C6457",
    "update_mode": 1
  }
}
```

Returns data for selected calendar event

### HTTP REQUEST
`GET /v2/accounts/:account_id/calendar_events/:calendar_event_id`

