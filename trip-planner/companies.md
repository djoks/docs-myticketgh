---
description: Get list of available bus companies
---

# Companies

{% swagger method="get" path="/bus/companies" baseUrl="" summary="This API endpoint returns an array of objects, each object representing a verified and activated bus company in the system." expanded="true" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
[
    {
        "name": "OA Travel & Tours",
        "alias": "OA",
        "icon": "https://myticketafrica.s3.us-west-2.amazonaws.com/13/oa-icon-256x256.png"
    },
    {
        "name": "VIP Jeoun Transport",
        "alias": "VIP",
        "icon": "https://myticketafrica.s3.us-west-2.amazonaws.com/14/vip-icon-256x256.png"
    }
]
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
