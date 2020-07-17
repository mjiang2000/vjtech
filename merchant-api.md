---
description: about merchant from git
---

# Merchant API

Merchant API

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

