---
description: about merchant from git
---

# Merchant API

Merchant API

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchantlist" %}
{% api-method-summary %}
Get a list of wholesale merchants
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="continuation\_token" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
default = 5
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "has_more": false,
    "continuation_token": null,
    "results": [
        {
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "logo": "https://media.beeshop.chat/asset/merchant/beeshop/logo.png",
            "overview": null
        },
        {
            "merchant_id": "pennystore",
            "merchant_name": "Penny Store",
            "logo": null,
            "overview": null
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/micromerchant" %}
{% api-method-summary %}
​Create a micro merchant
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "id": "3be9942d-6063-4bc2-8e7b-2736a7ebfc5f",
    "merchant_id": "ZEMBC",
    "merchant_name": "mjiang2000@gmail.com",
    "merchant_type": "micro",
    "roles": [
        "owner"
    ],
    "user_id": "mjiang2000@gmail.com",
    "given_name": "Min",
    "family_name": "Jiang",
    "name": "Min Jiang",
    "email": "mjiang2000@gmail.com",
    "document_type": "user_by_merchant"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"{user Id} is already a owner of merchant."
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
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
    "merchant_name": "mjiang2000@gmail.com"
}
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId" %}
{% api-method-summary %}
​Update a merchant
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}
merchant id
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "merchant_id": "ABCDEFG",
    "merchant_name": "Foodmart",
    "logo": null,
    "language": "en",
    "support_email": "jack.jiang@aj-emall.com",
    "support_phone": null,
    "order_process_notification_email": "jack.jiang@aj-emall.com",
    "theme_color": null,
}
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/user/:UserId" %}
{% api-method-summary %}
Add user to merchant
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userid" type="string" required=true %}
user id
{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}
merchant id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId" %}
{% api-method-summary %}
Get a merchant
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=false %}
merchant id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "merchant_type": "wholesale",
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "owner_id": null,
    "authorized_micro_merchant": false,
    "logo": null,
    "language": "en",
    "support_email": null,
    "support_phone": null,
    "order_process_notification_email": null,
    "pick_list_notification_email": null,
    "payout_notification_email": null,
    "theme_color": null,
    "menu_background_color": null,
    "menu_font_color": null,
    "pay_period": 0,
    "return_policy": null,
    "banner_background_color": null,
    "banner_logo": null,
    "banner_background_image": null,
    "square_banner": null,
    "square_logo": null,
    "overview": null,
    "one_line_marketing_promotion_text": null,
    "active": false,
    "merchant_category_id": null,
    "banner_font_color": null,
    "id": "merchant",
    "document_type": "merchant",
    "_etag": "\"d3008e33-0000-0200-0000-5ec6ec770000\""
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielonglist" %}
{% api-method-summary %}
Get a list of jielong
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="continuation\_token" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
5\(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
opened\(default\), closed, cancelled
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
        *jielong1,
        *jielong2
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

```text
if filter of the order status = closed, the returned jielong object will have order status field
{
 ...
 "merchant_order_status":"new" 
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/shipping" %}
{% api-method-summary %}
Get shipping rules
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

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
    "merchant_id": "ZEMBC",
    "shipping_rules": [
        {
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "description_template": null,
            "settings": [
                {
                    "name": "x_amount",
                    "type": "number",
                    "value": "10"
                },
                {
                    "name": "flat_price",
                    "type": "number",
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
                    "type": "text",
                    "value": "4 Danbury court"
                }
            ]
        }
    ],
    "id": "merchant_shipping_rules",
    "document_type": "merchant_shipping_rules"
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/shipping" %}
{% api-method-summary %}
Update shipping rules
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

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

```text
{
    "merchant_id": "ZEMBC",
    "shipping_rules": [
        {
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "description_template": null,
            "settings": [
                {
                    "name": "x_amount",
                    "type": "number",
                    "value": "10"
                },
                {
                    "name": "flat_price",
                    "type": "number",
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
                    "type": "text",
                    "value": "4 Danbury court"
                }
            ]
        }
    ],
    "id": "merchant_shipping_rules",
    "document_type": "merchant_shipping_rules"
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
    "merchant_id": "ZEMBC",
    "shipping_rules": [
        {
            "rule_code": "free_shipping_over_x_amount_or_flat",
            "name": "Free shipping over x amount, otherwisee flat price",
            "description": "Free shipping over x amount, otherwisee flat price",
            "description_template": null,
            "settings": [
                {
                    "name": "x_amount",
                    "type": "number",
                    "value": "10"
                },
                {
                    "name": "flat_price",
                    "type": "number",
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
                    "type": "text",
                    "value": "4 Danbury court"
                }
            ]
        }
    ]
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/orders" %}
{% api-method-summary %}
Get a list of merchant orders
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="continuation\_token" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
5\(default\)
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
submitted, processing, processed, shipped
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
        *merchant_order_1,
        *merchant_order_2
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantOrderId" %}
{% api-method-summary %}
Get a Merchant Order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantOrderId" type="string" required=true %}

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
    "jielong_id": "70a5399e-486f-4afc-93c1-e7c09608d705",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 10.0,
    "tax_amount": 1.3,
    "shipping_method": "pickup",
    "shipping_method_name": "pickup",
    "shipping_method_description": "pickup",
    "shipping_amount": 0.0,
    "total_amount": 11.3,
    "is_tax_included": true,
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
    "created_at": "2020-07-08T18:17:20.6005Z",
    "updated_at": "2020-07-08T18:17:28.5232331Z",
    "status": "submitted",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": null,
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10.0,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "merchant_order_number": "BSCM1-ZEMBC-271",
    "refunded": false,
    "is_cancellation_in_order": false,
    "id": "mo-70a5399e-486f-4afc-93c1-e7c09608d705",
    "document_type": "merchant_order",
    "_etag": "\"9d025a95-0000-0200-0000-5f060dd40000\""
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantOrderId/shipping" %}
{% api-method-summary %}
Get shipping information of the merchant order with remaining items
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantOrderId" type="string" required=true %}

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
    "jielong_id": "70a5399e-486f-4afc-93c1-e7c09608d705",
    "merchant_order_number": "BSCM1-ZEMBC-271",
    "shippments": [
        {
            "jielong_id": "70a5399e-486f-4afc-93c1-e7c09608d705",
            "tracking_number": "test",
            "carrier": "canada_post",
            "sent_at": "2020-07-16T14:25:38.4449487Z",
            "expect_delivered_at": "0001-01-01T00:00:00",
            "updated_at": "2020-07-16T14:25:38.4436536Z",
            "shipped_items": [
                {
                    "bcin": "SAMUVRY",
                    "sku": "SAMUVRY",
                    "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
                    "quantity": 1,
                    "image_url": null,
                    "list_price": 10.0,
                    "sale_price": null,
                    "merchant_id": "beeshop",
                    "tax_code": null,
                    "weight": 0.0
                }
            ],
            "shipping_method": null,
            "tracking_infos": null,
            "flag": "fully_shipped",
            "carrier_img_url": "https://media.beeshop.chat/asset/carrier/CanadaPost.png",
            "carrier_tracking_url": "https://www.canadapost.ca/trackweb/en#/details/test",
            "id": "6b6f8316-9db5-47b3-994d-5bfcef657ac1",
            "document_type": "order_shipping_info",
            "_etag": "\"6000c65e-0000-0200-0000-5f1063640000\""
        }
    ],
    "remainning_items": [
        {
            "bcin": "SAMUVRY",
            "sku": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 0,
            "image_url": null,
            "list_price": 10.0,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": null,
            "weight": 0.0
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantOrderId/shipping" %}
{% api-method-summary %}
create a new shipment of merchant order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantOrderId" type="string" required=true %}

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
    "id": "41e08e12-fbd5-4777-84e7-578c2589ad68",
    "jielong_id": "7d9fc8ba-01e3-4803-8f61-7d26d9f83a43",
    "tracking_number": "test",
    "carrier": "canada_post",
    "sent_at": "2020-07-16T18:15:38.4870005Z",
    "expect_delivered_at": "0001-01-01T00:00:00",
    "updated_at": "2020-07-16T18:15:35.3421946Z",
    "shipped_items": [
        {
            "bcin": "SAMUVRY",
            "sku": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": null,
            "weight": 0
        }
    ],
    "shipping_method": null,
    "tracking_infos": null,
    "flag": "fully_shipped",
    "carrier_img_url": "https://media.beeshop.chat/asset/carrier/CanadaPost.png",
    "carrier_tracking_url": "https://www.canadapost.ca/trackweb/en#/details/test",
    "document_type": "order_shipping_info"
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
"jielong_id":"7d9fc8ba-01e3-4803-8f61-7d26d9f83a43",
"tracking_number":"test",
"carrier":"canada_post", //supported carrier: canada_post or pickup
"shipped_items":[
      {
            "bcin": "SAMUVRY",
            "sku": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10.0,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": null,
            "weight": 0.0
        }
]
}
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantOrderId/cancel" %}
{% api-method-summary %}
cancel remaining item of merchant order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantOrderId" type="string" required=true %}

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
    "id": "41e08e12-fbd5-4777-84e7-578c2589ad68",
    "jielong_id": "7d9fc8ba-01e3-4803-8f61-7d26d9f83a43",
    "tracking_number": "test",
    "carrier": "canada_post",
    "sent_at": "2020-07-16T18:15:38.4870005Z",
    "expect_delivered_at": "0001-01-01T00:00:00",
    "updated_at": "2020-07-16T18:15:35.3421946Z",
    "shipped_items": [
        {
            "bcin": "SAMUVRY",
            "sku": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": null,
            "weight": 0
        }
    ],
    "shipping_method": null,
    "tracking_infos": null,
    "flag": "cancelled",
    "carrier_img_url": "https://media.beeshop.chat/asset/carrier/CanadaPost.png",
    "carrier_tracking_url": "https://www.canadapost.ca/trackweb/en#/details/test",
    "document_type": "order_shipping_info"
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/search/orders" %}
{% api-method-summary %}
Search merchant orders
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "total": 6,
    "hits": [
        order1,
        order2,
        ...
    ]
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

Request body

```text
{
    "keyword":"Danbury", //leave empty in the keyword will return all records 
                         //matched the filter
    "size":50,
    "from":0,
    "filters": [
        {
            "field":"status",
            "value":"submitted|new", //mutliple values are accepted
            "option":"terms"         //options:
                                     //    terms - for multiple values
                                     //    match - for matching array 
                                     //    term  - for single value (default)
        }
    ]
}
```

Keyword is searched within 

```text
"email",
"merchant_order_number",
"shipping_address.full_name",
"shipping_address.first_name",
"shipping_address.last_name",
"shipping_address.street_1",
"shipping_address.postal_code",
"shipping_address.phone",
"line_items.bcin"
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantorderId/address" %}
{% api-method-summary %}
Update merchant order - shipping address
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantOrderId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

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

```
{
 merchant_order*
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

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
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
    "shipping_method":"pickup",
    "shipping_method_name":"pickup",
    "shipping_method_description":"description"
}
```

{% api-method method="patch" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantorderId/shipping/:shipmentId" %}
{% api-method-summary %}
Update shipment status - received
{% endapi-method-summary %}

{% api-method-description %}
the flag \(status\) will be updated to "received"
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="shipmentId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantOrderId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "id": "6b6f8316-9db5-47b3-994d-5bfcef657ac1",
    "jielong_id": "70a5399e-486f-4afc-93c1-e7c09608d705",
    "tracking_number": "test",
    "carrier": "canada_post",
    "sent_at": "2020-07-16T14:25:38.4449487Z",
    "expect_delivered_at": "0001-01-01T00:00:00",
    "updated_at": "2020-07-30T19:31:08.0742773Z",
    "shipped_items": [
        {
            "bcin": "SAMUVRY",
            "sku": "SAMUVRY",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": null,
            "weight": 0
        }
    ],
    "shipping_method": null,
    "tracking_infos": null,
    "flag": "received",
    "carrier_img_url": "https://media.beeshop.chat/asset/carrier/CanadaPost.png",
    "carrier_tracking_url": "https://www.canadapost.ca/trackweb/en#/details/test",
    "document_type": "order_shipping_info"
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

Request Body

```text
{
    "jielong_id":"39f413f0-176e-44dd-852e-590f994917e5",
    "shipment_id":"6b6f8316-9db5-47b3-994d-5bfcef657ac1",
    "status":"received"
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielongtemplate/:jielongTemplateId" %}
{% api-method-summary %}
Get a Jielong Template
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongTemplateId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authoriazation" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "jielong_template_id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "listed_products": [
        {
            "bcin": "WLL7BXN",
            "title": "Made in Japan / Moritoku Insulated Bento Box Lunch Box (Dark Blue)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-02.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-02.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-02.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-02.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-02.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-03.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-03.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-03.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-03.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-03.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTKLU-02",
            "price": {
                "currency": "CAD",
                "list": 15,
                "msrp": 17.25,
                "cost": null,
                "gb_price": 10.09
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689592Z",
            "stay_on_top": true
        },
        {
            "bcin": "U9PES6J",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Pink)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/U9PES6J-4964549037650-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/U9PES6J-4964549037650-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/U9PES6J-4964549037650-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/U9PES6J-4964549037650-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/U9PES6J-4964549037650-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-4",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689597Z",
            "stay_on_top": true
        },
        {
            "bcin": "R7R923V",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Black)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/R7R923V-4964549037667-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/R7R923V-4964549037667-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/R7R923V-4964549037667-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/R7R923V-4964549037667-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/R7R923V-4964549037667-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-5",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689601Z",
            "stay_on_top": true
        }
    ],
    "name": "Hot hot hot!",
    "description": "HOT HOT HOT",
    "image": "https://bc01dmedia.blob.core.windows.net/jielong-image/template-7f835c4b-3e53-4823-bbbe-ae224382c73d-backup.png",
    "updated_at": "2020-10-19T18:11:40.0689603Z",
    "id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "document_type": "merchant_jielong_template"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielongtemplatelist" %}
{% api-method-summary %}
Get a list of jielong template
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="continuation\_token" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
default = 5
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "has_more": true,
    "continuation_token": "eyJ0b2tlbiI6IitSSUQ6fmRob1hBTG9GUlNaREF3QUFBQUFBQUE9PSNSVDoxI1RSQzo1I1JURDowYm5JR2FpV2xDZ2lTdzNva1VxWkJUTXhNekV1TVRrdU1UVlZNamc3TkRjN05Ea3ZPVGN4TkRvME0xc0EjSVNWOjIjSUVPOjY1NTUxI0ZQQzpBZ0VBQUFBRUFFRUQrUUE9IiwicmFuZ2UiOnsibWluIjoiIiwibWF4IjoiRkYifX0=",
    "results": [
        jielong_template_1,
        jielong_template_2,
    ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielongtemplate" %}
{% api-method-summary %}
Create a Jielong Template
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "jielong_template_id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "listed_products": [
        {
            "bcin": "WLL7BXN",
            "title": "Made in Japan / Moritoku Insulated Bento Box Lunch Box (Dark Blue)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-02.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-02.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-02.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-02.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-02.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-03.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-03.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-03.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-03.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-03.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTKLU-02",
            "price": {
                "currency": "CAD",
                "list": 15,
                "msrp": 17.25,
                "cost": null,
                "gb_price": 10.09
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689592Z",
            "stay_on_top": true
        },
        {
            "bcin": "U9PES6J",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Pink)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/U9PES6J-4964549037650-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/U9PES6J-4964549037650-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/U9PES6J-4964549037650-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/U9PES6J-4964549037650-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/U9PES6J-4964549037650-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-4",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689597Z",
            "stay_on_top": true
        },
        {
            "bcin": "R7R923V",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Black)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/R7R923V-4964549037667-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/R7R923V-4964549037667-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/R7R923V-4964549037667-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/R7R923V-4964549037667-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/R7R923V-4964549037667-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-5",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689601Z",
            "stay_on_top": true
        }
    ],
    "name": "Hot hot hot!",
    "description": "HOT HOT HOT",
    "image": "https://bc01dmedia.blob.core.windows.net/jielong-image/template-7f835c4b-3e53-4823-bbbe-ae224382c73d-backup.png",
    "updated_at": "2020-10-19T18:11:40.0689603Z",
    "id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "document_type": "merchant_jielong_template"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request Body

```text
{
  "merchant_id": "beeshop",
  "name":"Jielong Template 1",
  "description":"first jielong template",
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

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielongtemplate/:jielongTemplateId" %}
{% api-method-summary %}
Update a Jielong Template
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongTemplateId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "jielong_template_id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "listed_products": [
        {
            "bcin": "WLL7BXN",
            "title": "Made in Japan / Moritoku Insulated Bento Box Lunch Box (Dark Blue)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-02.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-02.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-02.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-02.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-02.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-03.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-03.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-03.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-03.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-03.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTKLU-02",
            "price": {
                "currency": "CAD",
                "list": 15,
                "msrp": 17.25,
                "cost": null,
                "gb_price": 10.09
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689592Z",
            "stay_on_top": true
        },
        {
            "bcin": "U9PES6J",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Pink)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/U9PES6J-4964549037650-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/U9PES6J-4964549037650-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/U9PES6J-4964549037650-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/U9PES6J-4964549037650-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/U9PES6J-4964549037650-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-4",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689597Z",
            "stay_on_top": true
        },
        {
            "bcin": "R7R923V",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Black)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/R7R923V-4964549037667-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/R7R923V-4964549037667-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/R7R923V-4964549037667-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/R7R923V-4964549037667-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/R7R923V-4964549037667-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-5",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689601Z",
            "stay_on_top": true
        }
    ],
    "name": "Hot hot hot!",
    "description": "HOT HOT HOT",
    "image": "https://bc01dmedia.blob.core.windows.net/jielong-image/template-7f835c4b-3e53-4823-bbbe-ae224382c73d-backup.png",
    "updated_at": "2020-10-19T18:11:40.0689603Z",
    "id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "document_type": "merchant_jielong_template"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
  "merchant_id": "beeshop", //required
  "name":"Jielong Template 1", //optional
  "description":"second jielong template", //optional
   "listed_products": [  //optional
      {
      "bcin":"SAMUVRY",
      "merchant_id":"beeshop"
      }
    ]
}
```

{% api-method method="delete" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielongtemplate/:jielongTemplateId" %}
{% api-method-summary %}
Delete a Jielong Template
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongTemplateId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
deleted
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/jielongtemplate/:jielongTemplateId/image" %}
{% api-method-summary %}
Upload a jielong template image
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jielongTemplateId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="image1" type="string" required=true %}
path to image
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "merchant_id": "beeshop",
    "merchant_name": "Beeshop",
    "jielong_template_id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "listed_products": [
        {
            "bcin": "WLL7BXN",
            "title": "Made in Japan / Moritoku Insulated Bento Box Lunch Box (Dark Blue)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-02.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-02.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-02.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-02.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-02.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                },
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/WLL7BXN-4964549034123-03.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/WLL7BXN-4964549034123-03.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/WLL7BXN-4964549034123-03.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/WLL7BXN-4964549034123-03.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/WLL7BXN-4964549034123-03.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTKLU-02",
            "price": {
                "currency": "CAD",
                "list": 15,
                "msrp": 17.25,
                "cost": null,
                "gb_price": 10.09
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689592Z",
            "stay_on_top": true
        },
        {
            "bcin": "U9PES6J",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Pink)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/U9PES6J-4964549037650-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/U9PES6J-4964549037650-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/U9PES6J-4964549037650-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/U9PES6J-4964549037650-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/U9PES6J-4964549037650-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-4",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689597Z",
            "stay_on_top": true
        },
        {
            "bcin": "R7R923V",
            "title": "Moritoku Tritan Leak-Proofed One-Touch Water Bottle 500ML (Black)",
            "media": [
                {
                    "url": "https://bc01dmedia.blob.core.windows.net/product-image/R7R923V-4964549037667-01.jpg",
                    "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/R7R923V-4964549037667-01.jpg",
                    "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/R7R923V-4964549037667-01.jpg",
                    "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/R7R923V-4964549037667-01.jpg",
                    "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/R7R923V-4964549037667-01.jpg",
                    "type": "image/jpeg",
                    "order": 9999
                }
            ],
            "language": "en",
            "unit": "",
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "sku": "MTWBL-5",
            "price": {
                "currency": "CAD",
                "list": 7.01,
                "msrp": 8.06,
                "cost": null,
                "gb_price": 4.71
            },
            "listed_by": "template",
            "listed_at": "2020-10-19T18:11:40.0689601Z",
            "stay_on_top": true
        }
    ],
    "name": "Hot hot hot!",
    "description": "HOT HOT HOT",
    "image": "https://bc01dmedia.blob.core.windows.net/jielong-image/template-7f835c4b-3e53-4823-bbbe-ae224382c73d-backup.png",
    "updated_at": "2020-10-19T18:11:40.0689603Z",
    "id": "7f835c4b-3e53-4823-bbbe-ae224382c73d",
    "document_type": "merchant_jielong_template"
}
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/merchantorder/:merchantOrderId/pickinglist" %}
{% api-method-summary %}
Get merchant order picking list
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantOrderid" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "jielong_id": "70a5399e-486f-4afc-93c1-e7c09608d705",
    "user_id": "mjiang2000@gmail.com",
    "email": "mjiang2000@gmail.com",
    "base_amount": 10.0,
    "tax_amount": 1.3,
    "shipping_method": "free_shipping_over_x_amount_or_flat",
    "shipping_method_name": "free shipping over $75",
    "shipping_method_description": "3-11 days, free shipping over $75",
    "shipping_amount": 0.0,
    "total_amount": 11.3,
    "is_tax_included": true,
    "billing_address": {
        "id": null,
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
        "email": "mjiang2000@hotmail.com",
        "is_default": false
    },
    "shipping_address": {
        "id": null,
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "7 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "ON",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com",
        "is_default": false
    },
    "created_at": "2020-07-08T18:17:20.6005Z",
    "updated_at": "2020-07-08T18:17:28.5232331Z",
    "status": "shipped",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": null,
    "line_items": [
        {
            "ajin": "SAMUVRY",
            "sku": "MT-AC-01",
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 1,
            "image_url": null,
            "list_price": 10.0,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": "regular",
            "weight": 0.0,
            "stock_location": {
                "aisle": "",
                "bay": "",
                "shelf": "",
                "bin": ""
            }
        }
    ],
    "merchant_order_number": "BSCM1-ZEMBC-271",
    "refunded": false,
    "is_cancellation_in_order": false
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

