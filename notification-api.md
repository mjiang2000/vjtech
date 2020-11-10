---
description: >-
  The notification api are hosted on firebase functions. the base url is in
  different pattern
---

# Firebase API

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



{% api-method method="post" host="https://us-central1-beeshop-dev.cloudfunctions.net/api" path="/notification/inapp" %}
{% api-method-summary %}
Send in-app notification to user/group
{% endapi-method-summary %}

{% api-method-description %}
This api will return  immediately without waiting for all notification messages are persisted in their document collection.
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
{ "status": "ok"}
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
    "audience_type":"group", //supported type: group or user
    "audience_id":"Ee1TuUKQKY9jT42kM43m", //id of the group or user
    "audience_option": "excludeMe", //optional
    "content_schema": "chat", //indicate the notification content schema
    "content":  //any json object, can be complex object with hierarchy
    {
        "boo":"foo",
        "my_payload":{
            "boo": "foo"
        }  
    }
}
```

To subscribe to the notification, set listener to firebase collection "groups" under "notifications" collection

```text
db.collection("notifications").doc("current_user_id").collection("groups")
.where(
    //filter by timestamp
)
```

Message schema

```text
{
    "timestamp":"2020-07-15T17:16:11Z",
    "content_schema":"chat",
    "content":{}
}
```

{% api-method method="post" host="https://us-central1-beeshop-dev.cloudfunctions.net/api" path="/notification/device" %}
{% api-method-summary %}
Send notification to device
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bear token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{ "status": "ok"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "audience_type":"group", //supported type: group or user
    "audience_id":"Ee1TuUKQKY9jT42kM43m", //id of the group or user
    "audience_option": "excludeMe", //optional
    "message": {
       "en": "English Message",
        "zh-Hans": "简体消息",
        "zh-Hant": "簡體消息"
    }
    "data":  
    {
        "boo":"foo"
    }
}
```

{% api-method method="post" host="https://us-central1-beeshop-dev.cloudfunctions.net/api" path="/invitetogroup" %}
{% api-method-summary %}
Invite user to group
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
firebase id token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "status": true //successfully added, false= already member of the group
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request Body

```text
{
    "group_id":"u7zCtDv5dD5dzSQoywcq",
    "user_id":"mjiang2000@gmail.com"
}
```

{% api-method method="post" host="https://us-central1-beeshop-dev.cloudfunctions.net/api" path="/notification/unregisterinappnotification" %}
{% api-method-summary %}
Unregister in app group notification
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
firebase id token
{% endapi-method-parameter %}
{% endapi-method-headers %}
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request Body

```text
{
    "group_id":"u7zCtDv5dD5dzSQoywcq",
    "user_id":"mjiang2000@gmail.com"
}
```



