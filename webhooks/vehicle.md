# Vehicle

Here is an example of request that Activix CRM can make to push data to an external web service. Refer to the [Vehicle object](https://docs.crm.activix.ca/objects/vehicle) documentation to see all the attributes that may be included in the request.

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
{% api-method-parameter name="X-Signature-Activix" type="string" required=true %}
 Signature encoded in SHA-256 and compound with the body and the secure key.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
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
    "lead_id": 1649444,
    "type": "exchange",
    "make": "Toyota",
    "model": "Yaris",
    "trim": null,
    "year": "2015",
    "stock": null,
    "vin": "Vnkktud34fa038207",
    "transmission": null,
    "color_exterior": null,
    "color_interior": null,
    "engine": null,
    "mileage": null,
    "price": null,
    "condition": null,
    "option": null,
    "url": null,
    "comment": null,
    "created_at": "2017-07-14 20:39:35",
    "updated_at": "2017-07-14 20:39:35",
    "order_number": null,
    "deleted_at": null,
    "created_by": null,
    "updated_by": null,
    "deleted_by": null,
    "funding": null,
    "client_number": null,
    "modality": "leasing",
    "term": null,
    "frequency": null,
    "end_contract_date": "2020-05-22 12:00:00",
    "preparation": null,
    "documentation": null,
    "accessories": null,
    "tire": false,
    "offer": null,
    "suffix": null,
    "recorded_date": null,
    "payment": null,
    "rate": null,
    "profit": null,
    "balance": null,
    "residual": null,
    "allowed_mileage": null,
    "intention": null,
    "value": null,
    "requested": null,
    "sold": false,
    "bank_id": null,
    "sold_by": null,
    "warranty": null,
    "stock_state": null,
    "security_deposit": null,
    "category": null,
    "category_rv": null,
    "fuel": null,
    "weight": null,
    "sleeping": null,
    "link": null,
    "budget_max": null,
    "budget_min": null,
    "year_max": null,
    "year_min": null,
    "initial_cash": null,
    "length_min": null,
    "length_max": null,
    "mechanical": null,
    "verified_by_id": null,
    "service": false,
    "sold_date": "",
    "actual_value": null,
    "trade_type": null,
    "trade_notes": null,
    "extended_warranty": null,
    "license_plate": null,
    "purchase_date": null,
    "end_warranty_date": null,
    "recall": null,
    "exported_to_serti": null,
    "timezone_changed": true,
    "vauto_value": null
}
```