```text
NOTE: Each line item has stock location info, which is major difference 
comparing to normal line item in the merchant order object.

  "stock_location": {
                "aisle": "",
                "bay": "",
                "shelf": "",
                "bin": ""
            }
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/merchant/v1" path="/merchant/:merchantId/search/customerorders" %}
{% api-method-summary %}
Search customer order
{% endapi-method-summary %}

{% api-method-description %}
this search has a default filter which is set to micro merchant id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

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

```
{
    "total": 2,
    "hits": [
        {
            "order_id": "d0787200-5aa1-4848-ba47-d90eefedbd5d",
            "user_id": "mjiang2000@gmail.com",
            "jielong_id": "4c65b551-365c-4d17-a136-86b0bfee8b27",
            "email": "mjiang2000@gmail.com",
            "user_name": null,
            "micro_merchant_id": "ZEMBC",
            "micro_merchant_name": "mjiang2000@gmail.com",
            "merchant_id": "pennystore",
            "merchant_name": "Penny Store",
            "line_items": [
                {
                    "bcin": "SAMUVRY",
                    "sku": null,
                    "title": null,
                    "quantity": 2,
                    "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/SAMUVRY-4991087345671-01.jpg",
                    "list_price": 0.01,
                    "sale_price": null,
                    "merchant_id": "pennystore",
                    "tax_code": "regular",
                    "weight": 0.0
                }
            ],
            "base_amount": 0.02,
            "shipping_method": null,
            "shipping_method_name": null,
            "shipping_method_description": null,
            "shipping_amount": 0.0,
            "total_amount": 0.02,
            "billing_address": null,
            "shipping_address": null,
            "created_at": "2020-10-27T16:16:45.4414159Z",
            "updated_at": "2020-10-27T16:18:54.4878575Z",
            "status": "new",
            "payment_id": null,
            "payment_gateway": null,
            "payment_provider": null,
            "order_number": "BSC1-1501",
            "notes": null,
            "bc_pay_enabled": false,
            "refunded": false,
            "id": "d0787200-5aa1-4848-ba47-d90eefedbd5d",
            "document_type": "order",
            "_etag": "\"020060a7-0000-0200-0000-5f9848710000\"",
            "_rid": "dhoXAO3AhMqzBAAAAAAAAA==",
            "_self": "dbs/dhoXAA==/colls/dhoXAO3AhMo=/docs/dhoXAO3AhMqzBAAAAAAAAA==/",
            "_attachments": "attachments/",
            "_lsn": 7155340,
            "_ts": 1603815537
        },
        {
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
            "id": "3cd78d1e-fe4b-4807-b80a-3262c835cf25",
            "document_type": "order",
            "_etag": "\"b6009835-0000-0200-0000-5f9cbf3b0000\"",
            "_rid": "dhoXAO3AhMrsBAAAAAAAAA==",
            "_self": "dbs/dhoXAA==/colls/dhoXAO3AhMo=/docs/dhoXAO3AhMrsBAAAAAAAAA==/",
            "_attachments": "attachments/",
            "_lsn": 7371222,
            "_ts": 1604108091
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
{
    "keyword":"",
    "size":50,
    "from":0,
    "filters": [
         {
            "field":"status",
            "value":"submitted|new",
            "option":"terms"
        }
    ]
}
```

