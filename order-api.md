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
{% api-method-parameter name="original" type="string" required=false %}
y/n  
y: as the same state when order is placed.  
n: apply order amendments to original order
{% endapi-method-parameter %}

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
    "micro_merchant_name": "mjiang2000@gmail.com",
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
    "micro_merchant_name": "mjiang2000@gmail.com",
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

{% api-method-response-example httpCode=412 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 "change_logs": [
        {
            "bcin":"SAMUVRY",
           "line_item":lineitem*
            "merchant_id":"beeshop",
            "before_change":"5",
            "after_change":"0",
            "change_reason": "product_not_found"
        },
         {
            "bcin":"SAMUVRY",
           "line_item":lineitem*
            "merchant_id":"beeshop",
            "before_change":"5",
            "after_change":"1",
            "change_reason": "insufficient_inventory"
        },
         {
            "bcin":"SAMUVRY",
            "line_item":lineitem*,
            "merchant_id":"beeshop",
            "before_change":"10",
            "after_change":"9",
            "change_reason": "price_adjusted"
        }
    ],
    "coupon_log":"coupon change message"
}
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/amendment" %}
{% api-method-summary %}
Amend order
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
            "order_amendment_id": "5d07f7d1-6a99-4f67-9279-7e8b49413766",
            "order_id": "3f5f61f0-d2c2-4ce8-bf3c-00bc2617a5cd",
            "user_id": "mjiang2000@gmail.com",
            "jielong_id": "750a31a1-5125-4413-84bf-ae9949b1fb9c",
            "email": "mjiang2000@gmail.com",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "line_items": [
                {
                    "bcin": "9KBZJAL",
                    "sku": null,
                    "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
                    "quantity": 1,
                    "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
                    "list_price": 27.42,
                    "sale_price": null,
                    "merchant_id": "beeshop",
                    "tax_code": "regular",
                    "weight": 0.0
                }
            ],
            "base_amount": 27.42,
            "shipping_method": null,
            "shipping_method_name": null,
            "shipping_method_description": null,
            "shipping_amount": 0.0,
            "total_amount": 27.42,
            "created_at": "2020-08-27T20:17:50.0878031Z",
            "updated_at": "2020-08-27T20:17:50.092274Z",
            "status": "refunded",
            "refund_id": "7cc23bcb-1d83-4905-b1f6-2d2a0c82a1bf",
            "refund_gateway": "Spreedly",
            "refund_provider": "VISA",
            "order_number": "BSC1-1361",
            "amended_by": "mjiang2000@gmail.com",
            "note": "customer request",
            "id": "5d07f7d1-6a99-4f67-9279-7e8b49413766",
            "document_type": "order_amendment",
            "_etag": "\"4f0549d7-0000-0200-0000-5f4815460000\""
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
{
    "message": "Invalid input",
    "validation_errors": [
        "line item 9KBZJAL: remaining qty(1) < amendment qty (2)"
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request Body

* the quantity is the number that to be reduced from the original order.
* One order amendment can contain multiple items
* The order amendment must be refund successfully to be considered in the campaign close action
* One order can have multiple amendments 

```text
{
    "line_items": [
            {
                    "bcin": "9KBZJAL",
                    "quantity":2,
                    "merchant_id": "beeshop"
            },
            {
                    "bcin": "SAMUVRY",
                    "quantity":2,
                    "merchant_id": "beeshop"
            }
    ],
    "shipping_amount": 3.0,
    "note":"second amendment"
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/amendment" %}
{% api-method-summary %}
Get order amendment
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="order\_id" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "amendments": [
        {
            "order_amendment_id": "3cb39c83-eeea-44e9-8ba9-0fac5e94ace9",
            "order_id": "3f5f61f0-d2c2-4ce8-bf3c-00bc2617a5cd",
            "user_id": "mjiang2000@gmail.com",
            "jielong_id": "750a31a1-5125-4413-84bf-ae9949b1fb9c",
            "email": "mjiang2000@gmail.com",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "line_items": [
                {
                    "bcin": "9KBZJAL",
                    "sku": null,
                    "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
                    "quantity": 1,
                    "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
                    "list_price": 27.42,
                    "sale_price": null,
                    "merchant_id": "beeshop",
                    "tax_code": "regular",
                    "weight": 0.0
                }
            ],
            "base_amount": 27.42,
            "shipping_method": null,
            "shipping_method_name": null,
            "shipping_method_description": null,
            "shipping_amount": 0.0,
            "total_amount": 27.42,
            "created_at": "2020-08-26T17:57:26.0136382Z",
            "updated_at": "2020-08-26T17:57:26.152041Z",
            "status": "refunded",
            "refund_id": "11cd6f03-a327-48a7-9ba7-9118d764add7",
            "refund_gateway": "Spreedly",
            "refund_provider": "VISA",
            "order_number": "BSC1-1361",
            "amended_by": "mjiang2000@gmail.com",
            "note": null,
            "id": "3cb39c83-eeea-44e9-8ba9-0fac5e94ace9",
            "document_type": "order_amendment",
            "_etag": "\"da062ed4-0000-0200-0000-5f46a2a70000\""
        },
        {
            "order_amendment_id": "5d07f7d1-6a99-4f67-9279-7e8b49413766",
            "order_id": "3f5f61f0-d2c2-4ce8-bf3c-00bc2617a5cd",
            "user_id": "mjiang2000@gmail.com",
            "jielong_id": "750a31a1-5125-4413-84bf-ae9949b1fb9c",
            "email": "mjiang2000@gmail.com",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "line_items": [
                {
                    "bcin": "9KBZJAL",
                    "sku": null,
                    "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
                    "quantity": 1,
                    "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
                    "list_price": 27.42,
                    "sale_price": null,
                    "merchant_id": "beeshop",
                    "tax_code": "regular",
                    "weight": 0.0
                }
            ],
            "base_amount": 27.42,
            "shipping_method": null,
            "shipping_method_name": null,
            "shipping_method_description": null,
            "shipping_amount": 0.0,
            "total_amount": 27.42,
            "created_at": "2020-08-27T20:17:50.0878031Z",
            "updated_at": "2020-08-27T20:17:50.092274Z",
            "status": "refunded",
            "refund_id": "7cc23bcb-1d83-4905-b1f6-2d2a0c82a1bf",
            "refund_gateway": "Spreedly",
            "refund_provider": "VISA",
            "order_number": "BSC1-1361",
            "amended_by": "mjiang2000@gmail.com",
            "note": null,
            "id": "5d07f7d1-6a99-4f67-9279-7e8b49413766",
            "document_type": "order_amendment",
            "_etag": "\"4f0549d7-0000-0200-0000-5f4815460000\""
        }
    ],
    "remaining_order": {
        "remainingLineItems": [
            {
                "bcin": "9KBZJAL",
                "sku": null,
                "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
                "quantity": 1,
                "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
                "list_price": 27.42,
                "sale_price": null,
                "merchant_id": "beeshop",
                "tax_code": "regular",
                "weight": 0.0
            }
        ],
        "remainingShippingAmount": 0.0
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/journals" %}
{% api-method-summary %}
Order Journal list
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="order\_id" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
action: paid, refunded, shipped, received  
reference\_id: payment\_id\(paid\), order\_amendment\_id\(refunded\)
{% endapi-method-response-example-description %}

```
{
 "journals": [
    {
        "order_id": "1c164786-4318-400a-996e-a7e037c6c3ce",
        "action": "paid",
        "occurred_at": "2020-09-16T17:53:55.0835567Z",
        "amount": "54.84",
        "reference_id": "aaac4dec-b3fc-48aa-b09e-ae7fa63c5580",
        "properties": null,
        "id": "ddcd36b3-04ca-4eea-b0e2-194b994ca81f",
        "document_type": "order_journal",
    },
    {
        "order_id": "1c164786-4318-400a-996e-a7e037c6c3ce",
        "action": "refunded",
        "occurred_at": "2020-09-16T17:55:02.8259241Z",
        "amount": "0.01",
        "reference_id": "8e5dabbb-3d22-4c5e-81e8-a6e86e2dec82",
        "properties": null,
        "id": "18858b45-ec04-4bdd-b92a-d205726772e7",
        "document_type": "order_journal",
    }
 ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/cancel" %}
{% api-method-summary %}
Cancel order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="order\_id" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Status = cancelled
{% endapi-method-response-example-description %}

```
{
    "id": "3cd78d1e-fe4b-4807-b80a-3262c835cf25",
    "_rid": "dhoXALwMwpf7BQAAAAAAAA==",
    "_self": "dbs/dhoXAA==/colls/dhoXALwMwpc=/docs/dhoXALwMwpf7BQAAAAAAAA==/",
    "_ts": 1604108086,
    "_etag": "\"b600d932-0000-0200-0000-5f9cbf360000\"",
    "order_id": "3cd78d1e-fe4b-4807-b80a-3262c835cf25",
    "user_id": "mjiang2000@gmail.com",
    "jielong_id": "3cf5ae93-1028-40e7-9f21-96f66551f3ef",
    "email": "mjiang2000@gmail.com",
    "user_name": "Jack Jiang Gmail3",
    "micro_merchant_id": "ZEMBC",
    "micro_merchant_name": "mjiang2000@gmail.com",
    "merchant_id": "pennystore",
    "merchant_name": "Penny Store",
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": null,
            "quantity": 1,
            "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/SAMUVRY-4991087345671-01.jpg",
            "list_price": 0.01,
            "sale_price": null,
            "merchant_id": "pennystore",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "base_amount": 0.01,
    "shipping_method": null,
    "shipping_method_name": null,
    "shipping_method_description": null,
    "shipping_amount": 0.0,
    "total_amount": 0.01,
    "billing_address": null,
    "shipping_address": null,
    "created_at": "2020-10-31T01:31:39.824619Z",
    "updated_at": "2020-10-31T01:34:45.1475653Z",
    "status": "cancelled",
    "payment_id": null,
    "payment_gateway": null,
    "payment_provider": null,
    "order_number": "BSC1-1531",
    "notes": null,
    "bc_pay_enabled": false,
    "refunded": false,
    "document_type": "order"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/order/v1" path="/order/coupon/:code/{action}" %}
{% api-method-summary %}
Apply Coupon
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="action" type="string" required=false %}
apply or remove
{% endapi-method-parameter %}

{% api-method-parameter name="code" type="string" required=false %}
coupon code
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "id": "e9faacc5-dc03-4cc2-a3e9-d8c6473b9951",
    "_rid": "dhoXALwMwpddBgAAAAAAAA==",
    "_self": "dbs/dhoXAA==/colls/dhoXALwMwpc=/docs/dhoXALwMwpddBgAAAAAAAA==/",
    "_ts": 1605288791,
    "_etag": "\"39000546-0000-0200-0000-5faec3570000\"",
    "order_id": "e9faacc5-dc03-4cc2-a3e9-d8c6473b9951",
    "user_id": "mjiang2000@gmail.com",
    "jielong_id": "c071353b-3ee5-4c0f-9d8f-433e580bff5f",
    "email": "mjiang2000@gmail.com",
    "user_name": "Jack Jiang Gmail3",
    "micro_merchant_id": "ZEMBC",
    "micro_merchant_name": "mjiang2000@gmail.com",
    "merchant_id": "pennystore",
    "merchant_name": "Penny Store",
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": null,
            "quantity": 5,
            "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/SAMUVRY-4991087345671-01.jpg",
            "list_price": 8.64,
            "sale_price": null,
            "merchant_id": "pennystore",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "base_amount": 43.2,
    "shipping_method": null,
    "shipping_method_name": null,
    "shipping_method_description": null,
    "shipping_amount": 0.0,
    "total_amount": 42.2,
    "billing_address": null,
    "shipping_address": null,
    "created_at": "2020-11-13T17:21:10.3730198Z",
    "updated_at": "2020-11-13T17:33:08.9218814Z",
    "status": "submitted",
    "payment_id": null,
    "payment_gateway": null,
    "payment_provider": null,
    "order_number": "BSC1-1629",
    "notes": null,
    "bc_pay_enabled": false,
    "refunded": false,
    "coupon": {
        "code": "COUPON1",
        "coupon_type": "fix_amount_over_min_value",
        "coupon_description": "fix_amount_over_min_value",
        "settings": [
            {
                "name": "min_order_total_before_tax",
                "type": "number",
                "value": "10"
            },
            {
                "name": "discount_amount",
                "type": "number",
                "value": "1"
            }
        ],
        "effective_date": null,
        "expiration_date": null,
        "one_time_use": true,
        "applied": false,
        "entitled_by": "mjiang2000@gmail.com",
        "id": "COUPON1",
        "document_type": "coupon",
        "_etag": "\"39005040-0000-0200-0000-5faec0e10000\""
    },
    "coupon_discount_amount": 1.0,
    "total_before_coupon_discount": 43.2,
    "document_type": "order"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Invalid coupon code
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

