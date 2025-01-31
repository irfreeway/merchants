

# Balance

## Get Balance

```shell
curl --location --request GET '{MERCHANT_BASE_URL}/assets/fiat-balance/' \
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

<aside class="notice">
for recently joined clients there is no record of active balance and the output of this endpoint would be []. make sure you handle it correctly.
</aside>


### HTTP Request

`GET {MERCHANT_BASE_URL}/assets/fiat-balance/`
