# Device Metadata

To get specific device metadata for a tracker, first ensure you have created an account at [https://track.shiprec.io/packages](https://track.shiprec.io/packages). Please see the [Authentication](authentication.md) page to get an access token. Use this token to setup Bearer Token Authentication.

Make a `POST` request to:

> https://track.shiprec.io/api/packages/device?token=ADD_TOKEN_ID_HERE

If the succesful, the return value will be of type: `application/json`. Here is an example of the return body with only 1 package in the profile.

```json
{
    "battery": "Full (>80%)",
    "temp": "Ok (0°C - 40°C)",
}
```

The options for battery and temperature are:

| Battery Status          |
|-------------------------|
| Critically Low (<= 20%) |
| Low (20% - 50%)         |
| Medium (50% - 80%)      |
| Full (>80%)             |


| Temperature Status |
|--------------------|
| Low (<= 0°C)       |
| High (>= 40°C)     |
| Ok (0°C - 40°C)    |
| Unknown            |