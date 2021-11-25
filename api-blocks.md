# API Blocks

{% swagger baseUrl="https://computer-api.example.com" path="/v1/computer" method="get" summary="Get a list of Computers" %}
{% swagger-description %}
Returns a list of computers
{% endswagger-description %}

{% swagger-parameter in="header" name="Accept" type="string" %}
the requested mime-type of the response
{% endswagger-parameter %}

{% swagger-parameter in="query" name="ids" type="array" %}
a list of the ids of the models to get
{% endswagger-parameter %}

{% swagger-parameter in="query" name="ghz-greater-than" type="number" %}
filter out computers with less than the specified processor speed in GHz
{% endswagger-parameter %}

{% swagger-parameter in="query" name="count" type="integer" %}
the number of computers to show per page
{% endswagger-parameter %}

{% swagger-parameter in="query" name="make" type="string" %}
filter computers to a specific make
{% endswagger-parameter %}

{% swagger-parameter in="query" name="hide-abacuses" type="boolean" %}
whether or not to hide abacuses
{% endswagger-parameter %}

{% swagger-response status="200" description="A list of computers was found" %}
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
{% endswagger-response %}

{% swagger-response status="404" description="Something was wrong with the request" %}
```
{
  "error": "no computers here!"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://computer-api.example.com" path="/v1/computer" method="post" summary="Create a new computer" %}
{% swagger-description %}
Create a new computer to be stored
{% endswagger-description %}

{% swagger-parameter in="body" name="metadata" type="object" %}
an object containing arbitrary metadata about the computer
{% endswagger-parameter %}

{% swagger-parameter in="body" name="model" type="string" %}
the model of the computer
{% endswagger-parameter %}

{% swagger-parameter in="body" name="make" type="string" %}
the make of the computer
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "make": "my new computer maker",
  "model": "the very best computer"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://computer-api.example.com" path="/v1/computer/{computer}" method="get" summary="Get a specific computer" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="computer" type="string" %}
the ID of the computer you want to get
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
  "id": "c982aa55-ffef-49ef-8c05-50f8f3b0b417",
  "make": "Raspberry Pi",
  "model": "zero"
}
```
{% endswagger-response %}
{% endswagger %}
