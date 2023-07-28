# Register

{% swagger method="post" path="/auth/register" baseUrl="" summary="Create a new unique account." expanded="true" %}
{% swagger-description %}
This endpoint allows the user to pass their personal info in order to create a brand new unverified account.
{% endswagger-description %}

{% swagger-parameter in="body" name="fullname" required="true" %}
Full name of customer.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="phone" required="true" %}
Valid phone number of user without country code.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="email" required="true" %}
Valid email of user.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}
A strong password with a minimum of 6 (six) characters.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="token" required="true" %}
A valid unique token provided by google recaptcha.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "message": "Registration was successful!"
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
<pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json"><a data-footnote-ref href="#user-content-fn-1">{</a>
    "message": "The given data was invalid.",
    "errors": {
        "fullname": [
            "The fullname field is required."
        ],
        "phone": [
            "The phone field is required."
        ],
        "email": [
            "The email field is required."
        ],
        "password": [
            "The password field is required."
        ]
    }
}
</code></pre>
{% endswagger-response %}
{% endswagger %}

[^1]: 
