# Reset Password

{% swagger method="post" path="/auth/reset" baseUrl="" summary="Send a password reset request via mail." expanded="true" %}
{% swagger-description %}
This API endpoint generates and sends a signed URL for a password reset to the user's registered email address.
{% endswagger-description %}

{% swagger-parameter in="body" name="email" type="String" required="true" %}
xxxx@gmail.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="token" type="String" %}
A valid unique token provided by google recaptcha.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "message": "Please check your mail for a verification link to reset your password."
}
```
{% endcode %}
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Suspicious Activity" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "title": "Are you a robot?",
    "message": "Suspicious activity detected, please turn off your VPN if you have it activated.",
    "data": null
}
```
{% endcode %}
{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="Validation Error" %}
{% code overflow="wrap" lineNumbers="true" %}
```json

    "message": "The given data was invalid.",
    "errors": {
        "email": [
            "The email field is required."
        ]
    }
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
