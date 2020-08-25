---
description: Merchant order related API
---

# Jielong API - Merchant Order

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantorder" %}
{% api-method-summary %}
Get a Merchant Order by Jielong Id
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "jielong_id": "4020e479-2015-4234-b39b-09c94f133b07",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 42.84,
    "tax_amount": 2.14,
    "shipping_method": "pickup",
    "shipping_method_name": "In Store Pickup",
    "shipping_method_description": "Mon-Fri 9AM-5PM\n162 Torbay Rd., Markham, ON L3R 1G6",
    "shipping_amount": 0.0,
    "total_amount": 44.98,
    "is_tax_included": true,
    "billing_address": {
        "id": null,
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "7 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "BC",
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
        "province": "BC",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com",
        "is_default": false
    },
    "created_at": "2020-08-25T16:15:07.6588348Z",
    "updated_at": "2020-08-25T17:49:23.83497Z",
    "status": "new",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "9KBZJAL",
            "sku": null,
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
            "quantity": 2,
            "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
            "list_price": 21.42,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "merchant_order_number": null,
    "refunded": false,
    "is_cancellation_in_order": false,
    "ibv_enabled": false,
    "ibv_rate": 0.2,
    "payment_received": 54.84,
    "payment_refunded": 0.0,
    "transaction_fee": 0.0,
    "total_payout": 9.86,
    "id": "mo-4020e479-2015-4234-b39b-09c94f133b07",
    "document_type": "merchant_order"
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantorderpreview" %}
{% api-method-summary %}
Get a Merchant order preview
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantorder/shippingaddress" %}
{% api-method-summary %}
Update Merchant order Address
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "jielong_id": "4020e479-2015-4234-b39b-09c94f133b07",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 42.84,
    "tax_amount": 2.14,
    "shipping_method": "pickup",
    "shipping_method_name": "In Store Pickup",
    "shipping_method_description": "Mon-Fri 9AM-5PM\n162 Torbay Rd., Markham, ON L3R 1G6",
    "shipping_amount": 0.0,
    "total_amount": 44.98,
    "is_tax_included": true,
    "billing_address": {
        "id": null,
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "7 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "BC",
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
        "province": "BC",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com",
        "is_default": false
    },
    "created_at": "2020-08-25T16:15:07.6588348Z",
    "updated_at": "2020-08-25T17:49:23.83497Z",
    "status": "new",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "9KBZJAL",
            "sku": null,
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
            "quantity": 2,
            "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
            "list_price": 21.42,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "merchant_order_number": null,
    "refunded": false,
    "is_cancellation_in_order": false,
    "ibv_enabled": false,
    "ibv_rate": 0.2,
    "payment_received": 54.84,
    "payment_refunded": 0.0,
    "transaction_fee": 0.0,
    "total_payout": 9.86,
    "id": "mo-4020e479-2015-4234-b39b-09c94f133b07",
    "document_type": "merchant_order"
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantOrder/shippingquotes" %}
{% api-method-summary %}
Get a Merchant Order shipping quotes
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
            "rule_code": "pickup",
            "name": "pickup",
            "description": "pickup",
            "settings": [
                {
                    "name": "pickup_address",
                    "value": ""
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

{% api-method method="patch" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/shippingmethod" %}
{% api-method-summary %}
Update shipping method of a Merchant Order
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "id": "mo-39f413f0-176e-44dd-852e-590f994917e5",
    "_rid": "dhoXAO3AhMqRAAAAAAAAAA==",
    "_self": "dbs/dhoXAA==/colls/dhoXAO3AhMo=/docs/dhoXAO3AhMqRAAAAAAAAAA==/",
    "_ts": 1592875660,
    "_etag": "\"3c00d455-0000-0200-0000-5ef15a8c0000\"",
    "jielong_id": "39f413f0-176e-44dd-852e-590f994917e5",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 10,
    "tax_amount": 1.3,
    "shipping_method": "pickup",
    "shipping_method_name": "pickup",
    "shipping_method_description": "pickup",
    "shipping_amount": 10,
    "total_amount": 21.3,
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
    "created_at": "2020-06-23T00:58:50.6652118Z",
    "updated_at": "2020-06-23T00:59:13.765005Z",
    "status": "new",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": null,
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
            "tax_code": null,
            "weight": 0
        }
    ],
    "merchant_order_number": "BSCM1-ZEMBC-145",
    "refunded": false,
    "is_cancellation_in_order": false,
    "document_type": "merchant_order"
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
        "shipping_amount": 10,
        "shipping_method": "pickup",
        "shipping_method_name": "pickup",
        "shipping_method_description": "pickup"
     }
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantOrder/calculation" %}
{% api-method-summary %}
Calculate a merchant order
{% endapi-method-summary %}

