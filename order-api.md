# Order API

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/item" %}
{% api-method-summary %}
Add item to order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "bcin": "SAMUVRY",
    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
    "quantity": 1,
    "merchant_id": "beeshop",
    "list_price": 10.0
}
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/item" %}
{% api-method-summary %}
Update item in order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "bcin": "SAMUVRY",
    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
    "quantity": 1,
    "merchant_id": "beeshop",
    "list_price": 10.0
}
```

{% api-method method="delete" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/item" %}
{% api-method-summary %}
Delete item in order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "bcin": "SAMUVRY",
    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
    "quantity": 1,
    "merchant_id": "beeshop",
    "list_price": 10.0
}
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/shippingaddress" %}
{% api-method-summary %}
Add shipping address
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
		"shipping_address":{
            "full_name": "Jack Jiang",
            "street_1": "8 Danbury court",
            "street_2": null,
            "city": "Markham",
            "country": "Canada",
            "province": "ON",
            "postal_code": "L3R7S1",
            "phone": "416-2728539",
            "email": "mjiang2000@hotmail.com"
        },
        "billing_address":{
            "full_name": "Jack Jiang",
            "street_1": "8 Danbury court",
            "street_2": null,
            "city": "Markham",
            "country": "Canada",
            "province": "ON",
            "postal_code": "L3R7S1",
            "phone": "416-2728539",
            "email": "mjiang2000@hotmail.com"
        }
}
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="order/note" %}
{% api-method-summary %}
Add Notes
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
   "notes":""
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order" %}
{% api-method-summary %}
Get a order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/orderlist" %}
{% api-method-summary %}
Get order list
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/calculation" %}
{% api-method-summary %}
Order calculation
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/validation" %}
{% api-method-summary %}
Order validation
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/submit" %}
{% api-method-summary %}
Submit an order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="new" type="string" required=false %}
y/n. force to create a new order.
{% endapi-method-parameter %}

{% api-method-parameter name="orderid" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielongid" type="string" required=false %}
jielong id. if order id is not generated, use jielong id to create a new order
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *order
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

