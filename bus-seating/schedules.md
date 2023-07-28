---
description: Available endpoints for schedules API
---

# Schedules

{% swagger method="get" path="/bus/schedules" baseUrl="" summary="Get all schedules" expanded="true" %}
{% swagger-description %}
This API endpoint returns an array of available bus schedule objects grouped by bus type.
{% endswagger-description %}

{% swagger-parameter in="body" name="company" required="true" %}
Selected bus company alias.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="origin" required="true" %}
Selected bus route origin name.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="destination" required="true" %}
Selected bus route destination name.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="date" required="true" %}
Selected departure date.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
<pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json"><strong>{
</strong>    "executive": [
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
</code></pre>
{% endswagger-response %}
{% endswagger %}



{% swagger method="get" path="/bus/schedules/:id" baseUrl="" summary="Get schedule by ID" expanded="true" %}
{% swagger-description %}
This API endpoint returns a single bus schedule object.
{% endswagger-description %}

{% swagger-parameter in="path" required="true" %}
1
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```json
{
	"id": 1,
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
}
```
{% endswagger-response %}
{% endswagger %}
