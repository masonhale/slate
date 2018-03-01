# RSVPs

## All RSVPs

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/rsvps"
```

> Example Response:

```json
[
 {
  "id": 8856,
  "type": "SwimMeetAthleteRsvp",
  "calendar_event_id": 66,
  "user_id": 2725,
  "is_attending": true,
  "relay_availability_code": 3,
  "created_at": "2012-04-20T12:33:16-04:00",
  "updated_at": "2012-04-20T12:33:16-04:00"
}, {
  "id": 535,
  "type": "SwimMeetAthleteRsvp",
  "calendar_event_id": 55,
  "user_id": 2724,
  "is_attending": true,
  "relay_availability_code": 2,
  "created_at": "2010-06-17T10:58:38-04:00",
  "updated_at": "2010-06-17T10:58:38-04:00"
}, {
  "id": 536,
  "type": "SwimMeetAthleteRsvp",
  "calendar_event_id": 55,
  "user_id": 2725,
  "is_attending": true,
  "relay_availability_code": 2,
  "created_at": "2010-06-17T10:58:38-04:00",
  "updated_at": "2010-06-17T10:58:38-04:00"
}
]
```

Returns **all** RVSPs for account/family. Generally this is more data than you really want.

### HTTP REQUEST
`GET /v2/accounts/:account_id/rsvps`

### URL Parameters
Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only assignments that have been updated since this timestamp (UTC) in `ISO 8601` format.



## RSVPs for current season

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/rsvps/current"
```

Retuns all RSVPs for account/family is current season.

### HTTP REQUEST
`GET /v2/accounts/:account_id/rsvps/current`


## RSVPs for calendar event

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/calendar_events/66/rsvps"
```

> Example Response:

```json
[{
  "id": 8856,
  "type": "SwimMeetAthleteRsvp",
  "calendar_event_id": 66,
  "user_id": 2725,
  "is_attending": true,
  "relay_availability_code": 3,
  "created_at": "2012-04-20T12:33:16-04:00",
  "updated_at": "2012-04-20T12:33:16-04:00"
}]
```

Returns RSVPs for account/family for specified event.

### HTTP REQUEST
`GET /v2/accounts/:account_id/calendar_events/:calendar_event_id/rsvps`

### URL Parameters

Parameter | Type | Description
----------|------|--------------
account_id | int | Id of account (team) to scope query
calendar_event_id | int | Id of calendar event to scope query
limit | int | Number of results to return
offset | int | Return results starting from this offset (enables paging)
updated_since | timestamp | Will return only assignments that have been updated since this timestamp (UTC) in `ISO 8601` format.

### Response Data Fields

Field | Type | Description
------|------|---------------
id | int | Unique ID of the RSVP record
type | string | Type of RSVP. Please see lookup codes.
calendar_event_id | int | Unique id of Calendar Event
user_id | int | Unique ID of user associated with this event.
is_attending | boolean | If true, indicates the user will be attending this event. If false, indicates will NOT be attending this event.
relay_availability_code | int | Indicates which relay events this athlete is available for. See Relay Available Codes under lookup codes for details.
created_at | timestamp | Date and time this RSVP record was created
updated_at | timestamp | Date and time this RSVP record was last updated.


