

# Balance

## Get Balance

```shell
curl --location --request GET 'https://napi.zarpay24.com/api/v1/assets/fiat-balance/' \
--header 'Authorization: your_api_key_here' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "symbol": "IRT",
        "balance": "20109",
        "blocked": "12"
    },
    {
        "symbol": "GOLD",
        "balance": "2017.317",
        "blocked": "0"
    }
]
```

This endpoint retrieves your balance of each coin.
### HTTP Request

`GET https://napi.zarpay24.com/api/v1/assets/fiat-balance/`
