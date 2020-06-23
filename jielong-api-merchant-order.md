# Jielong API - Merchant Order

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/group/v1" path="/jielong/:jielongId/merchantOrder" %}
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
    "jielong_id": "77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "user_id": "mjiang2000@gmail.com",
    "micro_merchant_id": "ZEMBC",
    "email": "mjiang2000@gmail.com",
    "base_amount": 0.0,
    "tax_amount": 0.0,
    "shipping_method": null,
    "shipping_method_name": null,
    "shipping_method_description": null,
    "shipping_amount": 0.0,
    "total_amount": 30.0,
    "is_tax_included": false,
    "billing_address": null,
    "shipping_address": null,
    "created_at": "2020-05-25T16:33:42.5759125Z",
    "updated_at": "2020-05-25T16:33:42.6086565Z",
    "status": "new",
    "supplier_merchant_id": "beeshop",
    "supplier_merchant_name": "beeshop",
    "line_items": [
        {
            "bcin": "SAMUVRY",
            "sku": null,
            "title": "Made in Japan / Tempura Paper  天妇罗纸*吸油纸(50 sheets)",
            "quantity": 3,
            "image_url": null,
            "list_price": 10.0,
            "sale_price": null,
            "merchant_id": "beeshop",
            "weight": 0.0
        }
    ],
    "merchant_order_number": null,
    "refunded": false,
    "is_cancellation_in_order": false,
    "id": "mo-77d6ff4d-9659-44af-a87e-16cc08b2ea9a",
    "document_type": "merchant_order",
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

