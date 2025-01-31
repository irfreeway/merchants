

# Balance

## Get Balance of all coins

```shell
curl --location --request GET '{MERCHANT_BASE_URL}/portfolio/assets/fiat-balance/' \
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





## Get Single Coin balance

```shell
curl --location --request GET '{MERCHANT_BASE_URL}/portfolio/assets/fiat-balance/?symbol=SILVER' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
{
    "balance": "200000",
    "blocked": "0"
},
```

This endpoint retrieves client balance of an specific coin.


### HTTP Request

`GET {MERCHANT_BASE_URL}portfolio/assets/fiat-balance/?symbol={COIN_SYMBOL}`
