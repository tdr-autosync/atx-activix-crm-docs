---
description: >-
  The following describes the available resources for an Email. Check out the
  Email object documentation for a complete list of attributes.
---

# Email

{% api-method method="post" host="https://crm.activix.ca/api/v2" path="/lead-emails" %}
{% api-method-summary %}
Create an email
{% endapi-method-summary %}

{% api-method-description %}
Create an email. Returns the created email.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentification" type="string" required=true %}
OAuth 2 or Basic Auth authentification credentials.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
Should be application/json.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=false %}
Should be application/json.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Email created successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 34566,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:05:00+00:00",
        "lead_id": 3466512,
        "address": "test@activix.ca",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Body Example

```javascript
{
    "lead_id": 3387562,
    "address": "test@activix.ca",
    "type": "home",
    ...
}
```

{% api-method method="put" host="https://crm.activix.ca/api/v2" path="/lead-emails/:id" %}
{% api-method-summary %}
Update an email
{% endapi-method-summary %}

{% api-method-description %}
Update an email. Returns the updated email.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the email to update.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentification" type="string" required=true %}
OAuth 2 or Basic Auth authentification credentials.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
Should be application/json.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=false %}
Should be application/json.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Email updated successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 34566,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "lead_id": 3466512,
        "address": "test@activix.ca",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Body Example

```javascript
{
    "address": "test@activix.ca",
    "type": "work",
    ...
}
```
