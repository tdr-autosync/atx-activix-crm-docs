# Task

The following describes the available resources for a Task. Check out the [Task object](../objects/task.md) documentation for a complete list of attributes.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/tasks" %}
{% api-method-summary %}
Create a task
{% endapi-method-summary %}

{% api-method-description %}
Creates a task. Returns the created task.
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
The first name of the user to whom you want to assign the task.  
This field is required when **owner.last\_name** is present.
{% endapi-method-parameter %}

{% api-method-parameter name="owner.last\_name" type="string" required=false %}
The last name of the user to whom you want to assign the task.  
This field is required when **owner.first\_name** is present.
{% endapi-method-parameter %}

{% api-method-parameter name="owner.id" type="number" required=false %}
The ID of the user to whom you want to assign the task.  
This field is required if **owner.first\_name** and **owner.last\_name** are not present.
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="string" required=true %}
ISO 8601 datetime representing the date and time of the task.
{% endapi-method-parameter %}

{% api-method-parameter name="lead\_id" type="integer" required=true %}
ID of the Lead associated with the task.
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=true %}
The title of the task.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Possible values are **call**, **email**, **sms** or **csi**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Task created successfully.
{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 6231885,
        "lead_id": 3387562,
        "owner_id": 87,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "title": "Call for John",
        "type": "call",
        "date": "2020-06-04T15:15:00-04:00",
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
        "id": 87,
    },
    "title": "Call for John",
    "type": "call",
    "date": "2020-06-04T15:15:00-04:00",
    ...
}
```

{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/tasks/:id" %}
{% api-method-summary %}
Retrieve a task
{% endapi-method-summary %}

{% api-method-description %}
Retrieves the details of an existing task. You only need to provide the task identifier that was returned upon task creation.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the task to retrieve.
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
Task retrieved successfully.
{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 6231885,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "title": "Call for John",
        "type": "call",
        "date": "2020-06-04T15:15:00-04:00",
        ...
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/tasks/:id" %}
{% api-method-summary %}
Update a task
{% endapi-method-summary %}

{% api-method-description %}
Update the specified task by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated task.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the task to update.
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
{% api-method-parameter name="title" type="string" required=false %}
The title of the task.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Task updated successfully.
{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 6231885,
        "lead_id": 3387562,
        "owner_id": 87,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "title": "Updated Call for John",
        "type": "call",
        "date": "2020-06-04T15:15:00-04:00",
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
    "title": "Updated Call for John",
    ...
}
```

{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/tasks" %}
{% api-method-summary %}
List all tasks
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of your tasks. The tasks are returned sorted by creation date, with the most recent tasks appearing first.
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
            "title": "Call for John",
            "type": "call",
            "date": "2020-06-04T15:15:00-04:00",
        },
        ...
    ],
    "links": {
        "first": "https://api.crm.activix.ca/v2/tasks?filter%5Btype%5D=call&page=1",
        "last": "https://api.crm.activix.ca/v2/tasks?filter%5Btype%5D=call&page=5",
        "prev": null,
        "next": "https://api.crm.activix.ca/v2/tasks?filter%5Btype%5D=call&page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 5,
        "path": "https://api.crm.activix.ca/v2/tasks",
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
| `type` | string | Filter on the type of the task. Possible values are **call**, **email**, **csi** or **sms**. | ❌ | ❌ |
| `completed` | bool | Filter on the completed state of the task. | ❌ | ❌ |
| `date` | date | Filter on the date of the task. | ❌ | ✅ |
| `created_at` | date | Filter on the creation date of the task. | ❌ | ✅ |
| `updated_at` | date | Filter on the last update date of the task. | ❌ | ✅ |

