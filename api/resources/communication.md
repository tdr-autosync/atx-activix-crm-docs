# Communication

The following describes the available resources for a Communication. Check out the [Communication object](https://docs.crm.activix.ca/objects/communication) documentation for a complete list of attributes.

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/communications" method="post" summary="Create a communication" %}
{% swagger-description %}
Creates a communication. Returns the created communication.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Bearer token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" type="string" %}
Should be 

`application/json`

.

\



{% endswagger-parameter %}

{% swagger-parameter in="body" name="lead_id" type="integer" %}
ID of the Lead associated with the communication.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="method" type="string" %}
Possible values are 

**phone**

, 

**email**

 or 

**sms**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
Possible values are 

**outgoing**

 or 

**incoming**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="executed_at" type="string" %}
ISO 8601 datetime representing the date the communication took place. 
{% endswagger-parameter %}

{% swagger-parameter in="body" name="executed_by" type="integer" %}
The ID of that that performed the communication.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="description" %}
Text describing the communication.
{% endswagger-parameter %}

{% swagger-response status="201" description="Communication created successfully." %}
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
{% endswagger-response %}
{% endswagger %}

**Body Example**

```javascript
{
    "lead_id": 3387562,
    "method": "phone",
    "type": "outgoing",
    "call_status": "calling",
    "description": "Call made to customer, reached voicemeail.",
    "executed_at": "2022-01-22T01:00:00-05:00",
    "executed_by": 5000,
    ...
}
```

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/communications/:id" method="put" summary="Update a communication" %}
{% swagger-description %}
Updates the specified communication by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated communication.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
The ID of the communication to update.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Bearer token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" type="string" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="lead_id" type="integer" %}
ID of the Lead associated with the communication.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="method" type="string" %}
Possible values are 

**phone**

, 

**email**

 or 

**sms**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
Possible values are 

**outgoing**

 or 

**incoming**

.
{% endswagger-parameter %}

{% swagger-response status="200" description="Communication updated successfully." %}
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
{% endswagger-response %}
{% endswagger %}

**Body Example**

```javascript
{
    "call_duration" : 25,
    "call_status": "answered",
    ...
}
```

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/communications/:id/recording" method="post" summary="Upload a recording" %}
{% swagger-description %}
Upload a recording for an existing communication.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
The ID of the communication of the recording.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Bearer token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-type" type="string" %}
Should be 

`multipart/form-data`

.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" type="string" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="recording" type="string" %}
Possible file types are 

**wav**

 or 

**mp3**

.
{% endswagger-parameter %}

{% swagger-response status="200" description="Recording uploaded successfully." %}
```javascript
{
    "message": "Recording uploaded successfully."
}
```
{% endswagger-response %}
{% endswagger %}

Body **must** be of type `multipart/form-data`.&#x20;

Only one recording may be uploaded for a communication. If you re-upload a recording, it will overwrite the old one.
