---
description: >-
  The notification api are hosted on firebase functions. the base url is in
  different pattern
---

# Notification API

| Env | base Url |
| :--- | :--- |
| prod | [https://us-central1-beeshop-chat.cloudfunctions.net/api](https://us-central1-beeshop-dev.cloudfunctions.net/api) |
| dev | [https://us-central1-beeshop-dev.cloudfunctions.net/api](https://us-central1-beeshop-dev.cloudfunctions.net/api) |

#### How to retrieve firebase Id token

1. Call login api by using aad b2c id token
2. Retrieve custom token from response

```text
   "custom_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1aWQiOiJtamlhbmcyMDAwQGdtYWlsLmNvbSIsImlzcyI6ImZpcmViYXNlLWFkbWluc2RrLXllYmplQGJlZXNob3AtZGV2LmlhbS5nc2VydmljZWFjY291bnQuY29tIiwic3ViIjoiZmlyZWJhc2UtYWRtaW5zZGsteWViamVAYmVlc2hvcC1kZXYuaWFtLmdzZXJ2aWNlYWNjb3VudC5jb20iLCJhdWQiOiJodHRwczovL2lkZW50aXR5dG9vbGtpdC5nb29nbGVhcGlzLmNvbS9nb29nbGUuaWRlbnRpdHkuaWRlbnRpdHl0b29sa2l0LnYxLklkZW50aXR5VG9vbGtpdCIsImV4cCI6MTU5NDc4NjEzNSwiaWF0IjoxNTk0NzgyNTM1fQ.h3SXGE6VBSUAjMPGY-vkPN74bN_vTTpEsRRzC0qE0OSJbulXvxnHgZfGv-T8XVSmBEvO4mop0JfZc9Sy8AhHIU-W4auLNJwEvIHbBHb33zr1cWfncjc4sMdLLf-miLWGk5Lf-LmtmS1IvAVXFIOzz0ghLEgYU8q7bmuZ33uMJKE6EPQTq3wDDCXKcVxzFVrAN0zQ4mDiwKpzKtT7o4KolcVjzt8qP58Ff6HbbanYZN2N6PJQCANwiW5f7MtzWn0Bxbxn0fgxoalisITmdyTUbNhXRm9_e4AqFv2kjBN0t8vYkQ8MHQZP_vEQ8hgBk-0xHQCliqq5sLUaLdhNWB0K2g"
```

 3.login to firebase by use

```text
firebase.auth().signInWithCustomToken(customToken)
```

4. Call getIdToken\(\) from current user instance 

```text
  firebase.auth().onAuthStateChanged(function(user) {
    user.getIdToken()
   }
```



{% api-method method="post" host="https://us-central1-beeshop-dev.cloudfunctions.net/api" path="/notification" %}
{% api-method-summary %}
Send notification to user/group
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer firebase\_id\_token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{ "done": "done"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
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
    "filter_field":"group", //supported filed group or user
    "filter_value":"Ee1TuUKQKY9jT42kM43m", //id of the group or user
    "filter_option": "excludeMe", //optional
    "content":  //any json object, can be complex object with hierarchy
    {
        "boo":"foo",
        "my_payload":{
            "boo": "foo"
        }  
    }
}
```



