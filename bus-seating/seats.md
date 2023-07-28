---
description: Available endpoints for seats API
---

# Seats

{% swagger method="get" path="/bus/seats" baseUrl="" summary="Get list of active bus seats" expanded="true" %}
{% swagger-description %}
This API endpoint returns an array of active bus seat objects.
{% endswagger-description %}

{% swagger-parameter in="body" name="schedule_id" type="integer" required="true" %}
Selected bus schedule object id.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="date" required="true" %}
Selected departure date.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
[
    {
        "schedule_id": 460,
        "terminal_id": 1,
        "bus_id": null,
        "date": "2021-07-02",
        "number": 2,
        "status": "selected"
    },
    {
        "schedule_id": 460,
        "terminal_id": 1,
        "bus_id": null,
        "date": "2021-07-02",
        "number": 5,
        "status": "selected"
    },
    {
        "schedule_id": 460,
        "terminal_id": 1,
        "bus_id": null,
        "date": "2021-07-02",
        "number": 10,
        "status": "selected"
    },
    {
        "number": 1,
        "status": "reserved"
    }
]
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
