---
description: User API
---

# User API

User related api

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/login" %}
{% api-method-summary %}
Login
{% endapi-method-summary %}

{% api-method-description %}
login as normal user
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
successfully login
{% endapi-method-response-example-description %}

```
{
    "merchant_list": [
        {
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "merchant_type": "wholesale",
            "roles": [
                "admin"
            ],
            "user_id": "mjiang2000@hotmail.com",
            "given_name": null,
            "family_name": null,
            "name": null,
            "email": "mjiang2000@hotmail.com",
            "id": "13ec185f-368d-4e6e-a55b-e0f56eb2f56b",
            "document_type": "user_by_merchant",
            "_etag": "\"f7007595-0000-0200-0000-5ec6ec580000\""
        }
    ],
    "merchant_flag": true,
    "micro_merchant_flag": false,
    "custom_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1aWQiOiJtamlhbmcyMDAwQGhvdG1haWwuY29tIiwiaXNzIjoiZmlyZWJhc2UtYWRtaW5zZGsteWViamVAYmVlc2hvcC1kZXYuaWFtLmdzZXJ2aWNlYWNjb3VudC5jb20iLCJzdWIiOiJmaXJlYmFzZS1hZG1pbnNkay15ZWJqZUBiZWVzaG9wLWRldi5pYW0uZ3NlcnZpY2VhY2NvdW50LmNvbSIsImF1ZCI6Imh0dHBzOi8vaWRlbnRpdHl0b29sa2l0Lmdvb2dsZWFwaXMuY29tL2dvb2dsZS5pZGVudGl0eS5pZGVudGl0eXRvb2xraXQudjEuSWRlbnRpdHlUb29sa2l0IiwiZXhwIjoxNTkwNDI0MDQzLCJpYXQiOjE1OTA0MjA0NDN9.iF_q07yvFLI4PtTbaZ63HPliYj6UrNalkT3R4P8Dy7uSDTExRfCFik8O8VXN44eeMe9FZhFWX2Q1uhijRplRPuwQ0aCbcr7YkJ1WkJPISK0PCtxzy6-VH6nmAGxpdrdBH-MmMot_XEEe1sL6kVQRF8PDG3-zovbteSq-J6mZHOQOuxC6y2VRirjd6d3k-LkQ3bvz0guS-nrmrqZOx4ANuOclN7rHVfIMlrD6hTejHJzmHo1yH_FU1qQw7WakmGUoEjDw5hXD8oTF2Qw13w4AUJO1cKMo1XXnMMZUOzCCAZS-IBGnYpjbyvHQbO08FWLNB_X4bSzUEJROcEBgntMbew",
    "address_book": null,
    "subjects": [
        {
            "sub": "3e0b9941-db5c-4a43-a10e-1a18cd9ae1a0",
            "id_provider": null
        }
    ],
    "status": "accepted",
    "status_updated_at": "2020-05-25T15:27:23.3734157Z",
    "gbm_flag": null,
    "user_id": "mjiang2000@hotmail.com",
    "given_name": "Jack",
    "family_name": "Jiang",
    "name": "JJhotmail",
    "email": "mjiang2000@hotmail.com",
    "id": "mjiang2000@hotmail.com",
    "document_type": "user",
    "_etag": "\"33014678-0000-0200-0000-5ecbe3dc0000\""
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Token is expired or not provided
{% endapi-method-response-example-description %}

```
{
    "statusCode": 401,
    "message": "Unauthorized. Access token is missing or invalid."
}
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

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/merchant/login" %}
{% api-method-summary %}
Login as Merchant
{% endapi-method-summary %}

{% api-method-description %}
login as merchant user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {token}
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
successful login
{% endapi-method-response-example-description %}

```
{
    "merchant_list": [
        {
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "roles": [
                "admin"
            ],
            "user_id": "mjiang2000@gmail.com",
            "given_name": "Min",
            "family_name": "Jiang",
            "name": null,
            "email": "mjiang2000@gmail.com",
            "id": "67d2bcf9-8e71-4099-af90-367a0bc458ac",
            "document_type": "user_by_merchant",
            "_etag": "\"2e027369-0000-0200-0000-5eb84d190000\""
        }
    ],
    "merchant_flag": true,
    "custom_token": null,
    "address_book": null,
    "subjects": [
        {
            "sub": "f102c1fb-120d-4099-bf3c-4b6f8a8e11b5",
            "id_provider": "google.com"
        }
    ],
    "status": "registered",
    "status_updated_at": "2020-05-06T22:19:57.510254Z",
    "gbm_flag": null,
    "user_id": "mjiang2000@gmail.com",
    "given_name": "Min",
    "family_name": "Jiang",
    "name": null,
    "email": "mjiang2000@gmail.com",
    "id": "mjiang2000@gmail.com",
    "document_type": "user",
    "_etag": "\"a901ee0a-0000-0200-0000-5eb3380d0000\""
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": 401,
    "message": "Unauthorized. Access token is missing or invalid."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
if user is not a user of merchant 
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/relay" %}
{% api-method-summary %}
Relay
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": 401,
    "message": "Unauthorized. Access token is missing or invalid."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "user_flow":"",
    "grant_type":"",
    "client_id":"",
    "code":"",
    "code"_verifier":"",
    "refresh_token":"",
    "scope":"",
    "response_type":"",
    "username":"",
    "password":""
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/firebase/jwt" %}
{% api-method-summary %}
Get firebase jwt
{% endapi-method-summary %}

{% api-method-description %}

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

{% endapi-method-response-example-description %}

```
{
    "custom_token":"jwt token string"
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

