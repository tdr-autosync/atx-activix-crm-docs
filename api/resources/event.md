# Event

The following describes the available resources for an Event. Check out the [Event object](../objects/event.md) documentation for a complete list of attributes.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/events" %}
{% api-method-summary %}
Create an event
{% endapi-method-summary %}

{% api-method-description %}
Creates an event. Returns the created event.
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
{% api-method-parameter name="owner.first\_name" type="string" required=false %}
The first name of the user to whom you want to assign the event.  
This field is required when **owner.last\_name** is present.
{% endapi-method-parameter %}

{% api-method-parameter name="owner.last\_name" type="string" required=false %}
The last name of the user to whom you want to assign the event.  
This field is required when **owner.first\_name** is present.
{% endapi-method-parameter %}

{% api-method-parameter name="owner.id" type="integer" required=false %}
The ID of the user to whom you want to assign the event.  
This field is required if **owner.first\_name** and **owner.last\_name** are not present.
{% endapi-method-parameter %}

{% api-method-parameter name="end\_at" type="string" required=true %}
ISO 8601 datetime representing the end of the event.
{% endapi-method-parameter %}

{% api-method-parameter name="start\_at" type="string" required=true %}
ISO 8601 datetime representing the beginning of the task.
{% endapi-method-parameter %}

{% api-method-parameter name="lead\_id" type="integer" required=true %}
ID of the Lead associated with the event.  
Required for all type, except **other**.
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=true %}
The title of the event.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Possible values are **appointment**, **phone\_appointment**, **delivery** or **other**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Event created successfully.
{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 6231885,
        "lead_id": 3387562,
        "owner_id": 87,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "title": "Appointment for John",
        "type": "appointment",
        "start_at": "2020-06-04T15:15:00-04:00",
        "end_at": "2020-06-04T16:45:00-04:00",
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
    "owner": {
        "id": 87
    },
    "title": "Appointment for John",
    "type": "appointment",
    "start_at": "2020-06-04T15:15:00-04:00",
    "end_at": "2020-06-04T16:45:00-04:00",
    ...
}
```

{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/events/:id" %}
{% api-method-summary %}
Retrieve an event
{% endapi-method-summary %}

{% api-method-description %}
Retrieves the details of an existing event. You only need to provide the event identifier that was returned upon event creation.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the event to retrieve.
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Event retrieved successfully.
{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 6231885,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "title": "Appointment for John",
        "type": "appointment",
        "start_at": "2020-06-04T15:15:00-04:00",
        "end_at": "2020-06-04T16:45:00-04:00",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/events/:id" %}
{% api-method-summary %}
Update an event
{% endapi-method-summary %}

{% api-method-description %}
Update the specified event by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated event.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the event to update.
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Event updated successfully.
{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 6231885,
        "lead_id": 3387562,
        "owner_id": 87,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "title": "Updated Appointment for John",
        "type": "appointment",
        "start_at": "2020-06-04T15:15:00-04:00",
        "end_at": "2020-06-04T16:45:00-04:00",
        "completed_at": "2020-06-04T17:15:00-04:00",
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
    "title": "Updated Appointment for John",
    "completed_at": "2020-06-04T17:15:00-04:00"
    ...
}
```



{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/events" %}
{% api-method-summary %}
List all events
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of your events. The events are returned sorted by creation date, with the most recent events appearing first.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="page" type="integer" required=false %}
The page result you wish to see.
{% endapi-method-parameter %}

{% api-method-parameter name="per\_page" type="integer" required=false %}
The number of desired results.
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="array" required=false %}
The filters you wish to apply.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "data": [
        {
            "id": 6231885,
            "created_at": "2018-04-09T18:05:00+00:00",
            "updated_at": "2018-04-09T18:07:00+00:00",
            "title": "Appointment for John",
            "type": "appointment",
            "start_at": "2020-06-04T15:15:00-04:00",
            "end_at": "2020-06-04T16:45:00-04:00",
        },
        ...
    ],
    "links": {
        "first": "https://api.crm.activix.ca/v2/events?filter%5Btype%5D=appointment&page=1",
        "last": "https://api.crm.activix.ca/v2/events?filter%5Btype%5D=appointment&page=5",
        "prev": null,
        "next": "https://api.crm.activix.ca/v2/events?filter%5Btype%5D=appointment&page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 5,
        "path": "https://api.crm.activix.ca/v2/events",
        "per_page": 25,
        "to": 25,
        "total": 114,
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

This endpoint supports [pagination](../pagination.md) so you can request more objects, or iterate through all results.

You may narrow the results based on specific parameters. See [here](../filtering.md) to learn more on filtering.

| Parameter | Type | Description | [Wildcards](../filtering.md#wildcards) | [Operators](../filtering.md#operators) |
| :--- | :--- | :--- | :--- | :--- |
| `type` | string | Filter on the type of the event. Possible values are **appointment**, **phone\_appointment**, **delivery** or **other**. | ❌ | ❌ |
| `canceled` | bool | Filter on the canceled state of the event. | ❌ | ❌ |
| `completed` | bool | Filter on the completed state of the event. | ❌ | ❌ |
| `confirmed` | bool | Filter on the confirmed state of the event. | ❌ | ❌ |
| `no_show` | bool | Filter on the no\_show state of the event. | ❌ | ❌ |
| `start_at` | date | Filter on the start date of the event. | ❌ | ✅ |
| `end_at` | date | Filter on the end date of the event. | ❌ | ✅ |
| `created_at` | date | Filter on the creation date of the event. | ❌ | ✅ |
| `updated_at` | date | Filter on the last update date of the event. | ❌ | ✅ |

