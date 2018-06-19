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

{% endapi-method-response-example-description %}

```javascript
{
    "id": 34566,
    "created_at": "2018-04-09T18:05:00+00:00",
    "extension": 555,
    "lead": {
        "id": 3387562,
        ...
    },
    "mobile": false,
    "number": "+15141234455",
    "updated_at": "2018-04-09T18:05:00+00:00",
    "valid": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "Unauthenticated."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Duplicate phone."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=405 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
"message": "Method not allowed."
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "The given data was invalid.",
    "errors": {
        "lead_id": [
            "The field lead_id is required."
        ]
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
    "extension": 555,
    "mobile": false,
    "number": "+15141234455"
}
```

{% api-method method="put" host="https://crm.activix.ca/api/v2" path="/lead-phones/:id" %}
{% api-method-summary %}
Update a phone
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID oh the phone to update
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

{% endapi-method-response-example-description %}

```javascript
{
    "id": 34566,
    "created_at": "2018-04-09T18:05:00+00:00",
    "extension": null,
    "lead": {
        "id": 3387562,
        ...
    },
    "mobile": true,
    "number": "+15141234459",
    "updated_at": "2018-04-09T18:05:00+00:00",
    "valid": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "Unauthenticated."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "Duplicate phone."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "No query results for model LeadPhone."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=405 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "Method not allowed."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "The given data was invalid.",
    "errors": {
        "number": [
            "The number format is invalid."
        ]
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
    "extension": null,
    "mobile": true,
    "number": "+15141234459"
}
```

