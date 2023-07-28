---
description: Get a list of available bus schedules
---

# Schedules

{% swagger method="get" path="/bus/schedules" baseUrl="" summary="This API endpoint returns an array of available bus schedule objects grouped by bus type." expanded="true" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="company" required="true" %}
Selected bus company alias.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="origin" required="true" %}
Selected bus route origin.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="destination" required="true" %}
Selected bus route destination.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="date" required="true" %}
Selected departure date.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "executive": [
        {
            "id": 14832,
            "batch_no": 1,
            "route_id": 1,
            "destination": "Achimota",
            "weekday": "friday",
            "reportingTime": "09:00",
            "departureTime": "10:00",
            "period": "AM",
            "fare": "50.00",
            "busType": {
                "name": "Executive",
                "minCapacity": 26,
                "maxCapacity": 30,
                "arrangement": "2x1"
            },
            "ticketsSold": 0,
            "almostSoldOut": false,
            "soldOut": false
        },
        {
            "id": 460,
            "batch_no": 1,
            "route_id": 1,
            "destination": "Achimota",
            "weekday": "friday",
            "reportingTime": "11:00",
            "departureTime": "12:00",
            "period": "PM",
            "fare": "113.00",
            "busType": {
                "name": "Executive",
                "minCapacity": 26,
                "maxCapacity": 30,
                "arrangement": "2x1"
            },
            "ticketsSold": 0,
            "almostSoldOut": false,
            "soldOut": false
        },
        {
            "id": 459,
            "batch_no": 1,
            "route_id": 1,
            "destination": "Achimota",
            "weekday": "friday",
            "reportingTime": "03:00",
            "departureTime": "04:00",
            "period": "PM",
            "fare": "113.00",
            "busType": {
                "name": "Executive",
                "minCapacity": 26,
                "maxCapacity": 30,
                "arrangement": "2x1"
            },
            "ticketsSold": 0,
            "almostSoldOut": false,
            "soldOut": false
        },
        {
            "id": 14833,
            "batch_no": 1,
            "route_id": 1,
            "destination": "Achimota",
            "weekday": "friday",
            "reportingTime": "03:00",
            "departureTime": "04:00",
            "period": "PM",
            "fare": "50.00",
            "busType": {
                "name": "Executive",
                "minCapacity": 28,
                "maxCapacity": 31,
                "arrangement": "1x2"
            },
            "ticketsSold": 0,
            "almostSoldOut": false,
            "soldOut": false
        }
    ],
    "standard": [
        {
            "id": 407,
            "batch_no": 1,
            "route_id": 1,
            "destination": "Achimota",
            "weekday": "friday",
            "reportingTime": "03:00",
            "departureTime": "04:00",
            "period": "PM",
            "fare": "113.00",
            "busType": {
                "name": "Standard",
                "minCapacity": 48,
                "maxCapacity": 53,
                "arrangement": "2x2"
            },
            "ticketsSold": 0,
            "almostSoldOut": false,
            "soldOut": false
        },
        {
            "id": 441,
            "batch_no": 1,
            "route_id": 1,
            "destination": "Achimota",
            "weekday": "friday",
            "reportingTime": "07:00",
            "departureTime": "08:00",
            "period": "PM",
            "fare": "113.00",
            "busType": {
                "name": "Standard",
                "minCapacity": 40,
                "maxCapacity": 44,
                "arrangement": "2x2"
            },
            "ticketsSold": 0,
            "almostSoldOut": false,
            "soldOut": false
        }
    ]
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
