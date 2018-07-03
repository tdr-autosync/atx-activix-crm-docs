---
description: >-
  The following describes the available resources for a Phone. Check out the
  Phone object documentation for a complete list of attributes.
---

# Phone

{% api-method method="post" host="https://crm.activix.ca/api/v2" path="/lead-phones" %}
{% api-method-summary %}
Create a phone
{% endapi-method-summary %}

{% api-method-description %}
Create a phone. Returns the created phone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentification" type="string" required=true %}
OAuth 2 or Basic Auth authentification credentials.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-type" type="string" required=false %}
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
Phone created successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 34566,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:05:00+00:00",
        "lead_id": 3466512,
        "number": "+15141234455",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Body Example

```javascript
{
    "lead_id": 3387562,
    "number": "+15141234455",
    "type": "home",
    ...
}
```

{% api-method method="put" host="https://crm.activix.ca/api/v2" path="/lead-phones/:id" %}
{% api-method-summary %}
Update a phone
{% endapi-method-summary %}

{% api-method-description %}
Update a phone. Returns the updated phone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the phone to update.
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
Phone updated successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 34566,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "lead_id": 3466512,
        "number": "+15141234455",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Body Example

```javascript
{
    "number": "+15141234459",
    "type": "home",
    ...
}
```
