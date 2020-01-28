# Phone

The following describes the available resources for a Phone. Check out the [Phone object](https://docs.crm.activix.ca/objects/phone) documentation for a complete list of attributes.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/lead-phones" %}
{% api-method-summary %}
Create a phone
{% endapi-method-summary %}

{% api-method-description %}
Creates a phone. Returns the created phone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-type" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="number" type="string" required=true %}
The phone number.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
The type of phone number. Possible values are **home**, **work** or **mobile**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
        "lead_id": 3387562,
        "number": "+15141234455",
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
    "number": "+15141234455",
    "type": "home",
    ...
}
```

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/lead-phones/:id" %}
{% api-method-summary %}
Update a phone
{% endapi-method-summary %}

{% api-method-description %}
Updates the specified phone by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated phone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the phone to update.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="number" type="string" required=true %}
The phone number.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
The type of phone number. Possible values are **home**, **work** or **mobile**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
        "number": "+15141234459",
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
    "number": "+15141234459",
    "type": "home",
    ...
}
```

