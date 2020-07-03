# Order API - Customer order

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order" %}
{% api-method-summary %}
Get an order
{% endapi-method-summary %}

{% api-method-description %}
Note: if get an order by jielong\_id and order is not exist, API will create an empty order and return in response
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

{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
    "order_id": "395c62f7-b120-463b-8576-e7d530975217",
    "user_id": "mjiang2000@gmail.com",
    "jielong_id": "74202b37-35d2-487f-97fb-c8b37a684e75",
    "email": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "merchant_id": null,
    "merchant_name": null,
    "line_items": null,
    "base_amount": 0.0,
    "shipping_method": null,
    "shipping_method_name": null,
    "shipping_method_description": null,
    "shipping_amount": 0.0,
    "total_amount": 0.0,
    "billing_address": null,
    "shipping_address": null,
    "created_at": "2020-06-23T13:33:14.0654629Z",
    "status": "new",
    "payment_id": null,
    "order_number": "BSC20-62",
    "notes": null,
    "bc_pay_enabled": true,
    "id": "395c62f7-b120-463b-8576-e7d530975217",
    "document_type": "order"
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

{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
    "id": "94c3ef1c-269b-4476-b4d1-9eb5dcb2837d",
    "order_id": "94c3ef1c-269b-4476-b4d1-9eb5dcb2837d",
    "user_id": "mjiang2000@hotmail.com",
    "jielong_id": "74202b37-35d2-487f-97fb-c8b37a684e75",
    "email": "mjiang2000@hotmail.com",
    "micro_merchant_id": "ZEMBC",
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "weight": 0
        }
    ],
    "base_amount": 10,
    "shipping_method": null,
    "shipping_method_name": null,
    "shipping_method_description": null,
    "shipping_amount": 0,
    "total_amount": 10,
    "billing_address": null,
    "shipping_address": null,
    "created_at": "2020-06-23T13:33:56.4431669Z",
    "updated_at": "2020-06-23T13:34:01.1739112Z",
    "status": "new",
    "payment_id": null,
    "order_number": "BSC20-63",
    "notes": null,
    "bc_pay_enabled": true,
    "document_type": "order"
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

{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
{% api-method-parameter name="status" type="string" required=false %}
Supported status: new, submitted, shipped, cancelled  
Use "\|" to provide multiple status, for example "new\|submited"  
{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
10
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}
token
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "has_more": false,
    "continuation_token": null,
    "results": [
        *order,
        *order
    ]
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

{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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
[
    {
        "bcin":"SAMUVRY",
        "merchant_id":"beeshop",
        "before_change":"5",
        "after_change":"0",
        "change_reason": "product_not_found"
    }
]
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

{% api-method-parameter name="order\_id" type="string" required=false %}
order id. If order is is provided, jielong id can be ingore for better performance
{% endapi-method-parameter %}

{% api-method-parameter name="jielong\_id" type="string" required=false %}
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/amendment/item" %}
{% api-method-summary %}
Amend an item in order
{% endapi-method-summary %}

{% api-method-description %}
Amend an jielong order after the payment is made by the customer user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="order\_id" type="string" required=true %}
the order to be amend
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "id": "4e0e412e-40f9-4dd0-8cb5-8fa08f8ef6ee",
    "order_amendment_id": "4e0e412e-40f9-4dd0-8cb5-8fa08f8ef6ee",
    "order_id": "577b066f-a30f-40a4-8951-077e2af1dadf",
    "user_id": "mjiang2000@gmail.com",
    "jielong_id": "ce59a172-41b9-4cef-9243-ce777cdf418d",
    "email": null,
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "weight": 0
        }
    ],
    "base_amount": 10,
    "shipping_method": null,
    "shipping_method_name": null,
    "shipping_method_description": null,
    "shipping_amount": 0,
    "total_amount": 10,
    "created_at": "2020-06-08T02:55:38.9553867Z",
    "updated_at": "2020-06-08T02:55:41.2548526Z",
    "status": "new",
    "refund_id": null,
    "order_number": "BSC20-40",
    "amended_by": "mjiang2000@gmail.com",
    "document_type": "order_amendment"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid Input
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

Request Body

* the quantity is the number that changed to. For example, the original number is 5, it can be changed to 3, which means refund 2 items. As a result, 2 will be persisted in the order amendment for this item.
* One order amendment can contain multiple items
* The order amendment must be refund successfully to be consider in the campaign close action
* One order can have multiple amendments, the GUI should avoid guiding user creating multiple amendments. Unless in scenario that extract amendment is required when previous amendment has completed refund process. 

```text
{
        "bcin": "SAMUVRY",
    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
    "quantity": 1,
    "merchant_id": "beeshop",
        "list_price": 10.0
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/shippingquotes" %}
{% api-method-summary %}
Get shipping quotes
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
{% api-method-parameter name="order\_id" type="string" required=true %}
the order to be amend
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "quotes": [
        {
            "quote": 0.0,
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "settings": [
                {
                    "name": "x_amount",
                    "value": "10"
                },
                {
                    "name": "flat_price",
                    "value": "3.99"
                }
            ]
        },
        {
            "quote": 0.0,
            "rule_code": "pickup",
            "name": "pickup",
            "description": "pickup",
            "settings": [
                {
                    "name": "pickup_address",
                    "value": "4 Danbury court"
                }
            ]
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid Input
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/shippingmethod" %}
{% api-method-summary %}
Update order shipping method
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
{% api-method-parameter name="order\_id" type="string" required=true %}
the order to be amend
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "order_id": "33a5de0b-8642-463a-82bf-032ef7d94df6",
    "user_id": "mjiang2000@gmail.com",
    "jielong_id": "d610e2ba-1f5e-49d9-8c65-308fab26b497",
    "email": null,
    "micro_merchant_id": "ZEMBC",
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 5,
            "image_url": null,
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "weight": 0
        }
    ],
    "base_amount": 50,
    "shipping_method": "free_shipping_over_x_amount_or_flat",
    "shipping_method_name": "Free shipping over x amount, otherwisee flat price",
    "shipping_method_description": "Free shipping over x amount, otherwisee flat price",
    "shipping_amount": 0,
    "total_amount": 50,
    "billing_address": {
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "8 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "ON",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com"
    },
    "shipping_address": {
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "8 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "ON",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com"
    },
    "created_at": "2020-06-09T23:41:04.7878223Z",
    "updated_at": "2020-06-12T13:19:26.2269966Z",
    "status": "submitted",
    "payment_id": "e3ed37d7-11e2-452c-acd2-f835f04c6d05",
    "order_number": "BSC1-31",
    "notes": null,
    "bc_pay_enabled": true,
    "document_type": "order"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid Input
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

Request Body

```text
        {
            "shipping_amount": 0.0,
            "shipping_method": "free_shipping_over_x_amount_or_flat",
            "shipping_method_name": "Free shipping over x amount, otherwisee flat price",
            "shipping_method_description": "Free shipping over x amount, otherwisee flat price"
        }
```

