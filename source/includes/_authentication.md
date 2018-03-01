# Authentication

Authentication is handled via the [OAuth2 password](https://github.com/doorkeeper-gem/doorkeeper/wiki/Using-Resource-Owner-Password-Credentials-flow) credentials flow.

First, a username and password are submitted to an API endpoint, and if login is successful, an `access_token`is returned.

All subequent requests are authenticated via the `access_token` included in an `Authentication` header.

<aside class="warning">
Clients communication with the API should <strong>never</strong> store or log the username or password.
</aside>

## Token creation

User credentials are verified via a `/oauth/token` request. If successful, an `access_token` is returned which can be used to authenticate other API requests.

> To authorize, use this code:

```shell
curl -d "grant_type=password" \
  -d 'username=user@example.com' \
  -d 'password=examplepassword' \
  "https://api.swimtopia.com/oauth/token"
```

> Be sure to replace `user@example.com` and `examplepassword` with corresponding credentials for the user. Credentials must be URL-encoded, for example `+` must be encoded as `%2B`.


> Example response:

```json
{
 "access_token":"d3d535dedccc7f097d97068a791b464d827497bb3f689ac0c2aae41cd249af20",
 "token_type":"bearer",
 "expires_in":86400,
 "refresh_token":"b0eb82065341343a3f9bcafae32884c9668f385487226cb95246b4046c91a8db"
}
```

### HTTP Request

`POST /oauth/token`

### Parameters

### For "password" grant

Use this grant type if user has not authenticated before, or if attempt to authenticate using refresh token failed.

Parameter | Required | Description
----------|---------|------------
grant_type | true | Must equal "password"
username | true | A valid user email address
password | true | Valide user password

### For "refresh_token" grant

Use this grant type if the access token has expired (and thus token needs to be refreshed).

Parameter | Required | Description
----------|---------|------------
grant_type | true | Must equal "refresh_token"
refresh_token | true | A valid refresh token


### Return values
Field name | Type | Description
-----------|------|---------------
access_token | String | Token used to authenticate subsequent API calls via inclusion in `Authorization: Bearer` header.
token_type | String | Identifies type of authentication token. Should be `bearer`.
expires_in | Integer |
refresh_token | String |

SwimTopia expects the `access_token` to be included in all API requests in a HTTP Authorization header that looks like this:

`Authorization: Bearer d3d535dedcc`

<aside class="notice">
You must replace `d3d535dedccc` with the access_token returned from the `oauth/token` API call.
</aside>
