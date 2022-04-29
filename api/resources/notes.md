# Notes

The following describes the available resources for a Note. Check out the [Note Object](notes.md) documentation for a complete list of attributes.

{% swagger method="post" path="/lead/:lead_id/notes" baseUrl="https://api.crm.activix.ca/v2" summary="Create a note" %}
{% swagger-description %}
_Creates a note in the specified lead. Returns the created note._
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
Bearer token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="content" %}
Text representing the content of the note. Required when 

`file_url`

 is not provided.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="file_url" %}
Link representing attachment to be added to the note. Required when 

`content is not provided.`
{% endswagger-parameter %}

{% swagger-parameter in="body" name="parent_id" type="integer" %}
Representing the id of the note being replied to.
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
  "data": {
    "id": 11,
    "parent_id": null,
    "created_at": "2022-02-25T13:20:13+00:00",
    "updated_at": "2022-02-25T13:20:13+00:00",
    "lead_id": 102,
    "user_id": 50,
    "content": "Customer requested a call back next week.",
    "file_url": ""
  }
}
```
{% endswagger-response %}
{% endswagger %}

Body example

```
{
    "content": "Customer requested a call next week",
}
```

{% swagger method="put" path="/lead/:lead_id/notes/:note_id" baseUrl="https://api.crm.activix.ca/v2" summary="Update an existing note" %}
{% swagger-description %}
_Updates an existing note in the specified lead. Returns the updated note._
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
Bearer token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="content" %}
Text representing the content of the note. Required when 

`file_url`

 is not provided and existing note does not have a value set for 

`file_url`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="file_url" %}
Link representing attachment to be added to the note. Required when 

`content is not provided and existing note does not have a value set`

 for 

`content`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="parent_id" type="integer" %}
Representing the id of the note being replied to.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
  "data": {
    "id": 11,
    "parent_id": null,
    "created_at": "2022-02-25T13:20:13+00:00",
    "updated_at": "2022-02-25T13:20:13+00:00",
    "lead_id": 102,
    "user_id": 50,
    "content": "Customer requested a call back next week.",
    "file_url": ""
  }
}
```
{% endswagger-response %}
{% endswagger %}

Body example

```
{
    "parent_id": 3,
    "content": "Customer requested a call next week",
}
```
