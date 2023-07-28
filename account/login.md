# Login

{% swagger method="post" path="/auth/login" baseUrl="" summary="Login using a valid phone number and password." expanded="true" %}
{% swagger-description %}
This endpoint allows the user to pass in their valid credentials in exchange for an access token as well as other relevant user data.
{% endswagger-description %}

{% swagger-parameter in="body" name="phone" required="true" %}
a valid registered phone number without country code.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}
password used during registration.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "message": "Logged in successfully!",
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.xxJpc3MiOiJodHRwczpcL1wvYXBpLm15dGlja2V0Z2guY29tXC92MVwvXXXXaFwvbG9naW4iLCJpXXQiOjE2NzXXXXXxNjUsImV4cCI6MTY4OTc2MzXXNSwibmXmIjoxNjczOTk1MTY1LCJqdGkiOiJpNXdxbnM1cjlEOEdTUGh6Iiwic3ViIjoXXXwicHJ2IjoiMTZlNGNkYTM1OGRiNGXXXjQxZTI4NzcxNjBmYjE4MmU1MGNhNmRmZSJ9.HM8bNNv4o31JeeZ7RrsbTmaYzOqiQWWuBQpAvq_4Qus",
    "user": {
        "fullname": "Michael Asante",
        "phone": "026XXXXXXX",
        "email": "xxx@gmail.com",
        "dateOfBirth": null,
        "nextOfKin": {
            "fullname": null,
            "phone": null
        },
        "hasProfile": false,
        "referralCode": "XXXX"
    }
}
```
{% endcode %}
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Failed" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "message": "Invalid phone number or password."
}
```
{% endcode %}
{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="Validation Error" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "message": "The given data was invalid.",
    "errors": {
        "password": [
            "The password field is required."
        ]
    }
}
```
{% endcode %}
{% endswagger-response %}
{% endswagger %}
