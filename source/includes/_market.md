# Market

## Get Coin Price


```shell
curl --location --request GET 'https://napi.zarpay24.com/api/v1/market/coins/GOLD/' \
--header 'Authorization: your_api_key_here' \
--header 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
{
    "id": 1,
    "symbol": "GOLD",
    "persian_name": "طلا آب‌شده",
    "buy_active": true,
    "sell_active": true,
    "max_order_qty": "350000000",
    "buy_price": "4000000",
    "sell_price": "3000000",
    "fee_percentage": "1.00",
    "unit": "گرم",
    "decimal_places": 4
}
```

This endpoint retrieves detailed information about a specific coin.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/coins/<symbol>/`


### URL Parameters

Parameter | Description
--------- | -----------
symbol | The symbol of coin to retrieve.




## Buy Coin with Quantity


```shell
curl --location 'https://napi.zarpay24.com/api/v1/market/buy/' \
--header 'Authorization: your_api_key_here' \
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
    "source": "front",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint allows you to purchase a coin by specifying the desired quantity.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/buy/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to buy.
quantity | The quantity of coin to buy.




## Sell Coin with Quantity


```shell
curl --location 'https://napi.zarpay24.com/api/v1/market/sell/' \
--header 'Authorization: your_api_key_here' \
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
    "source": "front",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint allows you to sell a coin by specifying the desired quantity.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/sell/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to sell.
quantity | The quantity of coin to sell.




## Buy Coin with Quote


```shell
curl --location 'https://napi.zarpay24.com/api/v1/market/buy/' \
--header 'Authorization: your_api_key_here' \
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
    "source": "front",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint creates an order to buy a coin by specifying the desired quote amount.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/buy/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to buy.
quote | Amount of quote currency to spend.




## Sell Coin with Quote


```shell
curl --location 'https://napi.zarpay24.com/api/v1/market/sell/' \
--header 'Authorization: your_api_key_here' \
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
    "source": "front",
    "user_tracker": null,
    "created_at": "2025-01-03T12:46:18.321695Z",
    "finalized_at": "2025-01-03T12:46:18.319125Z",
    "coin_name": "طلا آب‌شده"
}
```

This endpoint creates an order to sell a coin by specifying the desired quote amount.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/sell/`


### Request Body

Parameter | Description
--------- | -----------
coin_id | The id of coin to sell.
quote | Amount of quote currency to receive.




## Get Orders


```shell
curl --location 'https://napi.zarpay24.com/api/v1/market/orders/' \
--header 'Authorization: your_api_key_here' \
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
            "source": "front",
            "created_at": "2024-10-30T10:55:52.949253Z",
            "finalized_at": "2024-10-30T10:55:52.948687Z",
            "coin_name": "طلا آبشده"
        }
    ]
}
```

This endpoint retrieves a list of orders with pagination.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/orders/`


### Query Parameters

Parameter | Description 
--------- | ----------- 
page | The page number to retrieve (default: 1). 
page_size | The number of items per page (default: 10).




## Get Order by User Tracker


```shell
curl --location 'https://napi.zarpay24.com/api/v1/market/orders/by-tracker/<user_tracker>/' \
--header 'Authorization: your_api_key_here' \
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
            "source": "front",
            "created_at": "2024-10-30T10:55:52.949253Z",
            "finalized_at": "2024-10-30T10:55:52.948687Z",
            "coin_name": "طلا آبشده"
        }
    ]
}
```

This endpoint retrieves the details of a specific order using the `user_tracker` identifier.

### HTTP Request

`GET https://napi.zarpay24.com/api/v1/market/orders/by-tracker/<user_tracker>/`


### URL Parameters

Parameter | Description 
--------- | ----------- 
user_tracker | Unique tracker ID of the order to fetch details for.  



