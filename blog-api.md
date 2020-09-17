# Blog API

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/blog/v1" path="/merchant/:merchantId/bloglist " %}
{% api-method-summary %}
Get a blog list by micro merchant \(for editing\)
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
{% api-method-parameter name="Authoorization" type="string" required=true %}
bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="status" type="string" required=false %}
public, private \(use "\|" to concatenate multiple status\) 
{% endapi-method-parameter %}

{% api-method-parameter name="continuation\_token" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="page\_size" type="string" required=false %}
default 5
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "has_more": false,
    "continuation_token": null,
    "results": [
        {
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "third post",
            "image": null,
            "description": "test 3",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T20:37:07.6270371Z",
            "blog_id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "document_type": "blog"
         },
        {
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "third post",
            "image": null,
            "description": "test 3",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T20:35:58.8560682Z",
            "blog_id": "67fdbf95-3bd4-4893-888b-2dc479b79671",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "67fdbf95-3bd4-4893-888b-2dc479b79671",
            "document_type": "blog"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/blog/v1" path="/blog/search" %}
{% api-method-summary %}
Search blogs 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
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
    "total": 2,
    "hits": [
        {
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "third post",
            "image": null,
            "description": "test 3",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T20:35:58.8560682Z",
            "blog_id": "67fdbf95-3bd4-4893-888b-2dc479b79671",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "67fdbf95-3bd4-4893-888b-2dc479b79671",
            "document_type": "blog"
        },
        {
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "third post",
            "image": null,
            "description": "test 3",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T20:37:07.6270371Z",
            "blog_id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "document_type": "blog"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
{
    "keyword":"",
    "size":50,
    "from":0,
    "filters": [
        {
            "field":"status",
            "value":"public",
        }
    ]
}
```

{% api-method method="get" host="https://bc01d-coreapi-apim.azure-api.net/blog/v1" path="/merchant/:merchantId/blog/:blogId" %}
{% api-method-summary %}
Get a blog
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="blogId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=true %}

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
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "second post",
            "image": null,
            "description": "test 2",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T19:35:30.708595Z",
            "blog_id": "a82da77c-7eae-4946-89ff-681da736d1bd",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "a82da77c-7eae-4946-89ff-681da736d1bd",
            "document_type": "blog"
        }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/blog/v1" path="/merchant/:merchantId/blog" %}
{% api-method-summary %}
Create a blog
{% endapi-method-summary %}

{% api-method-description %}
blog is created as Private status, use put api to update the private status to public
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="merchantId" type="string" required=false %}

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
    {
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "third post",
            "image": null,
            "description": "test 3",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T20:37:07.6270371Z",
            "blog_id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "document_type": "blog"
         }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
     {
            "title": "third post",  //required
            "image": null,   
            "description": "test 3",  //required
            "description_markup": null,
            "jielong_id": null,
            "language": "en"
         }
```

{% api-method method="put" host="https://bc01d-coreapi-apim.azure-api.net/blog/v1" path="/merchant/:merchantId/blog/:blogId" %}
{% api-method-summary %}
Update a blog
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="blogId" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
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
            "merchant_id": "ZEMBC",
            "merchant_name": "mjiang2000@gmail.com",
            "title": "third post",
            "image": null,
            "description": "test 3",
            "description_markup": null,
            "author_id": "mjiang2000@gmail.com",
            "author_name": "Min Jiang",
            "updated_at": "2020-08-31T20:37:07.6270371Z",
            "blog_id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "jielong_id": null,
            "status": "private",
            "language": "en",
            "id": "4c087f05-270c-4a60-91e3-426bdbedbb95",
            "document_type": "blog"
         }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Request body

```text
     {
            "title": "third post",  //optional
            "image": null,           //optional      
            "description": "test 3",  //required
            "description_markup": null, //optional
            "jielong_id": null,       //optional
            "status:": "public"       //optional             
         }
```

{% api-method method="post" host="https://bc01d-coreapi-apim.azure-api.net/blog/v1" path="/merchant/:merchantId/blog/:blogId/image " %}
{% api-method-summary %}
Create a blog image
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="blogId" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="merchantId" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="image1" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{ "image": imageUrl }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

