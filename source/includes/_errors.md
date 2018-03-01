# Errors

> Error responses will include a JSON object with `error` and `error_description` (human readable) fields.

```json
{
"error":"invalid_resource_owner",
"error_description":"The provided resource owner credentials are not valid, or resource owner cannot be found"
}
```
The SwimTopia API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Invalid request
401 | Unauthorized -- Missing or invalid authentication token
403 | Forbidden -- Authenticated user not authorized to view requested resource
404 | Not Found -- Resource not found
405 | Method Not Allowed -- Invalid HTTP method for request
406 | Not Acceptable -- Invalid format requested (not JSON)
410 | Gone -- Resource has been removed from our servers
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.

