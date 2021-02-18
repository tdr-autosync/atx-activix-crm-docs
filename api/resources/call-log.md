# Call Log

The following describes the available resources for a Call Log. Check out the [Call Log object](../objects/call-log.md) documentation for a complete list of attributes.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/call-logs" %}
{% api-method-summary %}
Create a call log
{% endapi-method-summary %}

{% api-method-description %}
Creates a call log. Returns the created call log with the associated Lead.   
  
Use this endpoint to indicate that a call has been initiated or to log a completed call. If a **media\_url** is provided in the payload it will be uploaded to our system and the communication will contain the audio playback.
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
{% api-method-parameter name="status" type="string" required=true %}
The status of the call. Possible values are **answered**, **attempted**, **calling**, **error**, **interrupted**, **pending** or **unanswered**.
{% endapi-method-parameter %}

{% api-method-parameter name="direction" type="string" required=true %}
The direction of the call. Possible values are **outgoing** or **incoming**.
{% endapi-method-parameter %}

{% api-method-parameter name="duration" type="integer" required=false %}
The duration of the call in seconds.   
  
_\*Provide this parameter to indicate that the call is completed._
{% endapi-method-parameter %}

{% api-method-parameter name="start\_at" type="string" required=true %}
ISO 8601 datetime representing the start of the call.
{% endapi-method-parameter %}

{% api-method-parameter name="end\_at" type="string" required=false %}
ISO 8601 datetime representing the end of the call.   
  
_\*Provide this parameter to indicate that the call is completed._
{% endapi-method-parameter %}

{% api-method-parameter name="media\_url" type="string" required=false %}
The web URL of the media file of the call. Possible file types are **wav** or **mp3**.
{% endapi-method-parameter %}

{% api-method-parameter name="from" type="string" required=true %}
The phone number from where the call originated in E.164 format.
{% endapi-method-parameter %}

{% api-method-parameter name="to" type="string" required=true %}
The phone number to where the call is targeted in E.164 format.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_did" type="string" required=false %}
The phone number in E.164 format of the user who is the target of the call.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_email" type="string" required=false %}
The email of the user who is the target of the call. 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Call Log created successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 42534452,
        "created_at": "2019-04-05T17:33:43+00:00",
        "updated_at": "2019-04-05T17:33:43+00:00",
        "communication_id": 521345,
        "start_at": "2021-04-22T01:00:00-05:00",
        "direction": "outgoing",
        "status": "calling",
        "from": "+15146526793",
        "to": "+14182579084",
        "lead": {
            "id": 2093021,
            "first_name": "John",
            "last_name": "Doe",
            ...
        }
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

If you want to indicate that a call is completed, **end\_at** and **duration** parameters are mandatory.

**Body Example**

```javascript
{
    "direction": "outgoing",
    "status": "calling",
    "from": "+15146526793",
    "to": "+14182579084",
    "start_at": "2021-04-22T01:00:00-05:00",
    ...
}
```

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/call-logs/:id" %}
{% api-method-summary %}
Update a call log
{% endapi-method-summary %}

{% api-method-description %}
Updates the specified call log by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated call log.  
  
Use this endpoint to change status or information about an existing call or indicate that the call has ended. If a **media\_url** is provided in the payload it will be uploaded to our system and the communication will contain the audio playback.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the call log to update.
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
{% api-method-parameter name="status" type="string" required=true %}
The status of the call. Possible values are **answered**, **attempted**, **calling**, **error**, **interrupted**, **pending** or **unanswered**.
{% endapi-method-parameter %}

{% api-method-parameter name="duration" type="integer" required=false %}
The duration of the call in seconds.  
  
_\*Provide this parameter to indicate that the call is completed._
{% endapi-method-parameter %}

{% api-method-parameter name="end\_at" type="string" required=false %}
ISO 8601 datetime representing the end of the call.  
  
_\*Provide this parameter to indicate that the call is completed._
{% endapi-method-parameter %}

{% api-method-parameter name="media\_url" type="string" required=false %}
The web URL of the media file of the call. Possible file types are **wav** or **mp3**.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_did" type="string" required=false %}
The phone number in E.164 format of the user who is the target of the call.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_email" type="string" required=false %}
The email of the user who is the target of the call.
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
        "updated_at": "2019-04-05T17:33:43+00:00",
        "communication_id": 521345,
        "start_at": "2021-04-22T01:00:00-05:00",
        "direction": "outgoing",
        "status": "answered",
        "from": "+15146526793",
        "to": "+14182579084",
        "end_at": "2021-04-22T01:00:00-05:00",
        "duration": 345,
        "lead": {
            "id": 2093021,
            "first_name": "John",
            "last_name": "Doe",
            ...
        }
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

If you want to indicate that a call is completed, **end\_at** and **duration** parameters are mandatory.

**Body Example**

```javascript
{
    "status" : "answered",
    "end_at": "2021-04-22T01:00:00-05:00",
    "duration": 345,
    "media_url": "http://www.example.com/audio.mp3",
    ...
}
```

