# Call Log

The following describes the available resources for a Call Log. Check out the [Call Log object](../objects/call-log.md) documentation for a complete list of attributes.

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/call-logs" method="post" summary="Create a call log" %}
{% swagger-description %}
Creates a call log. Returns the created call log with the associated Lead. 

\




\


Use this endpoint to indicate that a call has been initiated or to log a completed call. If a 

**media_url**

 is provided in the payload it will be uploaded to our system and the communication will contain the audio playback.
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

{% swagger-parameter in="body" name="status" type="string" %}
The status of the call. Possible values are 

**answered**

, 

**attempted**

, 

**calling**

, 

**error**

, 

**interrupted**

, 

**pending**

 or 

**unanswered**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="direction" type="string" %}
The direction of the call. Possible values are 

**outgoing**

 or 

**incoming**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="duration" type="integer" %}
The duration of the call in seconds. 

\




\




_*Provide this parameter to indicate that the call is completed._
{% endswagger-parameter %}

{% swagger-parameter in="body" name="start_at" type="string" %}
ISO 8601 datetime representing the start of the call.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="end_at" type="string" %}
ISO 8601 datetime representing the end of the call. 

\




\




_*Provide this parameter to indicate that the call is completed._
{% endswagger-parameter %}

{% swagger-parameter in="body" name="media_url" type="string" %}
The web URL of the media file of the call. Possible file types are 

**wav**

 or 

**mp3**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="from" type="string" %}
The phone number from where the call originated in E.164 format.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="to" type="string" %}
The phone number to where the call is targeted in E.164 format.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_did" type="string" %}
The phone number in E.164 format of the user who is the target of the call.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="string" %}
The email of the user who is the target of the call. 
{% endswagger-parameter %}

{% swagger-response status="201" description="Call Log created successfully." %}
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
{% endswagger-response %}
{% endswagger %}

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

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/call-logs/:id" method="put" summary="Update a call log" %}
{% swagger-description %}
Updates the specified call log by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated call log.

\




\


Use this endpoint to change status or information about an existing call or indicate that the call has ended. If a 

**media_url**

 is provided in the payload it will be uploaded to our system and the communication will contain the audio playback.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
The ID of the call log to update.
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

{% swagger-parameter in="body" name="status" type="string" %}
The status of the call. Possible values are 

**answered**

, 

**attempted**

, 

**calling**

, 

**error**

, 

**interrupted**

, 

**pending**

 or 

**unanswered**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="duration" type="integer" %}
The duration of the call in seconds.

\




\




_*Provide this parameter to indicate that the call is completed._
{% endswagger-parameter %}

{% swagger-parameter in="body" name="end_at" type="string" %}
ISO 8601 datetime representing the end of the call.

\




\




_*Provide this parameter to indicate that the call is completed._
{% endswagger-parameter %}

{% swagger-parameter in="body" name="media_url" type="string" %}
The web URL of the media file of the call. Possible file types are 

**wav**

 or 

**mp3**

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_did" type="string" %}
The phone number in E.164 format of the user who is the target of the call.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_email" type="string" %}
The email of the user who is the target of the call.
{% endswagger-parameter %}

{% swagger-response status="200" description="Communication updated successfully." %}
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
{% endswagger-response %}
{% endswagger %}

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
