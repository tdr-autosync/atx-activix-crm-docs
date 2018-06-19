# Email

{% api-method method="post" host="https://crm.activix.ca/api/v2" path="/lead-emails" %}
{% api-method-summary %}
Create a email
{% endapi-method-summary %}

{% api-method-description %}
Create a email. Returns the created email.
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 34566,
    "address": "test@activix.ca",
    "created_at": "2018-04-09T18:05:00+00:00",
    "lead": {
        "id": 3387562,
        ...    
    },
    "updated_at": "2018-04-09T18:05:00+00:00",
    "valid": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
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
    "address": "test@activix.ca"
}
```

{% api-method method="put" host="https://crm.activix.ca/api/v2" path="/lead-phones/:id" %}
{% api-method-summary %}
Update a email
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the email to update
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

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Body Example

```javascript
{    
    "address": "test@activix.ca"
}
```

