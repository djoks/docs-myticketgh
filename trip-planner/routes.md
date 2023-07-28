---
description: Available endpoints for routes API
---

# Routes

{% swagger method="get" path="" baseUrl="/bus/routes" summary="Get route origins" expanded="true" %}
{% swagger-description %}
This API endpoint returns an array of location names taken from related route objects' "origin" field.
{% endswagger-description %}

{% swagger-parameter in="query" name="origin" required="true" %}
This param simply specifies which part of the route object needs to be returned and can be left empty as long as the key name is present.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="company" required="true" %}
Alias of selected bus company.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```
[
    "Accra",
    "Achimota",
    "Banda Nkwanta",
    "Cape coast",
    "Dadieso",
    "Dambai",
    "Dormaa",
    "Drobo",
    "Kete Krachi",
    "Kintampo",
    "Linda D'or",
    "Nandom",
    "Nkawkaw",
    "Sunyani",
    "Wa"
]
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/bus/routes" baseUrl="" summary="Get route destinations" expanded="true" %}
{% swagger-description %}
Get the list of routes by company and origin.

\




\


This API endpoint returns an array of route objects based on the selected route origin and company names.
{% endswagger-description %}

{% swagger-parameter in="body" name="origin" required="true" %}
Selected bus route origin name.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="company" required="true" %}
Selected bus company alias.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```javascript
[
    {
        "id": 1,
        "originId": 1,
        "origin": "Accra",
        "destination": "Achimota",
        "duration": "9 hrs 51 mins",
        "distance": 27
    },
    {
        "id": 2,
        "originId": 1,
        "origin": "Accra",
        "destination": "Banda Nkwanta",
        "duration": "10 hrs 53 mins",
        "distance": 14
    },
    {
        "id": 3,
        "originId": 1,
        "origin": "Accra",
        "destination": "Cape coast",
        "duration": "2 hrs 50 mins",
        "distance": 22
    },
    {
        "id": 4,
        "originId": 1,
        "origin": "Accra",
        "destination": "Dadieso",
        "duration": "6 hrs 09 mins",
        "distance": 21
    },
    {
        "id": 5,
        "originId": 1,
        "origin": "Accra",
        "destination": "Dambai",
        "duration": "2 hrs 21 mins",
        "distance": 8
    },
    {
        "id": 6,
        "originId": 1,
        "origin": "Accra",
        "destination": "Dormaa",
        "duration": "5 hrs 48 mins",
        "distance": 5
    },
    {
        "id": 7,
        "originId": 1,
        "origin": "Accra",
        "destination": "Drobo",
        "duration": "8 hrs 04 mins",
        "distance": 13
    },
    {
        "id": 8,
        "originId": 1,
        "origin": "Accra",
        "destination": "Kete Krachi",
        "duration": "6 hrs 10 mins",
        "distance": 7
    },
    {
        "id": 9,
        "originId": 1,
        "origin": "Accra",
        "destination": "Kintampo",
        "duration": "6 hrs 51 mins",
        "distance": 6
    },
    {
        "id": 10,
        "originId": 1,
        "origin": "Accra",
        "destination": "Linda D'or",
        "duration": "10 hrs 41 mins",
        "distance": 6
    },
    {
        "id": 11,
        "originId": 1,
        "origin": "Accra",
        "destination": "Nandom",
        "duration": "5 hrs 38 mins",
        "distance": 7
    },
    {
        "id": 12,
        "originId": 1,
        "origin": "Accra",
        "destination": "Nkawkaw",
        "duration": "6 hrs 10 mins",
        "distance": 28
    },
    {
        "id": 13,
        "originId": 1,
        "origin": "Accra",
        "destination": "Sunyani",
        "duration": "6 hrs 56 mins",
        "distance": 21
    },
    {
        "id": 14,
        "originId": 1,
        "origin": "Accra",
        "destination": "Wa",
        "duration": "9 hrs 06 mins",
        "distance": 18
    }
]
```
{% endswagger-response %}
{% endswagger %}
