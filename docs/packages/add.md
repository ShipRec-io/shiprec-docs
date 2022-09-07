# Add Package

To add a new package to begin tracking, first scan the QR code on the tracker to get the Mac Address for the tracking device.

Check that you have created an account at [https://track.shiprec.io/packages](https://track.shiprec.io/packages). Please see the [Authentication](authentication.md) page to get an access token. Use this token to setup Bearer Token Authentication.

Make a `POST` request to:

> https://track.shiprec.io/api/packages/new

Set the header Content-Type to: `application/json`

In the body, have the following values:

| Key                | Value                                  | Description                                                          |
|--------------------|----------------------------------------|----------------------------------------------------------------------|
| deviceId           | Mac Address                            | The Mac Address is received from the QR code on the tracking device. |
| name (optional)    | Jonny Test                             | Name for the individual receiving the package                        |
| email (optional)   | j.test@test.com                        | Email for individual receiving the package                           |
| address (optional) | 101010 Test Dr, Test City, NY 10101010 | Mailing address for package                                          |