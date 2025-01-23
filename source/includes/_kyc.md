# KYC

## Get Profile(include KYC state)


```shell
curl --location --request GET '{BASE_URL}/users/profile/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
{
    "_id": "200002",
    "full_name": "ایمان اشراقی",
    "email": "",
    "phone_number": "+98912****873",
    "phone_number_str": "0912****873",
    "invite_code": "XGvy",
    "national_number": "******1234",
    "is_blocked": false,
    "is_banned": false,
    "first_name": "ایمان",
    "last_name": "اشراقی",
    "kyc": "DN",
}
```

This endpoint retrieves user profile detail which includes KYC state.


### HTTP Request

`GET {BASE_URL}/users/profile/`



## Proceed KYC (register personal info)


```shell
curl --location '{BASE_URL}/users/personal-info/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "national_number": "0010859684",
    "birth_date": "1998-01-12"
}'
```

> The above command returns JSON structured like this:

```json
{
    "_id": "200002",
    "full_name": "ایمان اشراقی",
    "email": "",
    "phone_number": "+98912****873",
    "phone_number_str": "0912****873",
    "invite_code": "XGvy",
    "national_number": "******1234",
    "is_blocked": false,
    "is_banned": false,
    "first_name": "ایمان",
    "last_name": "اشراقی",
    "kyc": "DN",
}
```

This endpoint allows you ti submit client personal-info and proceed KYC.

### HTTP Request

`GET {BASE_URL}/users/personal-info/`


### Request Body

Parameter | Description
--------- | -----------
national_number | 10 numbers length.
birth_date | The gregorian birth_date in %Y-%M-%D format.

