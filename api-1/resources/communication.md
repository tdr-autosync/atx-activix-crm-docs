# Communication

The following describes the available resources for a Communication. Check out the [Communication object](https://docs.crm.activix.ca/objects/communication) documentation for a complete list of attributes.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/communications" %}
{% api-method-summary %}
Create a communication
{% endapi-method-summary %}

{% api-method-description %}
Creates a communication. Returns the created communication.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
{% api-method-parameter name="lead\_id" type="integer" required=true %}
ID of the Lead associated with the communication.
{% endapi-method-parameter %}

{% api-method-parameter name="method" type="string" required=true %}
Possible values are **phone**, **email** or **sms**.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Possible values are **outgoing** or **incoming**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Communication created successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 42534452,
        "created_at": "2019-04-05T17:33:43+00:00",
        "updated_at": "2019-04-05T17:33:43+00:00",
        "method": "phone",
        "type": "outgoing",
        "call_status": "calling",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body Example**

```javascript
{
    "lead_id": 3387562,
    "method": "phone",
    "type": "outgoing",
    "call_status": "calling",
    ...
}
```

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/communications/:id" %}
{% api-method-summary %}
Update a communication
{% endapi-method-summary %}

{% api-method-description %}
Updates the specified communication by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated communication.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the communication to update.
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
{% api-method-parameter name="lead\_id" type="integer" required=true %}
ID of the Lead associated with the communication.
{% endapi-method-parameter %}

{% api-method-parameter name="method" type="string" required=true %}
Possible values are **phone**, **email** or **sms**.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Possible values are **outgoing** or **incoming**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Communication updated successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 42534452,
        "created_at": "2019-04-05T17:33:43+00:00",
        "updated_at": "2019-04-05T17:46:01+00:00",
        "method": "phone",
        "type": "incoming",
        "call_duration" : 25,
        "call_status": "answered",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body Example**

```javascript
{
    "call_duration" : 25,
    "call_status": "answered",
    ...
}
```

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/communications/:id/recording" %}
{% api-method-summary %}
Upload a recording
{% endapi-method-summary %}

{% api-method-description %}
Upload a recording for an existing communication.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the communication of the recording.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-type" type="string" required=true %}
Should be `multipart/form-data`.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="recording" type="string" required=true %}
Possible file types are **wav** or **mp3**.
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Recording uploaded successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Recording uploaded successfully."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Body **must** be of type `multipart/form-data`. 

Only one recording may be uploaded for a communication. If you re-upload a recording, it will overwrite the old one.