{% api-method-description %}
This API should be called to get most up to date total amount when display the order review page before final submit
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "jielong_id": "4020e479-2015-4234-b39b-09c94f133b07",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 42.84,
    "tax_amount": 2.14,
    "shipping_method": "pickup",
    "shipping_method_name": "In Store Pickup",
    "shipping_method_description": "Mon-Fri 9AM-5PM\n162 Torbay Rd., Markham, ON L3R 1G6",
    "shipping_amount": 0.0,
    "total_amount": 44.98,
    "is_tax_included": true,
    "billing_address": {
        "id": null,
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "7 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "BC",
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
        "province": "BC",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com",
        "is_default": false
    },
    "created_at": "2020-08-25T16:15:07.6588348Z",
    "updated_at": "2020-08-25T17:49:23.83497Z",
    "status": "new",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "9KBZJAL",
            "sku": null,
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
            "quantity": 2,
            "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
            "list_price": 21.42,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "merchant_order_number": null,
    "refunded": false,
    "is_cancellation_in_order": false,
    "ibv_enabled": false,
    "ibv_rate": 0.2,
    "payment_received": 54.84,
    "payment_refunded": 0.0,
    "transaction_fee": 0.0,
    "total_payout": 9.86,
    "id": "mo-4020e479-2015-4234-b39b-09c94f133b07",
    "document_type": "merchant_order"
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

{% api-method method="patch" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantOrder/submit" %}
{% api-method-summary %}
submit a merchant order
{% endapi-method-summary %}

{% api-method-description %}
This API should be called to submit the order to supplier merchant. It will kick off the merchant order process automatically. Merchant order can only be submitted once. 
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "id": "mo-39f413f0-176e-44dd-852e-590f994917e5",
    "jielong_id": "39f413f0-176e-44dd-852e-590f994917e5",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 10,
    "tax_amount": 1.3,
    "shipping_method": "pickup",
    "shipping_method_name": "pickup",
    "shipping_method_description": "pickup",
    "shipping_amount": 0,
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
    "created_at": "2020-06-23T00:58:50.6652118Z",
    "updated_at": "2020-06-23T00:59:13.765005Z",
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
            "list_price": 10,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": null,
            "weight": 0
        }
    ],
    "merchant_order_number": "BSCM1-ZEMBC-145",
    "refunded": false,
    "is_cancellation_in_order": false,
    "document_type": "merchant_order"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
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

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantorder/ibv/{switch}" %}
{% api-method-summary %}
Enable IBV price of merchant order
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="switch" type="string" required=true %}
y/n
{% endapi-method-parameter %}

{% api-method-parameter name="jielongId" type="string" required=true %}
jielong Id
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
    "jielong_id": "4020e479-2015-4234-b39b-09c94f133b07",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 42.84,
    "tax_amount": 2.14,
    "shipping_method": "pickup",
    "shipping_method_name": "In Store Pickup",
    "shipping_method_description": "Mon-Fri 9AM-5PM\n162 Torbay Rd., Markham, ON L3R 1G6",
    "shipping_amount": 0.0,
    "total_amount": 44.98,
    "is_tax_included": true,
    "billing_address": {
        "id": null,
        "full_name": "Jack Jiang",
        "first_name": null,
        "Last_name": null,
        "company_name": null,
        "street_1": "7 Danbury court",
        "street_2": null,
        "city": "Markham",
        "country": "Canada",
        "province": "BC",
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
        "province": "BC",
        "postal_code": "L3R7S1",
        "phone": "416-2728539",
        "email": "mjiang2000@hotmail.com",
        "is_default": false
    },
    "created_at": "2020-08-25T16:15:07.6588348Z",
    "updated_at": "2020-08-25T17:49:23.83497Z",
    "status": "new",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": "Beeshop",
    "line_items": [
        {
            "bcin": "9KBZJAL",
            "sku": null,
            "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
            "quantity": 2,
            "image_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/9KBZJAL-4964549034550-01.jpg",
            "list_price": 21.42,
            "sale_price": null,
            "merchant_id": "beeshop",
            "tax_code": "regular",
            "weight": 0.0
        }
    ],
    "merchant_order_number": null,
    "refunded": false,
    "is_cancellation_in_order": false,
    "ibv_enabled": false,
    "ibv_rate": 0.2,
    "payment_received": 54.84,
    "payment_refunded": 0.0,
    "transaction_fee": 0.0,
    "total_payout": 9.86,
    "id": "mo-4020e479-2015-4234-b39b-09c94f133b07",
    "document_type": "merchant_order"
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

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
"merchant order is not valid to update"
"IBV price is not supported by supplier merchant"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

