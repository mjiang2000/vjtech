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

```
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

```
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

```

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

