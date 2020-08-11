# Product API

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/product/:bcin" %}
{% api-method-summary %}
Get a product
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="bcin" type="string" required=true %}
bcin aka product id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "merchant_id": "beeshop",
    "merchant_name": "beeshop",
    "sku": "B0369",
    "stock_location": {
        "aisle": "",
        "bay": "",
        "shelf": "",
        "bin": ""
    },
    "selll_without_inventory": true,
    "bcin": "9KBZJAL",
    "title": "Made in Japan / Moritoku Traditional Japanese Ceramic Plate (5-piece set)",
    "brand": "Moritoku",
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
    "gtin": "4964549034550",
    "active": true,
    "unit": null,
    "description": "TRADITIONAL AUTHENTIC STYLE: Our plate set features an authentic Japanese style.  Hand-crafted from thick, durable and restaurant-grade ceramic material.\nGreat tableware to serve your family and guests with. With these beautiful dishwares, your home cooked meals can feel like you are eating out at a fancy restaurant.\nMULTI-FUNCTIONAL: Designed to enhance the dining experience of Asian inspired foods (Thai curries, noodle dishes, dumplings, fried rice, stir fry, chow mein, laksa, etc). Use also for cereals, popcorn, oatmeal, etc.\nEASY TO CLEAN: Dishwasher-safe. Simply throw into the top rack of your dishwasher or scrub by hand",
    "created_at": "2020-05-10T01:59:17.2561589Z",
    "updated_at": "2020-05-27T20:01:19.7944375Z",
    "tags": [
        "Ceramic",
        "Made in Japan",
        "Moritoku",
        "Noodle Soup",
        "Plate",
        "Plate Set"
    ],
    "specifications": [
        {
            "section_name": "General",
            "properties": [
                {
                    "name": "Dishwasher",
                    "value": " Safe"
                },
                {
                    "name": " Product size",
                    "value": " approximate 16.5cm diameter"
                }
            ]
        }
    ],
    "created_by": "mjiang2000@gmail.com",
    "updated_by": "mjiang2000@gmail.com",
    "price": {
        "currency": "CAD",
        "list": 35.0,
        "msrp": 35.0,
        "cost": null,
        "gb_price": 30.0
    },
    "weight": 1.425,
    "id": "beeshop-9KBZJAL",
    "document_type": "product_by_merchant",
    "_etag": "\"2100d2b5-0000-0200-0000-5ecec70f0000\""
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
9KBZJAL1 is not found.
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/productlist" %}
{% api-method-summary %}
Get a list of products
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="language" type="string" required=false %}
en
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}
paginate token
{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="integer" required=false %}
default 10
{% endapi-method-parameter %}

