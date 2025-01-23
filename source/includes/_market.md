# Market

## Get Coins Data (Pricing)


```shell
curl --location --request GET '{BASE_URL}/market/coins/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": 2,
        "symbol": "GOLD",
        "persian_name": "طلا آبشده",
        "buy_active": true,
        "sell_active": true,
        "max_order_qty": "100",
        "buy_price": "5531187",
        "sell_price": "5519645",
        "fee_percentage": "1.00",
        "unit": "گرم",
        "decimal_places": 4
    },
    {
        "id": 4,
        "symbol": "SILVER",
        "persian_name": "نقره",
        "buy_active": true,
        "sell_active": true,
        "max_order_qty": "250",
        "buy_price": "102000",
        "sell_price": "101000",
        "fee_percentage": "2.00",
        "unit": "گرم",
        "decimal_places": 0
    },
]
```

This endpoint retrieves detailed information about a specific coin.

### HTTP Request

`GET {BASE_URL}/market/coins/`



## Buy Coin with Quantity


```shell
curl --location '{BASE_URL}/market/buy/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "coin_id":1,
    "quantity":"12.00"
}'
```

> The above command returns JSON structured like this:

```json
{
    "id": 291,
    "coin": 1,
    "quantity": "2.0000",
    "quote": "8000000",
    "quote_with_fee": "8080000",
    "fee": 80000.0,
    "coin_price": "1000.00",
    "side": "buy",
    "state": "done",
    "request_type": 2,
    "source": "merchant",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint allows you to purchase a coin by specifying the desired quantity.

### HTTP Request

`GET {BASE_URL}/market/buy/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to buy.
quantity | The quantity of coin to buy.




## Sell Coin with Quantity


```shell
curl --location '{BASE_URL}/market/sell/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "coin_id":1,
    "quantity":"12.00"
}'
```

> The above command returns JSON structured like this:

```json
{
    "id": 291,
    "coin": 1,
    "quantity": "2.0000",
    "quote": "8000000",
    "quote_with_fee": "8080000",
    "fee": 80000.0,
    "coin_price": "1000.00",
    "side": "sell",
    "state": "done",
    "request_type": 2,
    "source": "merchant",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint allows you to sell a coin by specifying the desired quantity.

### HTTP Request

`GET {BASE_URL}/market/sell/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to sell.
quantity | The quantity of coin to sell.




## Buy Coin with Quote


```shell
curl --location '{BASE_URL}/market/buy/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "coin_id":1,
    "quote":"50000"
}'
```

> The above command returns JSON structured like this:

```json
{
    "id": 291,
    "coin": 1,
    "quantity": "2.0000",
    "quote": "8000000",
    "quote_with_fee": "8080000",
    "fee": 80000.0,
    "coin_price": "1000.00",
    "side": "buy",
    "state": "done",
    "request_type": 2,
    "source": "merchant",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint creates an order to buy a coin by specifying the desired quote amount.

### HTTP Request

`GET {BASE_URL}/market/buy/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to buy.
quote | Amount of quote currency to spend.




## Sell Coin with Quote


```shell
curl --location '{BASE_URL}/market/sell/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "coin_id":1,
    "quote":"50000"
}'
```

> The above command returns JSON structured like this:

```json
{
    "id": 291,
    "coin": 1,
    "quantity": "2.0000",
    "quote": "8000000",
    "quote_with_fee": "8080000",
    "fee": 80000.0,
    "coin_price": "1000.00",
    "side": "sell",
    "state": "done",
    "request_type": 2,
    "source": "merchant",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint creates an order to sell a coin by specifying the desired quote amount.

### HTTP Request

`GET {BASE_URL}/market/sell/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to sell.
quote | Amount of quote currency to receive.



## Sell & Cash Out

```shell
curl --location '{BASE_URL}/market/sell/cash-out/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "coin_id":1,
    "quote":"50000"
    "card_id":53
}'
```

> The above command returns JSON structured like this:

```json
{
    "id": 291,
    "coin": 1,
    "quantity": "2.0000",
    "quote": "8000000",
    "quote_with_fee": "8080000",
    "fee": 80000.0,
    "coin_price": "1000.00",
    "side": "sell",
    "state": "done",
    "request_type": 2,
    "source": "merchant",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

The final quote_with_fee of this order would be directly withdraw to user bank account (card_id).

### HTTP Request

`POST {BASE_URL}/market/sell/cash-out/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to sell.
quote | Amount of quote currency to receive.
card_id | The id of verified card of client.




## Sell & Settle by merchant

```shell
curl --location '{BASE_URL}/market/sell/settle-by-merchant/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json' \
--data '{
    "coin_id":1,
    "quote":"50000"
}'
```

> The above command returns JSON structured like this:

```json
{
    "id": 291,
    "coin": 1,
    "quantity": "2.0000",
    "quote": "8000000",
    "quote_with_fee": "8080000",
    "fee": 80000.0,
    "coin_price": "1000.00",
    "side": "sell",
    "state": "done",
    "request_type": 2,
    "source": "merchant",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

The final quote_with_fee of this order would be added to merchant account balances.

### HTTP Request

`POST {BASE_URL}/market/sell/settle-by-merchant/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to sell.
quote | Amount of quote currency to receive.




## Get Orders


```shell
curl --location '{BASE_URL}/market/orders/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
{
    "page": 1,
    "page_size": "10",
    "total_pages": 1,
    "total_items": 1,
    "data": [
        {
            "id": 1,
            "coin": 2,
            "quantity": "1.0000",
            "quote": "470358",
            "quote_with_fee": "4662264",
            "fee": 47094.0,
            "coin_price": "4708.00",
            "side": "sell",
            "state": "done",
            "request_type": 2,
            "source": "merchant",
            "created_at": "2024-10-30T10:55:52.949253Z",
            "finalized_at": "2024-10-30T10:55:52.948687Z",
            "coin_name": "طلا آبشده"
        }
    ]
}
```

This endpoint retrieves a list of orders with pagination.

### HTTP Request

`GET {BASE_URL}/market/orders/`


### Query Parameters

Parameter | Description 
--------- | ----------- 
page | The page number to retrieve (default: 1). 
page_size | The number of items per page (default: 10).




## Get Order by User Tracker


```shell
curl --location '{BASE_URL}/market/orders/by-tracker/<user_tracker>/' \
--header 'Authorization: Bearer client_access_token' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
{
    "page": 1,
    "page_size": "10",
    "total_pages": 1,
    "total_items": 1,
    "data": [
        {
            "id": 1,
            "coin": 2,
            "quantity": "1.0000",
            "quote": "470358",
            "quote_with_fee": "4662264",
            "fee": 47094.0,
            "coin_price": "4708.00",
            "side": "sell",
            "state": "done",
            "request_type": 2,
            "source": "merchant",
            "created_at": "2024-10-30T10:55:52.949253Z",
            "finalized_at": "2024-10-30T10:55:52.948687Z",
            "coin_name": "طلا آبشده"
        }
    ]
}
```

This endpoint retrieves the details of a specific order using the `user_tracker` identifier.

### HTTP Request

`GET {BASE_URL}/market/orders/by-tracker/<user_tracker>/`


### URL Parameters

Parameter | Description 
--------- | ----------- 
user_tracker | Unique tracker ID of the order to fetch details for.  



