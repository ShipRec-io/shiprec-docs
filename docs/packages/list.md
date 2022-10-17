# List Packages

To list all the packages associated to your profile, first ensure you have created an account at [https://track.shiprec.io/packages](https://track.shiprec.io/packages). Please see the [Authentication](authentication.md) page to get an access token. Use this token to setup Bearer Token Authentication.

Make a `POST` request to:

> https://track.shiprec.io/api/packages/list?offset=0&limit=10

By default, the limit and offset are set at 10 and 0. The response header will include a key `x-api-total-records`, which has the total count of records available to be queried. 

If the succesful, the return value will be of type: `application/json`. Here is an example of the return body with only 1 package in the profile.

```json
[
    {
        "tokenId": "1234123412341234", // ID used for unique journey created
        "packageId": "1234-1234-1234-1234-1234", // UUID for package added through UI or API
        "deleted": false, // boolean used for soft deletes
        "deviceId": "ABC12345", // MAC Address for device
        "userId": "test@shiprec.io", // User who created the package record
        "notes": "", // Any notes associated with the package, edited in the UI
        "created": "2022-08-30T11:10:13.768Z", // Timestamp for when the record was created
        "address": "", // Address associated with the package, edited in the UI
        "email": "", // Email for the individual receiving the package, edited in the UI
        "name": "TESTING", // Name for the package
        "location": { // last position for the device
            "lat": 10.0,
            "long": -10.0,
            "timestamp": 1662520862
        },
        "status": 5 // Encoded temperature and battery for device
    }
]
```