{% api-method-parameter name="merchant\_id" type="string" required=false %}
merchant id
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
    "continuation_token": "eyJ0b2tlbiI6IitSSUQ6fm53SUVBS3VOSzVrNkFRQUFBQUFBQUE9PSNSVDoxI1RSQzoxMDAjSVNWOjIjSUVPOjY1NTUxI0ZQQzpBZ0VBQUFBS0FERUJBUHhoUVA4SEVvQT0iLCJyYW5nZSI6eyJtaW4iOiIiLCJtYXgiOiJGRiJ9fQ==",
    "results": [
        {*product1},
        {*product2}
        ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="merchant/:merchantId/product" %}
{% api-method-summary %}
Create a new product
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
    "merchant_id": "beeshop",
    "merchant_name": "beeshop",
    "sku": "B1326",
    "stock_location": {
        "aisle": "",
        "bay": "",
        "shelf": "",
        "bin": ""
    },
    "selll_without_inventory": true,
    "bcin": "JH8QRQ2",
    "title": "Made in Japan / Moritoku Traditional Japanese Hand Crafted Ceramic Rice Bowl (Lucky Plant 5-piece set)",
    "brand": "Moritoku",
    "media": [
        {
            "url": "https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-01.jpg",
            "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/JH8QRQ2-4964549034598-01.jpg",
            "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/JH8QRQ2-4964549034598-01.jpg",
            "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/JH8QRQ2-4964549034598-01.jpg",
            "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/JH8QRQ2-4964549034598-01.jpg",
            "type": "image/jpeg",
            "order": 9999
        },
        {
            "url": "https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-02.jpg",
            "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/JH8QRQ2-4964549034598-02.jpg",
            "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/JH8QRQ2-4964549034598-02.jpg",
            "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/JH8QRQ2-4964549034598-02.jpg",
            "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/JH8QRQ2-4964549034598-02.jpg",
            "type": "image/jpeg",
            "order": 9999
        }
    ],
    "language": "en",
    "gtin": "4964549034598",
    "categories": [
        {
            "product_category_id": "72",
            "name": "Home and Kitchen",
            "url": null,
            "media": null,
            "path": null,
            "visible": false,
            "sub_categories": null,
            "depth": 0
        }
    ],
    "active": true,
    "unit": null,
    "description": "Besides using it as rice bowl, you can also use it for ice cream, snacks or whatever strikes your fancy\nMade of high quality ceramic and hand painted with traditional Japanese Plant which represents beauty, life and tranquility. The bowls are dishwasher and microwave safe\nThis traditionally crafted ceramic set will fit right in with any home decor with zen elements\nComes with easy packed gift box, a wonderful gift idea. These bowls makes a perfect gift item for house warming, birthdays, wedding, graduation, business gift or almost any occasion.",
    "created_at": "2020-05-10T01:59:18.2552261Z",
    "updated_at": "2020-05-27T20:01:20.2863528Z",
    "tags": [
        "Ceramic",
        "Hand Crafted",
        "Made in Japan",
        "Moritoku",
        "Rice Bowl",
        "Rice Bowl Set"
    ],
    "specifications": [
        {
            "section_name": "General",
            "properties": [
                {
                    "name": "Dishwasher",
                    "value": " Safe"
                },
                {
                    "name": " Product size",
                    "value": " approximate 4.5 inches diameter and 2.5 inches tall"
                }
            ]
        }
    ],
    "created_by": "mjiang2000@gmail.com",
    "updated_by": "mjiang2000@gmail.com",
    "price": {
        "currency": "CAD",
        "list": 33,
        "msrp": 33,
        "cost": null
    },
    "weight": 1.32,
    "id": "beeshop-JH8QRQ2",
    "document_type": "product_by_merchant",
    "_etag": "\"2100d6b5-0000-0200-0000-5ecec7100000\"",
    "_rid": "yVctAP1cTtWFAgAAAAAAAA==",
    "_self": "dbs/yVctAA==/colls/yVctAP1cTtU=/docs/yVctAP1cTtWFAgAAAAAAAA==/",
    "_attachments": "attachments/",
    "_ts": 1590609680
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
invalid request body
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
    "sku": "B1326",
    "stock_location": {
        "aisle": "",
        "bay": "",
        "shelf": "",
        "bin": ""
    },
    "selll_without_inventory": true,
    "title": "Made in Japan / Moritoku Traditional Japanese Hand Crafted Ceramic Rice Bowl (Lucky Plant 5-piece set)",
    "brand": "Moritoku",
    "language": "en", //only support en for now
    "gtin": "4964549034598",
    "active": true,
    "unit": null,
    "description": "Besides using it as rice bowl, you can also use it for ice cream, snacks or whatever strikes your fancy\nMade of high quality ceramic and hand painted with traditional Japanese Plant which represents beauty, life and tranquility. The bowls are dishwasher and microwave safe\nThis traditionally crafted ceramic set will fit right in with any home decor with zen elements\nComes with easy packed gift box, a wonderful gift idea. These bowls makes a perfect gift item for house warming, birthdays, wedding, graduation, business gift or almost any occasion.",
    "tags": [
        "Ceramic",
        "Hand Crafted",
        "Made in Japan",
        "Moritoku",
        "Rice Bowl",
        "Rice Bowl Set"
    ],
    "price": {
        "currency": "CAD",
        "list": 33,
        "msrp": 33,
        "cost": null
    },
    "weight": 1.32
}
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/merchant/:merchantId/product/:bcin" %}
{% api-method-summary %}
Update a existing product
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="bcin" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="skipmedia" type="string" required=false %}
y / n   
y: image information will be reserved  
n: image information will be reset  
default is y
{% endapi-method-parameter %}

