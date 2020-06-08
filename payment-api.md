---
description: Payment API
---

# Payment API

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/payment/v1" path="/pay" %}
{% api-method-summary %}
Pay 
{% endapi-method-summary %}

{% api-method-description %}
Pay through gateway directly by credit card or tokenized cc
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "payment_id": "0fdb1f3c-916e-4f67-a0f8-7f6353d7ac4d",
    "payment_gateway": "Spreedly",
    "payment_provider": "VISA",
    "external_payment_id": "kbDECr7Wbcn3EERO1nZxWatLDs",
    "total_amount": 0.01,
    "currency": "CAD",
    "order_id": "577b066f-a30f-40a4-8951-077e2af1dadf",
    "status": "succeeded",
    "updated_at": "2020-06-08T02:38:44.5920924Z",
    "extra_info_from_gateway": "411111 - 1111",
    "gateway_type": "test",
    "trans_id": null,
    "external_transaction_settle_time": "2020-06-08T02:38:44Z",
    "id": "1b0b5ddb-ca6f-4648-b5a7-3daa9e2ef805",
    "document_type": "payment"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
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

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
Invalid request
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

by tokenized CC, through Spreedly

```text
{
    "order_id":"9b1579d5-4cc5-4df5-b5e2-32d7671a8e10",
    "payment_provider":"CC",
    "total_amount":0.01,
    "currency":"CAD",
    "description":"test",
    "payment_token":"C72jBTpIBfMXsQyVIOF7XuRvjnq"
 }
```

By CC number, through Moneris

```text
{
    "order_id":"9b1579d5-4cc5-4df5-b5e2-32d7671a8e10",
    "payment_provider":"UNIONPAY",
    "total_amount":0.01,
    "currency":"CAD",
    "description":"test",
    "card_number":"6250944000000771",
    "expiry_date":"4912",
    "cvd":"371"
 }
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/payment/v1" path="/pay/prepare" %}
{% api-method-summary %}
Prepare Pay
{% endapi-method-summary %}

{% api-method-description %}
Pay through 3rd party payment by redirect to the payment provider's web pages or SDK  
1\)Wechat pay \(mobile only\)  
2\)Alipay \(mobile and web\)  
3\)Unionpay \(web only\)  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
    "order_payment_id": "998fa09c-683e-4bba-a95a-9a15d3747fd8",
    "order_id": "20200608-01D2-4F0F-96E2-4CFCCAA8B823",
    "payment_provider": "ALIPAY",
    "total_amount": 0.01,
    "currency": "CAD",
    "description": "test",
    "external_payment_id": "TA120000571200608000002",
    "payment_token": "_input_charset=\"utf-8\"&appenv=\"null\"&currency=\"CAD\"&forex_biz=\"FP\"&notify_url=\"https://pbs.snappay.ca/api/alipay/notice/\"&out_trade_no=\"TA120000571200608000002\"&partner=\"2088821431374179\"&payment_type=\"1\"&product_code=\"NEW_WAP_OVERSEAS_SELLER\"&refer_url=\"http://example.com\"&secondary_merchant_id=\"902000057124\"&secondary_merchant_industry=\"7299\"&secondary_merchant_name=\"Beeshop Solutions Inc\"&seller_id=\"2088821431374179\"&service=\"mobile.securitypay.pay\"&subject=\"order:20200608-01D2-4F0F-96E2-4CFCCAA8B823\"&total_fee=\"0.01\"&sign=\"RO7olR1TNuzOz1U90BWz92sfjlKTieHtXG9gjzSCkVn7I7fACcBhEwCMiBX4rGekALb0A%2FXgjDf5qDLSQKDVz7ztgX4taRXgrSOMnzfjeGTWDojgu8dnNgfeF45HOKsjKPLs6F4T5NYdUc7aRWHo7Sn%2BjQyQucM6EYZVrdWxkEM%3D\"&sign_type=\"RSA\"",
    "second_payment_token": null
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

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
Invalid input
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

By web

```text
{
	"order_id":"20200608-01D2-4F0F-96E2-4CFCCAA8B823",
    "payment_provider":"ALIPAY",
    "total_amount":0.01,
    "currency":"CAD",
    "description":"test",
    "device_type": "web",
    "return_url": "http://example.com"
}
```

By Mobile

```text
{
	"order_id":"20200608-01D2-4F0F-96E2-4CFCCAA8B823",
    "payment_provider":"ALIPAY",
    "total_amount":0.01,
    "currency":"CAD",
    "description":"test",
    "device_type": "mobile",
    "return_url": "http://example.com"
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/payment/v1" path="/pay/status/order/{orderId}/payment/{orderPaymentId}" %}
{% api-method-summary %}
Query Payment status
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="orderPaymentId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="orderId" type="string" required=true %}

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
    "payment_id": "0fdb1f3c-916e-4f67-a0f8-7f6353d7ac4d",
    "payment_gateway": "Spreedly",
    "payment_provider": "VISA",
    "external_payment_id": "kbDECr7Wbcn3EERO1nZxWatLDs",
    "total_amount": 0.01,
    "currency": "CAD",
    "order_id": "577b066f-a30f-40a4-8951-077e2af1dadf",
    "status": "succeeded",
    "updated_at": "2020-06-08T02:38:44.5920924Z",
    "extra_info_from_gateway": "411111 - 1111",
    "gateway_type": "test",
    "trans_id": null,
    "external_transaction_settle_time": "2020-06-08T02:38:44Z",
    "id": "1b0b5ddb-ca6f-4648-b5a7-3daa9e2ef805",
    "document_type": "payment"
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/payment/v1" path="/refund/micromerchant/{microMerchantId}" %}
{% api-method-summary %}
Refund
{% endapi-method-summary %}

{% api-method-description %}
Refund can only be executed as a micro merchant who own's the Campaign
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="microMerchantId" type="string" required=true %}

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
    "refund_id": "61cc6a13-9d8d-48e5-b55e-a14f23e04b7d",
    "refund_gateway": "Spreedly",
    "refund_provider": "VISA",
    "external_refund_id": "CAXS8rG7pAB8eEY3QRDO1tTxBxz",
    "total_amount": 0.01,
    "currency": "CAD",
    "order_id": "577b066f-a30f-40a4-8951-077e2af1dadf",
    "order_amendment_id": "4e0e412e-40f9-4dd0-8cb5-8fa08f8ef6ee",
    "status": "succeeded",
    "updated_at": "2020-06-08T02:57:40.8192629Z",
    "extra_info_from_gateway": null,
    "original_payment_id": "0fdb1f3c-916e-4f67-a0f8-7f6353d7ac4d",
    "original_external_payment_id": "kbDECr7Wbcn3EERO1nZxWatLDs",
    "description": "refund",
    "external_transaction_settle_time": "2020-06-08T02:58:08Z",
    "id": "7851a7a9-2c2d-49d6-8ce8-228b69d1de42",
    "document_type": "refund"
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

Request Body

* Order amendment have to be generated before the refund can be process. 
* Micro merchant is response for creating an order amendment up on request by the jielong user
* Successful refund will mark the order amendment as refunded
* Only Beeshop pay enabled order can be refund

```text
{
    "order_id":"577b066f-a30f-40a4-8951-077e2af1dadf",
    "order_amendment_id":"4e0e412e-40f9-4dd0-8cb5-8fa08f8ef6ee",
    "total_amount":0.01,
    "currency":"CAD",
    "description":"refund"
 }
```

