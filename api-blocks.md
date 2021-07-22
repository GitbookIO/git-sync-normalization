# API Blocks

{% api-method method="get" host="https://computer-api.example.com" path="/v1/computer" %}
{% api-method-summary %}
Get a list of Computers
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of computers
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Accept" type="string" required=false %}
the requested mime-type of the response
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="ids" type="array" required=false %}
a list of the ids of the models to get
{% endapi-method-parameter %}

{% api-method-parameter name="ghz-greater-than" type="number" required=false %}
filter out computers with less than the specified processor speed in GHz
{% endapi-method-parameter %}

{% api-method-parameter name="count" type="integer" required=false %}
the number of computers to show per page
{% endapi-method-parameter %}

{% api-method-parameter name="make" type="string" required=false %}
filter computers to a specific make
{% endapi-method-parameter %}

{% api-method-parameter name="hide-abacuses" type="boolean" required=true %}
whether or not to hide abacuses
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
A list of computers was found
{% endapi-method-response-example-description %}

```
{
  "items": [{
    "id": "c982aa55-ffef-49ef-8c05-50f8f3b0b415",
    "make": "Apple",
    "model": "Apple 1"
  }, {
    "id": "c982aa55-ffef-49ef-8c05-50f8f3b0b416",
    "make": "Commodore",
    "model": "64"
  }, {
    "id": "c982aa55-ffef-49ef-8c05-50f8f3b0b417",
    "make": "Raspberry Pi",
    "model": "zero"
  }],
  "total": 9345
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Something was wrong with the request
{% endapi-method-response-example-description %}

```
{
  "error": "no computers here!"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://computer-api.example.com" path="/v1/computer" %}
{% api-method-summary %}
Create a new computer
{% endapi-method-summary %}

{% api-method-description %}
Create a new computer to be stored
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="metadata" type="object" required=false %}
an object containing arbitrary metadata about the computer
{% endapi-method-parameter %}

{% api-method-parameter name="model" type="string" required=true %}
the model of the computer
{% endapi-method-parameter %}

{% api-method-parameter name="make" type="string" required=true %}
the make of the computer
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "make": "my new computer maker",
  "model": "the very best computer"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://computer-api.example.com" path="/v1/computer/{computer}" %}
{% api-method-summary %}
Get a specific computer
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="computer" type="string" required=true %}
the ID of the computer you want to get
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "id": "c982aa55-ffef-49ef-8c05-50f8f3b0b417",
  "make": "Raspberry Pi",
  "model": "zero"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

