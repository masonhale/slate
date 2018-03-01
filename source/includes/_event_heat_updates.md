# Event/Heat Updates

## Event/Heat update for calendar event

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events/66/event_heat"
```

> Example Response:

```json
{
  "data": {
    "channel_name": "585160851b26ad29170ea2f454df17f7166fcc08",
    "host_meet_start_date": "2011-06-18",
    "host_meet_end_date": "2011-06-18",
    "host_meet_name": "Dolphins vs. Gators",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "94C6457",
    "update_mode": 1,
    "sessions": [{
      "session_id": 66,
      "session_name": "Dolphins vs. Gators",
      "is_live": true,
      "update_status": "started",
      "start_at": "2011-06-18T08:30:00-05:00",
      "start_timestamp": 1308403800,
      "start_date": "2011-06-18",
      "start_time": "08:30:00",
      "updated_at": "2014-06-04T14:27:31-05:00",
      "schedule": {
        "version": 1,
        "start": 1308403800,
        "adjustments": []
      },
      "current": {
        "event_id": 182827,
        "heat": 4,
        "combined_from": [],
        "combined_into": {}
      },
      "next": {
        "event_id": null,
        "heat": null,
        "combined_from": [],
        "combined_into": {}
      }
    }]
  },
  "meta": {
    "ttl": 600
  }
}
```

### HTTP REQUEST
`GET /v2/accounts/:account_id/calendar_events/:calendar_event_id/event_heat`

OR
`GET /v2/accounts/:account_id/sessions/:sesion_id/event_heat`


### Result Data Fields

Field | type | Description
------|------|--------------
is_live | boolean | If true, heat/event updates are begin published
current.event_id | int | ID of current/last event published
current.heat | int | Current/last event number published
next.event_id | int | ID of event after current/last event published
next.heat | int | Current/last event number published
updated_at | timestamp | Timestamp of last event/heat update
channel_name | string | Unique/random channel name to subscribe to push updates for this meet. (Via pusher.io)
host_meet_date | date |
host_meet_name | string | Name of hosting meet
host_team_name | string | Name of hosting team at meet
visitor_code | string | Unique code for updating to event/heat for this meet
update_mode | int | Either 0 for 'Host' mode or 1 for 'Visitor' mode


## Update Event/Heat

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   --header "Content-Type: application/json" \
   -X POST \
   -d '{"is_enabled": true, "event":"2", "heat":"3"}' \
   "https://api.swimtopia.com/v2/accounts/:account_id/sessions/:session_id/event_heat_update"
```


> Example Response:

```json
{
  "data": {
    "calendar_event_id": 66,
    "channel_name": "585160851b26ad29170ea2f454df17f7166fcc08",
    "host_meet_start_date": "2011-06-18",
    "host_meet_end_date": "2011-06-18",
    "host_meet_name": "Dolphins vs. Gators",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "94C6457",
    "update_mode": 1,
    "sessions": [{
      "session_id": 66,
      "session_name": "Dolphins vs. Gators",
      "is_live": true,
      "update_status": "started",
      "start_at": "2011-06-18T08:30:00-05:00",
      "start_timestamp": 1308403800,
      "start_date": "2011-06-18",
      "start_time": "08:30:00",
      "updated_at": "2014-06-04T14:27:31-05:00",
      "schedule": {
        "version": 1,
        "start": 1308403800,
        "adjustments": []
      },
      "current": {
        "event_id": 182827,
        "heat": 4,
        "combined_into": [],
        "combined_from": []
      },
      "next": {
        "event_id": null,
        "heat": null,
        "combined_from": [],
        "combined_into": {}
      }
    }]
  },
  "meta": {
    "ttl": 600
  }
}
```

Allows authenticated user (with special permissions) to update current event/heat information for specified SESSION.


### HTTP REQUEST
`POST /v2/accounts/:account_id/sessions/:session_id/event_heat_update`

`PUT /v2/accounts/:account_id/sessions/:session_id/event_heat_update`


### Parameters

Parameter | type | Description
----------|------|-------------
event | string  | The current event number (e.g. "13A")
heat  | integer | The current heat number (e.g. 2)
is_enabled | boolean | If true, then event/heat updates are "in progress"


## Update Event/Heat Subscription

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   --header "Content-Type: application/json" \
   -X POST \
   -d '{"update_mode": 1, "visitor_code":"V83JMK"}' \
   "https://api.swimtopia.com/v2/accounts/:account_id/calendar_events/:calendar_event_id/event_heat_subscription"
```

> Example Response:

```json
{
  "data": {
    "calendar_event_id": 66,
    "channel_name": "585160851b26ad29170ea2f454df17f7166fcc08",
    "host_meet_start_date": "2011-06-18",
    "host_meet_end_date": "2011-06-18",
    "host_meet_name": "Dolphins vs. Gators",
    "host_team_name": "Dolphins Swim Team",
    "visitor_code": "94C6457",
    "update_mode": 1,
    "sessions": [{
      "session_id": 66,
      "session_name": "Dolphins vs. Gators",
      "is_live": true,
      "update_status": "started",
      "start_at": "2011-06-18T08:30:00-05:00",
      "start_timestamp": 1308403800,
      "start_date": "2011-06-18",
      "start_time": "08:30:00",
      "updated_at": "2014-06-04T14:27:31-05:00",
      "schedule": {
        "version": 1,
        "start": 1308403800,
        "adjustments": []
      },
      "current": {
        "event_id": 182827,
        "heat": 4,
        "combined_into": [],
        "combined_from": []
      },
      "next": {
        "event_id": null,
        "heat": null,
        "combined_from": [],
        "combined_into": []
      }
    }]
  },
  "meta": {
    "ttl": 600
  }
}
```

Allows authenticated user (with special permissions) to update current event/heat subscription settings such as publisher/subscriber mode and the subscribed meet code for the specified meet.

### Parameters

Parameter | type | Description
----------|------|-------------
visitor_code | string | Subscriber code to subscribe the specified meet to another meet for updates.
update_mode | int | 0 = Publisher (meet host), 1 = Subscriber (visitor)


## Event/Heat (guest access)

```shell
curl  "https://api.swimtopia.com/v2/event_heat_updates/94C6457"
```

> Example Response:

```json
{
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
```

Note: no authentication is required for this end point.
This is meant to enable a "guest" user without a SwimTopia
account to receive current event/heat updates for a selected meet.

### HTTP Request
`GET /v2/event_heat_updates/:visitor_code`

### URL Parameters
Parameter | type | Description
----------|-------|-------------
visitor_code | string | A short random code that uniquely identifies a swim meet, e.g. "94C6457"