{% api-method-parameter name="language" type="string" required=false %}
en \(default\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "merchant_id": "beeshop",
    "merchant_name": "beeshop",
    "sku": "B1326",
    "stock_location": {
        "aisle": "",
        "bay": "",
        "shelf": "",
        "bin": ""
    },
    "selll_without_inventory": true,
    "bcin": "JH8QRQ2",
    "title": "Made in Japan / Moritoku Traditional Japanese Hand Crafted Ceramic Rice Bowl (Lucky Plant 5-piece set)",
    "brand": "Moritoku",
    "media": [
        {
            "url": "https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-01.jpg",
            "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/JH8QRQ2-4964549034598-01.jpg",
            "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/JH8QRQ2-4964549034598-01.jpg",
            "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/JH8QRQ2-4964549034598-01.jpg",
            "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/JH8QRQ2-4964549034598-01.jpg",
            "type": "image/jpeg",
            "order": 9999
        },
        {
            "url": "https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-02.jpg",
            "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/JH8QRQ2-4964549034598-02.jpg",
            "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/JH8QRQ2-4964549034598-02.jpg",
            "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/JH8QRQ2-4964549034598-02.jpg",
            "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/JH8QRQ2-4964549034598-02.jpg",
            "type": "image/jpeg",
            "order": 9999
        }
    ],
    "language": "en",
    "gtin": "4964549034598",
    "categories": [
        {
            "product_category_id": "72",
            "name": "Home and Kitchen",
            "url": null,
            "media": null,
            "path": null,
            "visible": false,
            "sub_categories": null,
            "depth": 0
        }
    ],
    "active": true,
    "unit": null,
    "description": "Besides using it as rice bowl, you can also use it for ice cream, snacks or whatever strikes your fancy\nMade of high quality ceramic and hand painted with traditional Japanese Plant which represents beauty, life and tranquility. The bowls are dishwasher and microwave safe\nThis traditionally crafted ceramic set will fit right in with any home decor with zen elements\nComes with easy packed gift box, a wonderful gift idea. These bowls makes a perfect gift item for house warming, birthdays, wedding, graduation, business gift or almost any occasion.",
    "created_at": "2020-05-10T01:59:18.2552261Z",
    "updated_at": "2020-05-27T20:01:20.2863528Z",
    "tags": [
        "Ceramic",
        "Hand Crafted",
        "Made in Japan",
        "Moritoku",
        "Rice Bowl",
        "Rice Bowl Set"
    ],
    "specifications": [
        {
            "section_name": "General",
            "properties": [
                {
                    "name": "Dishwasher",
                    "value": " Safe"
                },
                {
                    "name": " Product size",
                    "value": " approximate 4.5 inches diameter and 2.5 inches tall"
                }
            ]
        }
    ],
    "created_by": "mjiang2000@gmail.com",
    "updated_by": "mjiang2000@gmail.com",
    "price": {
        "currency": "CAD",
        "list": 33,
        "msrp": 33,
        "cost": null
    },
    "weight": 1.32,
    "id": "beeshop-JH8QRQ2",
    "document_type": "product_by_merchant",
    "_etag": "\"2100d6b5-0000-0200-0000-5ecec7100000\"",
    "_rid": "yVctAP1cTtWFAgAAAAAAAA==",
    "_self": "dbs/yVctAA==/colls/yVctAP1cTtU=/docs/yVctAP1cTtWFAgAAAAAAAA==/",
    "_attachments": "attachments/",
    "_ts": 1590609680
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

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
  "bcin":"JH8QRQ2"
	"title": "Jack - Oil Dispenser, White 123",
	"description": "Description: Oil Dispenser, White",
	"brand": "Cuisipro",
	"gtin": "0313",
  "weight": 200
 	"sku": "sku999",
  "active": true,
  "unit": "pound",
   "price": {
        "currency": "CAD",
        "list": 33,
        "msrp": 33,
        "cost": null
    },
   "tax_code": "regular"
}
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/merchant/:merchantId/product/:bcin/image" %}
{% api-method-summary %}
Upload a new image
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="bcin" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="file" type="object" required=true %}
supported image format : jpg, png and gif
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
    {
            "url": "https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-01.jpg",
            "thumbnail_url": "https://bc01dmedia.blob.core.windows.net/product-image-t/JH8QRQ2-4964549034598-01.jpg",
            "small_url": "https://bc01dmedia.blob.core.windows.net/product-image-s/JH8QRQ2-4964549034598-01.jpg",
            "medium_url": "https://bc01dmedia.blob.core.windows.net/product-image-m/JH8QRQ2-4964549034598-01.jpg",
            "large_url": "https://bc01dmedia.blob.core.windows.net/product-image-l/JH8QRQ2-4964549034598-01.jpg",
            "type": "image/jpeg",
            "order": 9999
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

{% api-method method="delete" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/merchant/:merchantId/product/:bcin/image" %}
{% api-method-summary %}
Delete an image
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="bcin" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="url" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-01.jpg
https://bc01dmedia.blob.core.windows.net/product-image-t/JH8QRQ2-4964549034598-01.jpg
https://bc01dmedia.blob.core.windows.net/product-image-s/JH8QRQ2-4964549034598-01.jpg
https://bc01dmedia.blob.core.windows.net/product-image-m/JH8QRQ2-4964549034598-01.jpg
https://bc01dmedia.blob.core.windows.net/product-image-l/JH8QRQ2-4964549034598-01.jpg

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

```text
url=https://bc01dmedia.blob.core.windows.net/product-image/JH8QRQ2-4964549034598-01.jpg
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/search" %}
{% api-method-summary %}
Search product
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "total": 213,
    "hits": [
        *product1
        *product2
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

Request Body

* List products without searching, only specify the filter, keep the keyword empty

```text
{
    "keyword":"",
    "size":10,
    "from":40,
    "filters": [
        {
            "field":"merchant_id",
            "value":"beeshop"
        }
    ]
}
```

* Search keyword with multiple filters

```text
{
    "keyword":"water bottle",
    "size":10,
    "from":0,
    "filters": [
        {
            "field":"merchant_id",
            "value":"beeshop"
        },
         {
            "field":"active",
            "value":"true"
        },
         {
            "field":"tags",
            "value":"upinkoo"
        }
    ]
}
```

{% api-method method="delete" host="https://bc01d-coreapi-apim.azure-api.net/product/v1" path="/merchant/:merchantId/product/:bcin" %}
{% api-method-summary %}
Delete a product
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="bcin" type="string" required=true %}

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
*Product
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

