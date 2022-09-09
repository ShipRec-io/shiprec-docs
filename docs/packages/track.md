# Track Package

To track all the packages associated to your profile, first ensure you have created an account at [https://track.shiprec.io/packages](https://track.shiprec.io/packages). This route is not authenticated, allowing package receivers to view the current location of their package.

Make a `GET` request to:

> https://track.shiprec.io/api/packages/track?token=ADD_PACKAGE_TOKEN_HERE


**GET parameters**:
- `token` (required): You can get the link to this package by clicking on the `API` button on the [package UI](https://track.shiprec.io/packages).
- `interval_hours` (optional): Granularity for older location reports. The backend will return the most recent location for each time interval of `interval_hours` hours, starting from the most recent location report (default `24`, min `1`, max `7 * 24`)


Alternatively, see [List](/packages/list.md) and use the `tokenId` from the return body as a parameter.