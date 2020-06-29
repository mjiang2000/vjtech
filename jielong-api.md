# Jielong API

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong" %}
{% api-method-summary %}
Create a Jielong
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create a new Jeilong
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {token}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{
    "jielong_id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "supplier_merchant_id": "beeshop",
    "merchant_name": "beeshop",
    "micro_merchant_id": "ZEMBC",
    "listed_products": [
        {
            "bcin": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "beeshop",
            "sku": "MT-AC-01",
            "price": {
                "currency": "CAD",
                "list": 10,
                "msrp": 10,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-05-22T13:26:19.0342926Z",
            "stay_on_top": false
        },
        {
            "bcin": "9KBZJAL",
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "beeshop",
            "sku": "B0369",
            "price": {
                "currency": "CAD",
                "list": 35,
                "msrp": 35,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-05-22T13:26:19.034294Z",
            "stay_on_top": false
        }
    ],
    "name": null,
    "description": null,
    "shipping_address": null,
    "billing_address": null,
    "status": "closed",
    "start_date": "2020-05-21T00:00:00Z",
    "end_date": "2020-05-25T16:33:27.2971201Z",
    "bc_pay_enabled": false,
    "id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "document_type": "jielong",
    "shipping_rules": [
        {
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "description_template": null,
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
            "rule_code": "pickup",
            "name": "pickup",
            "description": "pickup",
            "description_template": null,
            "settings": [
                {
                    "name": "pickup_address",
                    "value": "4 Danbury court"
                }
            ]
        }
    ],
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
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    message = "invalid input",
    validation_errors = []
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request Body

```text
{
  "name": "beeshop product jielong",
  "micro_merchant_id" : "ZEMBC",
  "end_date":"2020-05-23",
    "listed_products": [
      {
      "bcin":"SAMUVRY",
      "merchant_id":"beeshop"
      },
      {
      "bcin":"9KBZJAL",
      "merchant_id":"beeshop"
      }
    ]
}
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId" %}
{% api-method-summary %}
Update a Jielong
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
Jielong id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "jielong_id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "supplier_merchant_id": "beeshop",
    "merchant_name": "beeshop",
    "micro_merchant_id": "ZEMBC",
    "listed_products": [
        {
            "bcin": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "beeshop",
            "sku": "MT-AC-01",
            "price": {
                "currency": "CAD",
                "list": 10,
                "msrp": 10,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-05-22T13:26:19.0342926Z",
            "stay_on_top": false
        },
        {
            "bcin": "9KBZJAL",
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "beeshop",
            "sku": "B0369",
            "price": {
                "currency": "CAD",
                "list": 35,
                "msrp": 35,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-05-22T13:26:19.034294Z",
            "stay_on_top": false
        }
    ],
    "name": null,
    "description": null,
    "shipping_address": null,
    "billing_address": null,
    "status": "closed",
    "start_date": "2020-05-21T00:00:00Z",
    "end_date": "2020-05-25T16:33:27.2971201Z",
    "bc_pay_enabled": false,
    "id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "document_type": "jielong",
    "shipping_rules": [
        {
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "description_template": null,
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
            "rule_code": "pickup",
            "name": "pickup",
            "description": "pickup",
            "description_template": null,
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
  "name": "beeshop product jielong",
  "description":"",
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
        },
    "BCPayEnabled":true,
    "shipping_rules": [
        {
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "description_template": null,
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
            "rule_code": "pickup",
            "name": "pickup",
            "description": "pickup",
            "description_template": null,
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

{% api-method method="patch" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/close" %}
{% api-method-summary %}
Close a Jielong
{% endapi-method-summary %}

{% api-method-description %}
A jielong without submitted order cannot be closed. GUI should prompt user to Cancel the Jielong.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
Jielong id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *merchant_order 
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

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

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
If  jielong has no active orders, it cannot be closed
{% endapi-method-response-example-description %}

```
No active order found.
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/cancel" %}
{% api-method-summary %}
Cancel a Jielong
{% endapi-method-summary %}

{% api-method-description %}
A jielong enabled beeshop pay cannot be Cancelled if there is submitted orders.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
Jielong id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *merchant_order 
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=304 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
 A jielong enabled beeshop pay cannot be Cancelled if there is submitted orders.
{% endapi-method-response-example-description %}

```text
Jielong cannot be cancelled, it has active orders.
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/cancel" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
A jielong enabled beeshop pay cannot be Cancelled if there is submitted orders.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/publish/:groupId" %}
{% api-method-summary %}
Publish a jielong to a group
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
jielong id
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="string" required=true %}
group id
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
jielong\_by\_group document
{% endapi-method-response-example-description %}

```text
{
    "jielong_id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "group_id": "group1",
    "published_at": "2020-05-25T17:06:19.3264005Z",
    "published_by": "mjiang2000@gmail.com",
    "jielong_status": "closed",
    "id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a-group1",
    "document_type": "jielong_by_group"
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/product" %}
{% api-method-summary %}
Add product to Jielong
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
jielong Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *jielong 
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

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

post a list of jielong products

```text
[
    {
    "bcin":"SAMUVRY",
    "merchant_id":"beeshop"
    },
    {
    "bcin":"9KBZJAL",
    "merchant_id":"beeshop"
    }
]
```

{% api-method method="delete" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/product/:bcin" %}
{% api-method-summary %}
Remove a product from Jielong
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
Jielong id
{% endapi-method-parameter %}

{% api-method-parameter name="bcin" type="string" required=true %}
product id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 *jielong
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId" %}
{% api-method-summary %}
Get a Jielong
{% endapi-method-summary %}

{% api-method-description %}
This call is authorized call. it will return "editable" flag according to user's context.NEW Update\* ordered\_quantity field will be returned in the listed\_products
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
jielong id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 "editable": true,
 ...
  "listed_products": [ {
            "ordered_quantity": 3,
            "bcin": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "beeshop",
            "sku": "MT-AC-01",
            "price": {
                "currency": "CAD",
                "list": 10,
                "msrp": 10,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-05-22T13:26:19.0342926Z",
            "stay_on_top": false
        }
    ]
  ...
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/summary" %}
{% api-method-summary %}
Get a Jielong Summary
{% endapi-method-summary %}

{% api-method-description %}
This is anonymous call
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
jielong id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
*jielong
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/group/:groupId/jielonglist" %}
{% api-method-summary %}
Get a list of Jielong by Group Id
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="string" required=true %}
group id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="status" type="string" required=false %}
Supported status: opened, closed, cancelled  
Provide multiple status by "\|", for example "opened\|closed"
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}

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
        {
            "jielong_id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
            "group_id": "group1",
            "published_at": "2020-05-22T15:06:46.3822637Z",
            "published_by": "mjiang2000@gmail.com",
            "jielong_status": "opened",
            "id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a-group1",
            "document_type": "jielong_by_group"
        }
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host=" https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/productlist" %}
{% api-method-summary %}
Get a list of Products by Jielong Id
{% endapi-method-summary %}

{% api-method-description %}
NEW Update\* ordered\_quantity field will be returned in the listed\_products
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}
Jielong id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
[
    {
        "ordered_quantity": 3,
        "bcin": "SAMUVRY",
        "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
        "language": "en",
        "merchant_id": "beeshop",
        "merchant_name": "beeshop",
        "sku": "MT-AC-01",
        "price": {
            "currency": "CAD",
            "list": 10.0,
            "msrp": 10.0,
            "cost": null
        },
        "listed_by": "mjiang2000@gmail.com",
        "listed_at": "2020-05-22T13:26:19.0342926Z",
        "stay_on_top": false
    },
    {
        "ordered_quantity": 3,
        "bcin": "9KBZJAL",
        "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
        "language": "en",
        "merchant_id": "beeshop",
        "merchant_name": "beeshop",
        "sku": "B0369",
        "price": {
            "currency": "CAD",
            "list": 35.0,
            "msrp": 35.0,
            "cost": null
        },
        "listed_by": "mjiang2000@gmail.com",
        "listed_at": "2020-05-22T13:26:19.034294Z",
        "stay_on_top": false
    }
]
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/image" %}
{% api-method-summary %}
Add image to Jielong
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="image1" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "id": "d610e2ba-1f5e-49d9-8c65-308fab26b497",
    "jielong_id": "d610e2ba-1f5e-49d9-8c65-308fab26b497",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": null,
    "micro_merchant_id": "ZEMBC",
    "listed_products": [
        {
            "bcin": "9KBZJAL",
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set) jack",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/9KBZJAL-4964549034550-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/9KBZJAL-4964549034550-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/9KBZJAL-4964549034550-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/9KBZJAL-4964549034550-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/9KBZJAL-4964549034550-02.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/9KBZJAL-4964549034550-02.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/9KBZJAL-4964549034550-02.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-02.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/9KBZJAL-4964549034550-02.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/9KBZJAL-4964549034550-03.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/9KBZJAL-4964549034550-03.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/9KBZJAL-4964549034550-03.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-03.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/9KBZJAL-4964549034550-03.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/9KBZJAL-4964549034550-05.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/9KBZJAL-4964549034550-05.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/9KBZJAL-4964549034550-05.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-05.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/9KBZJAL-4964549034550-05.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/9KBZJAL-4964549034550-04.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/9KBZJAL-4964549034550-04.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/9KBZJAL-4964549034550-04.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-04.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/9KBZJAL-4964549034550-04.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "beeshop",
            "sku": "B0369",
            "price": {
                "currency": "CAD",
                "list": 35,
                "msrp": 35,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-06-09T23:40:47.8726322Z",
            "stay_on_top": false
        },
        {
            "bcin": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "language": "en",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MT-AC-01",
            "price": {
                "currency": "CAD",
                "list": 10,
                "msrp": 10,
                "cost": null
            },
            "listed_by": "mjiang2000@gmail.com",
            "listed_at": "2020-06-09T23:40:47.8726332Z",
            "stay_on_top": false
        }
    ],
    "name": "Jack Jielong 2",
    "description": null,
    "shipping_address": null,
    "billing_address": null,
    "status": "opened",
    "start_date": "2020-06-09T00:00:00Z",
    "end_date": "2020-06-30T00:00:00",
    "bc_pay_enabled": true,
    "image": "https://bc01dmedia.blob.core.windows.net/jielong-image/d610e2ba-1f5e-49d9-8c65-308fab26b497-groupby.jpg",
    "document_type": "jielong"
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
Content-Type: multipart/form-data

Response jielong object will have url link
{
...
"image": "https://bc01dmedia.blob.core.windows.net/jielong-image/d610e2ba-1f5e-49d9-8c65-308fab26b497-groupby.jpg",
...
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/orderlist" %}
{% api-method-summary %}
Get a list of Jielong orders
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="status" type="string" required=false %}
submitted \(default\)  
Provide multiple status by "\|", for example "new\|submmited"
{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
10 \(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}

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
       *order1,
       *order2,
       ...
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/ordersummarylist" %}
{% api-method-summary %}
Get a list of Jielong order summaries
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="status" type="string" required=false %}
submitted \(default\)  
Provide multiple status by "\|", for example "new\|submitted"
{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
10 \(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}

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
         {
            "order_id": "5ceddfdf-a57b-4d5c-b3ff-c92088cf09d3",
            "user_id": "mjiang2000@gmail.com",
            "jielong_id": "10099ea5-13de-4ce6-9d0e-5d91c95f871c",
            "group_id": null,
            "email": null,
            "line_items": [
                {
                    "bcin": "SAMUVRY",
                    "sku": null,
                    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
                    "quantity": 5,
                    "image_url": null,
                    "list_price": 10.0,
                    "sale_price": null,
                    "merchant_id": "beeshop",
                    "weight": 0.0
                }
            ],
            "created_at": "2020-06-08T20:09:08.5787054Z",
            "status": "submitted",
            "order_number": "BSC20-52"
        },
        {
            "order_id": "c56705ea-fe0d-4366-aeb8-c8ae3b303535",
            "user_id": "mjiang2000@hotmail.com",
            "jielong_id": "10099ea5-13de-4ce6-9d0e-5d91c95f871c",
            "group_id": null,
            "email": null,
            "line_items": [
                {
                    "bcin": "SAMUVRY",
                    "sku": null,
                    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
                    "quantity": 5,
                    "image_url": null,
                    "list_price": 10.0,
                    "sale_price": null,
                    "merchant_id": "beeshop",
                    "weight": 0.0
                }
            ],
            "created_at": "2020-06-08T20:10:46.9539363Z",
            "status": "submitted",
            "order_number": "BSC20-56"
        }
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/orderlist" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="status" type="string" required=false %}
"new\|submmited"
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/publishedgrouplist" %}
{% api-method-summary %}
Get a list of published group id by jielong id
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="page\_size" type="string" required=false %}
10 \(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}

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
                {
                    "jielong_id": "0f22c74c-0e8f-4996-8e4f-9e3276420764",
                    "group_id": "group1",
                    "published_at": "2020-06-16T15:24:51.9600251Z",
                    "published_by": "mjiang2000@gmail.com",
                    "jielong_status": "opened",
                    "document_type": "jielong_by_group"
                }
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

