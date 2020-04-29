# Vehicle

The following describes the available resources for a Vehicle. Check out the [Vehicle object](../objects/vehicle.md) documentation for a complete list of attributes.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/lead-vehicles" %}
{% api-method-summary %}
Create a vehicle
{% endapi-method-summary %}

{% api-method-description %}
Creates a vehicle. Returns the created vehicle.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
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
{% api-method-parameter name="lead\_id" type="number" required=true %}
The id of the lead associated with the vehicle.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
The type of vehicle. Possible values are **existing** or **exchange**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Vehicle created successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 3387562,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "lead_id": 3466512,
        "type": "wanted",
        "vin": "VIN333",
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
    "lead_id": 3454440,
    "type": "wanted",
    "vin": "VIN333",
    ...
}
```

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/lead-vehicles/:id" %}
{% api-method-summary %}
Update a vehicle
{% endapi-method-summary %}

{% api-method-description %}
Updates the specified vehicle by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated vehicle.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
The ID of the vehicle to update.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
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
{% api-method-parameter name="lead\_id" type="number" required=true %}
The ID of the lead associated with the vehicle.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
The type of vehicle. Possible values are **existing** or **exchange**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Vehicle updated successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 3387562,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "lead_id": 3466512,
        "type": "wanted",
        "vin": "VIN444",
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
    "vin": "VIN444",
    ...
}
```

