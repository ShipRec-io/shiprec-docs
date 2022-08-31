# Authentication

Authentication for an API is done through the Resource Owner Password Flow. To get started, please create a [ShipRec account](https://shiprec.io). Login using a username and password. Reach out to <a href="mailto:hello@shiprec.io" target="_blank">hello@shiprec.io</a> to get whitelisted for API access. 

## Generate an Access Token

To generate an access token needed to authenticate with the API, make a post request to the route:

> https://auth.shiprec.io/oauth/token

Set the Content-Type header to: `application/x-www-form-urlencoded`

Then, use the table below to generate the body of the request

| Key           | Value                  | Description                                                                                               |
|---------------|------------------------|-----------------------------------------------------------------------------------------------------------|
| grant_type    | password               | Let identity provider know which type of flow to use (Resource Owner Password Flow)                       |
| client_id     | INSERT_CLIENT_ID       | Reach out to <a href="mailto:hello@shiprec.io" target="_blank">hello@shiprec.io</a> for the Client ID     |
| client_secret | INSERT_CLIENT_SECRET   | Reach out to <a href="mailto:hello@shiprec.io" target="_blank">hello@shiprec.io</a> for the Client Secret |
| scope         | write:packages openid  | Check the user is part of the write:packages scope and include user id information in return payload      |
| username      | INSERT_USERNAME        | This is the username used to login to the shiprec.io UI.                                                  |
| password      | INSERT_PASSWORD        | This is the password used to login to the shiprec.io UI.                                                  |