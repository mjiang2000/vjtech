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

```text
{
    "merchant_list": [
        {
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "merchant_type": "wholesale",
            "roles": [
                "admin"
            ]
        },
        {
            "merchant_id": "secondMerchant",
            "merchant_name": "Second Merchant",
            "merchant_type": "wholesale",
            "roles": [
                "admin"
            ]
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

```text
{
    "statusCode": 401,
    "message": "Unauthorized. Access token is missing or invalid."
}
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

```text
{
   "merchant_list": [
        {
            "merchant_id": "beeshop",
            "merchant_name": "Beeshop",
            "merchant_type": "wholesale",
            "roles": [
                "admin"
            ]
        },
        {
            "merchant_id": "secondMerchant",
            "merchant_name": "Second Merchant",
            "merchant_type": "wholesale",
            "roles": [
                "admin"
            ]
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

```text
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

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/relay" %}
{% api-method-summary %}
aad b2c relay
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

```text
{
    "custom_token":"jwt token string"
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
get user firebase token
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

```text
{
    "custom_token":"jwt token string"
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

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/user/addressbook" %}
{% api-method-summary %}
Update address book
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
*user
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
"address_book": [
        {
            "id": "a",
            "full_name": "Jack Jiang",
            "street_1": "4 Danbury court",
            "street_2": null,
            "city": "Markham",
            "country": "Canada",
            "province": "ON",
            "postal_code": "L3R7S1",
            "phone": "416-2728539",
            "email": "mjiang2000@hotmail.com",
            "is_default": false
        },
        {
            "id": "b",
            "full_name": "Jack Jiang",
            "street_1": "5 Danbury court",
            "street_2": null,
            "city": "Markham",
            "country": "Canada",
            "province": "ON",
            "postal_code": "L3R7S1",
            "phone": "416-2728539",
            "email": "mjiang2000@hotmail.com",
            "is_default": false
        },
        {
            "id": "c",
            "full_name": "Jack Jiang",
            "street_1": "6 Danbury court",
            "street_2": null,
            "city": "Markham",
            "country": "Canada",
            "province": "ON",
            "postal_code": "L3R7S1",
            "phone": "416-2728539",
            "email": "mjiang2000@hotmail.com",
            "is_default": false
        },
        {
            "id": "d",
            "full_name": "Jack Jiang",
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
        {
            "id": "e",
            "full_name": "Jack Jiang",
            "street_1": "8 Danbury court",
            "street_2": null,
            "city": "Markham",
            "country": "Canada",
            "province": "ON",
            "postal_code": "L3R7S1",
            "phone": "416-2728539",
            "email": "mjiang2000@hotmail.com",
            "is_default": false
        }
    ]
    }
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/user/avatar" %}
{% api-method-summary %}
Update user avatar
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

{% api-method-form-data-parameters %}
{% api-method-parameter name="file1" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
 "avatar": "url",
*user
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
{
   "group_id": auto_id,
   "group_owner_id": user_id,
   "is_group_chat": true //true: group chat, false conversation in 2 members
   other fields ...
}
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/user" %}
{% api-method-summary %}
Update user name
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=false %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
 *user
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "given_name": "Min3", //optional
    "family_name": "Jiang3", //optional
    "name":"Jack Jiang Gmail3" //optional
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/wechatjwt" %}
{% api-method-summary %}
Get Wechat JWT
{% endapi-method-summary %}

{% api-method-description %}
The custom JWT token expired in 24 hours
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="openid" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="access\_token" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "custom_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6Im1qaWFuZzIwMDBAaG90bWFpbC5jb20iLCJnaXZlbl9uYW1lIjoiamFjayB3ZWNoYXQiLCJmYW1pbHlfbmFtZSI6ImppYW5nIiwic3ViIjoibWppYW5nMjAwMEBob3RtYWlsLmNvbSIsIm5iZiI6MTYwNzAxNjc4OCwiZXhwIjoxNjA3MTAzMTg0LCJpYXQiOjE2MDcwMTY3ODgsImlzcyI6Imh0dHA6Ly9iZWVzaG9wLmNoYXQiLCJhdWQiOiJodHRwOi8vbW9iaWxlLmJlc2hvcC5jb20ifQ.wQVE98zTTxVnE5dr3jPW8mcejtX3FStqhTth1467_WE"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "nickname": "J.J",
    "openid": "oNXh9uBuHSX5dO6BJ04OnEQW2eXI",
    "unionid": "o5XWQv9iPJmj6PPz8Q13iNoTPOJQ",
    "headimgurl": "https://thirdwx.qlogo.cn/mmopen/vi_32/sDYYvwoOpqFCe6wDm3MVGL7IiaMTEChwguH6c4RheQn8zEfytnuOibRWeCVFx6tNm7nTWllJweCjQYRa7qH7ku8A/132",
    "email": "",
    "given_name": "",
    "family_name": ""
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=412 %}
{% api-method-response-example-description %}
return when email is not validated yet
{% endapi-method-response-example-description %}

```
{
    "nickname": "J.J",
    "openid": "oNXh9uBuHSX5dO6BJ04OnEQW2eXI",
    "unionid": "o5XWQv9iPJmj6PPz8Q13iNoTPOJQ",
    "headimgurl": "https://thirdwx.qlogo.cn/mmopen/vi_32/sDYYvwoOpqFCe6wDm3MVGL7IiaMTEChwguH6c4RheQn8zEfytnuOibRWeCVFx6tNm7nTWllJweCjQYRa7qH7ku8A/132",
    "email": "mjiang2000@hotmail.com",
    "given_name": "jack wechat",
    "family_name": "jiang"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/wechatusersignup" %}
{% api-method-summary %}
Wechat User Signup
{% endapi-method-summary %}

{% api-method-description %}
if response is 200, an email should be send to the given email address for verification.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="access\_token" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="openid" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "status": "ok"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Email is required.
Email is invalid.
User is registered.

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "email" : "mjiang2000@hotmail.com",
    "given_name": "jack wechat",
    "family_name": "jiang"
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/user/v1" path="/wechatuseremailverify" %}
{% api-method-summary %}
Verify Wechat User email 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="code" type="string" required=true %}
verification code
{% endapi-method-parameter %}

{% api-method-parameter name="union\_id" type="string" required=true %}
union id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Your email is verified. You are all set to login beeshop with Wechat.
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Sorry we cannot verify your email. Either the link is expired or wrong verification code.
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

