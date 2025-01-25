# Cards

## Get Verified Cards 


```shell
curl --location --request GET '{MERCHANT_BASE_URL}/users/verified-cards/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "number": "6219861929783016",
        "id": 4,
        "state": "DN",
        "iban": "IR720560611828005347224101",
        "bank_name": "سامان",
        "bank_code": "056"
    },
    {
        "number": "5859831216890185",
        "id": 5,
        "state": "DN",
        "iban": "IR900180000000136234069882",
        "bank_name": "تجارت",
        "bank_code": "018"
    }
]
```

This endpoint retrieves list of client verified cards which will be used for cash out

### HTTP Request

`GET {MERCHANT_BASE_URL}/users/verified-cards/`



## Add new card


```shell
curl --location '{MERCHANT_BASE_URL}/users/cards/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "number": "0010859684",
}'
```

> The above command returns JSON structured like this:

```json
{
    "number":"6219861076488716",
    "id":22,
    "state":"DN",
    "iban":"IR350560213780004605786001",
    "bank_name":"سامان",
    "bank_code":"056"
}
```

This endpoint allows you ti submit client personal-info and proceed KYC.

### HTTP Request

`POST {MERCHANT_BASE_URL}/users/cards/`


### Request Body

Parameter | Description
--------- | -----------
number | 10 digits card number.

