# Verify Email



{% swagger method="get" path="verify/{email}" baseUrl="" summary="Verify registered user account via email." expanded="true" %}
{% swagger-description %}
This operation verified the user's email and generates a signed URL.
{% endswagger-description %}

{% swagger-parameter in="path" name="email" %}
Valid email of registered user.
{% endswagger-parameter %}
{% endswagger %}
