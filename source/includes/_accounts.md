
# Accounts

## All accounts

```shell
curl --header "Authorization: Bearer d3d535dedccc7f097d97068a791b464d827497bb3f689ac0c2aae41cd249af20" \
  "https://api.swimtopia.com/v2/accounts/"
```

> The above command returns JSON structured like this:

```json
[
 {
  "id":14,
  "organization_id":14,
  "organization_name":"Demo Dolphins",
  "organization_full_name":"Dolphins Swim Team",
  "organization_abbreviation":"DEMO",
  "organization_type":"ST-REC",
  "organization_site_url":"https://demo.swimtopia.com",
  "organization_logo_urls": {
    "large":"https://swimtopia.s3.amazonaws.com/14/logos/large/demo-dolphin.jpg?1354751015",
    "medium":"https://swimtopia.s3.amazonaws.com/14/logos/medium/demo-dolphin.jpg?1354751015",
    "small":"https://swimtopia.s3.amazonaws.com/14/logos/small/demo-dolphin.jpg?1354751015",
    "icon":"https://swimtopia.s3.amazonaws.com/14/logos/icon/demo-dolphin.jpg?1354751015"
  }
 }
]
```

This endpoint retrieves all team accounts associated with the authenticated user.
A single user login may belong to at most one "account" per organization. An account represents a single family (typically), and represents the group of people that should be billed as a group. A user can be connected to multiple teams through a single SwimTopia login.

### HTTP REQUEST
`GET /v2/accounts`

### URL Parameters

Parameter | Type | Description
----------|------|-----------
limit | int | Maximum number of accounts to return. Default/maximum = 100

### Result Data Fields

Field | Type | Description
------|------|------------
id | int | Unique id of account for this family & team. **Note** Our data model is transitioning to provide more clear separationg between families on the same team. In the interim, the id for the account may be the same as the organization, but the account_id should be used.
organization_id | int | Globally unique id for this organization.
organization_name | string | Name of organization / team. (16 characters max.)
organization_full_name | string | Full (long) name for organization. May be same as organization_name.
organization_abbreviation | string | 1-5 character abbreviation for this team.
organization_type | string | Identifies type of organization. Please see organization_type lookup codes.
organization_site_url | string | URL to website associated with this team.
organization_logo_urls | object | JS object/hash/dictionary mapping the keys: <ul><li>"icon" (48x48)</li><li>"small" (80x80)</li><li>"medium" (200x100)</li><li>"large" (300x150)</li></ul> to the associated logo image URLs in those sizes.


## Specific account

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14"
```

> Example response:

```json
{
  "id":14,
  "organization_id":14,
  "organization_name":"Demo Dolphins",
  "organization_full_name":"Dolphins Swim Team",
  "organization_abbreviation":"DEMO",
  "organization_type":"ST-REC",
  "organization_site_url":"https://demo.swimtopia.com",
  "organization_logo_urls": {
    "large":"https://swimtopia.s3.amazonaws.com/14/logos/large/demo-dolphin.jpg?1354751015",
    "medium":"https://swimtopia.s3.amazonaws.com/14/logos/medium/demo-dolphin.jpg?1354751015",
    "small":"https://swimtopia.s3.amazonaws.com/14/logos/small/demo-dolphin.jpg?1354751015",
    "icon":"https://swimtopia.s3.amazonaws.com/14/logos/icon/demo-dolphin.jpg?1354751015"
  }
}
```

Returns records for a single account, identified by :account_id

### HTTP Request
`GET /v2/accounts/:account_id`

### URL Parameters

Parameter | Description
--------- | -----------
account_id | The ID of the account to retrieve

### Result Data Fields

Field | Type | Description
------|------|------------
id | int | Unique id of account for this family & team.
organization_id | int | Globally unique id for this organization.
organization_name | string | Name of organization / team. (16 characters max.)
organization_full_name | string | Full (long) name for organization. May be same as organization_name.
organization_abbreviation | string | 1-5 character abbreviation for this team.
organization_type | string | Identifies type of organization. Please see organization_type lookup codes.
organization_site_url | string | URL to website associated with this team.
organization_logo_urls | object | JS object/hash/dictionary mapping the keys: <ul><li>"icon" (48x48)</li><li>"small" (80x80)</li><li>"medium" (200x100)</li><li>"large" (300x150)</li></ul> to the associated logo image URLs in those sizes.


