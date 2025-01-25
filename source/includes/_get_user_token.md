# User Sign-in

## Login/Register client (send OTP)



```shell
curl --location '{API_BASE_URL}/users/sign-up/send-otp/' \
--header 'Authorization: MERCHANT_API_KEY' \
--header 'Content-Type: application/json' \
--data '{
    "phone_number": "+989124136159",
}'
```

> The above command returns JSON structured like this:

```json
{
    "data": "verification code sent."
}
```

This endpoint allows you ti submit client personal-info and proceed KYC.

### HTTP Request

`POST {API_BASE_URL}/users/sign-up/send-otp/`


### Request Body

Parameter | Description
--------- | -----------
phone_number | client phone number startswith: +98



## Verify OTP (get client access_token)


```shell
curl --location '{API_BASE_URL}/users/sign-up/verify-otp/' \
--header 'Authorization: MERCHANT_API_KEY' \
--header 'Content-Type: application/json' \
--data '{
    "phone_number": "+989124136159",
    "code": "25895"
}'
```

> The above command returns JSON structured like this:

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SdvlG5K6QK8IslONhwBbEK7l5QzYO09IEcGdFd7k8yQ",
  "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SdvlG5K6QK8IslONhwBbEK7l5QzYO09IEcGdFd7k8yQ"
}
```

This endpoint allows you ti submit client personal-info and proceed KYC.

### HTTP Request

`POST {API_BASE_URL}/users/sign-up/verify-otp/`


### Request Body

Parameter | Description
--------- | -----------
phone_number | client phone number startswith: +98
code | OTP sent to client phone number

