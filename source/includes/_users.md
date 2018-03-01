
# Users

## All users (in family)

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/users"
```

> Example Response:

```json
[{
  "id": 2723,
  "first_name": "Lorri",
  "last_name": "Ault",
  "middle_name": null,
  "email": "3YJ@city.zz.moc",
  "gender": null,
  "preferred_first_name": null,
  "born_on": null,
  "competition_age": null,
  "age_up_on": null,
  "registration_number": null,
  "record_type": "User",
  "group_labels": [{
    "name": "Parent",
    "type": "parent"
  }, {
    "name": "Banquet Committee",
    "type": "role",
    "points": 5.0
  }],
  "has_swim_history": false
}, {
  "id": 2726,
  "first_name": "Wayne",
  "last_name": "Ault",
  "middle_name": null,
  "email": "masonhale+wayneault@gmail.com",
  "gender": null,
  "preferred_first_name": null,
  "born_on": null,
  "competition_age": null,
  "age_up_on": null,
  "registration_number": null,
  "record_type": "User",
  "group_labels": [{
    "name": "Parent",
    "type": "parent"
  }],
  "has_swim_history": false
}, {
  "id": 2724,
  "first_name": "June",
  "last_name": "Ault",
  "middle_name": null,
  "email": null,
  "gender": "F",
  "preferred_first_name": null,
  "born_on": "2003-04-07",
  "competition_age": 11,
  "age_up_on": "2014-05-01",
  "registration_number": null,
  "record_type": "User",
  "group_labels": [{
    "name": "Girls 7-8",
    "type": "athlete"
  }],
  "has_swim_history": true
}, {
  "id": 2725,
  "first_name": "Matilde",
  "last_name": "Ault",
  "middle_name": null,
  "email": null,
  "gender": "F",
  "preferred_first_name": null,
  "born_on": "2005-10-09",
  "registration_number": null,
  "record_type": "User",
  "group_labels": [{
    "name": "Girls 6 & Under",
    "type": "athlete"
  }],
  "has_swim_history": true
}

```

### HTTP Request
`GET /v2/accounts/:account_id/users`

### Response Data Fields

Field | Type | Description
------|------|---------------
id | int | Unique ID of the user
first_name | string | First name of the user
last_name | string | Last name of the user
middle_name | string | Middle name (or initial) of the user
email | string | Email address associated with user
gender | string | The gender of the user, if known. Usually only set for athletes. See Gender under lookup codes.
preferred_first_name | string | The preferred first name / nickname to use for this user.
born_on | date | The date of birth for this user, if known.
competition_age | int | Pre-computed competiton age for the athlete, based on age-up-on date.
age_up_on | date | The date used to calculated competition age of the athlete.
registration_number | string |
record_type | string | // TODO -- normalized this before making API public
group_labels | Array | TODO
has_swim_history | boolean | If true, inidicates this user has swim history.


## Current user (self)

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/users/self"
```

> Example Response:

```json
{
  "id": 2726,
  "first_name": "Wayne",
  "last_name": "Ault",
  "middle_name": null,
  "email": "masonhale+wayneault@gmail.com",
  "gender": null,
  "preferred_first_name": null,
  "born_on": null,
  "competition_age": null,
  "age_up_on": null,
  "registration_number": null,
  "record_type": "User",
  "group_labels": [{
    "name": "Parent",
    "type": "parent"
  }],
  "has_swim_history": false
}
```

### HTTP Request
`GET /v2/accounts/:account_id/users/self`


## Specific user

```shell
curl --header "Authorization: Bearer d3d535dedccc7f" \
   "https://api.swimtopia.com/v2/accounts/14/users/2724"
```

> Example Response:

```json
{
  "id": 2724,
  "first_name": "June",
  "last_name": "Ault",
  "middle_name": null,
  "email": null,
  "gender": "F",
  "preferred_first_name": null,
  "born_on": "2003-04-07",
  "competition_age": 11,
  "age_up_on": "2014-05-01",
  "registration_number": null,
  "record_type": "User",
  "group_labels": [{
    "name": "Girls 7-8",
    "type": "athlete"
  }],
  "has_swim_history": true
}
```

### HTTP Request
`GET /v2/accounts/:account_id/users/:user_id`


