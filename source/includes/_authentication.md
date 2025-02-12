
# Authentication

ZarPay24 expects for the access token to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer client_access_token`

<aside class="notice">
You must replace <code>client_access_token</code> with client access token.
</aside>



## Refresh Token

```shell
curl --location --request GET '{MERCHANT_BASE_URL}/users/refresh/' \
--header 'Authorization: Bearer client_refresh_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
{
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNzM5OTU0NDk1LCJpYXQiOjE3MzkzNDk2OTUsImp0aSI6IjhhODM4ZWZlZDNiYzRlMjQ5ZjZjNjU3ZWQyY2VhMGU5IiwidXNlcl9pZCI6MTUzLCJtZXJjaGFudF9pZCI6MTR9.bxQ_RYaerOk1mV5G14NHKjaJD944RPXpWH3vE0iEDQY"
}
```

Use this endpoint to generate new access_token for your client based on client_refresh_token you've been provided [here](https://merchants.zarpay24.com/merchants.html#verify-otp-get-client-access_token).


<aside class="notice">
Make sure you pass <code>client_refresh_token</code> as authorization header in this endpoint.
</aside>


### HTTP Request

`GET {MERCHANT_BASE_URL}/users/refresh/`