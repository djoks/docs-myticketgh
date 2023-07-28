---
description: Get names of locations
---

# Route Origins

{% swagger method="get" path="/bus/routes" baseUrl="" summary="This API endpoint returns an array of location names taken from the "origin" field of related route objects." expanded="true" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="origin" required="true" %}
This param simply specifies which part of the route object needs to be returned and can be left empty as long as the key name is present.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="company" required="true" %}
Alias of selected bus company.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
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
{% endcode %}
{% endswagger-response %}
{% endswagger %}
