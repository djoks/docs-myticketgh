---
description: Get available bus schedule dates
---

# Available Dates

{% swagger method="get" path="/bus/schedules/dates" baseUrl="" summary="This API endpoint returns an object of available and excluded bus schedule dates arrays.  All dates within the available array field will be selectable on the front-end and all dates within the excluded field array will be disabled.  A user can only select dates up to 7 days in advance, current date excluded." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="origin" required="true" %}
Selected bus route origin name.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="destination" required="true" %}
Selected bus route destination name.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="company" required="true" %}
Select bus company alias.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "available": [
        "2023-01-24",
        "2023-01-25",
        "2023-01-26",
        "2023-01-28",
        "2023-01-29",
        "2023-01-30"
    ],
    "excluded": [
        "2023-01-27"
    ]
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
