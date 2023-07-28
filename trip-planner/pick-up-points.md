---
description: Available endpoints for pick-up points API
---

# Pick-Up Points

{% swagger method="get" path="/bus/pickup-points" baseUrl="" summary="Get route pick-up points" expanded="true" %}
{% swagger-description %}
This API endpoint returns an array of pickup-point objects based on the selected route origin and destination names.
{% endswagger-description %}

{% swagger-parameter in="body" name="origin" required="true" %}
Selected bus route origin name.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="destination" required="true" %}
Selected bus route destination name.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
[
    {
        "name": "Amasaman",
        "latitude": "5.5911921",
        "longitude": "-0.3198162"
    },
    {
        "name": "Linda D'or",
        "latitude": "5.5911921",
        "longitude": "-0.3198162"
    }
]
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
