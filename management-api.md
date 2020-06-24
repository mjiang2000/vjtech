# Management API

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/management/v1" path="/setting/type/:type/id/:id" %}
{% api-method-summary %}
Get Settings
{% endapi-method-summary %}

{% api-method-description %}
Get global settings such as ios\_version, etc
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
if document type has multiple files, provide id  
otherwise provide same value in type field  
for example ios\_version
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
setting document type:  
1. ios\_version  
2. android\_version \(tbd\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
the response will vary depends on the setting type required. see response samples below
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
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Response - ios\_version 

```text
{
    "id": "ios_version",
    "document_type": "ios_version",
    "minimum_supported_version": "1.3.5",
    "latest_version": "1.3.5",
    "what_is_new": "",
    "update_url": "itms-apps://itunes.apple.com/ca/app/id1491390902"
}
```





