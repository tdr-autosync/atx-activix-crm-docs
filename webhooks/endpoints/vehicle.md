# Vehicle

Here is an example of a request Activix CRM can make to push data to an external web service. Refer to the [Vehicle object](https://docs.crm.activix.ca/objects/vehicle) documentation to see all the attributes that may be included in the request.

All the responses in the example **must** be handled \(you may handle more if you want\).

{% api-method method="post" host="https://your-url.com" path="/example" %}
{% api-method-summary %}
Vehicle created
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="X-Activix-Signature" type="string" required=true %}
 Signature encoded in SHA-256 and compound with the body and the secure key.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Lead successfully created.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Vehicle created successfully"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "Unknwon Account."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "Internal Server Error."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```javascript
{
    "id": 2258306,
    "created_at": "2018-04-09T18:05:00+00:00",
    "updated_at": "2018-04-09T18:07:00+00:00"
    "lead_id": 1649444,
    "type": "exchange",
    "make": "Toyota",
    "model": "Yaris",
    "trim": null,
    "year": "2015",
    "stock": null,
    "vin": "Vnkktud34fa038207",
    ...
}
```

