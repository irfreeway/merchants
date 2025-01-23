

# Balance

## Get Balance

```shell
curl --location --request GET '{BASE_URL}/assets/fiat-balance/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "symbol": "IRT",
        "balance": "200000",
        "blocked": "0"
    },
    {
        "symbol": "GOLD",
        "balance": "25.3157",
        "blocked": "0"
    }
]
```

This endpoint retrieves client balance of each asset.

### HTTP Request

`GET {BASE_URL}/assets/fiat-balance/`
