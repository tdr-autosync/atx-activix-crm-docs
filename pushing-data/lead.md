# Lead

Here is an example of request that Activix CRM can make to push data to an external web service. Refer to the [Lead object](https://docs.crm.activix.ca/objects/lead) documentation to see all the attributes that may be included in the request.

All the responses in the example **must** be handled \(you may handle more if you want\).

{% api-method method="post" host="https://your-url.com" path="/example" %}
{% api-method-summary %}
Create a lead
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
OAuth 2 or Basic Auth authentication credentials.
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="Content-Type" required=false %}
Should be `application/json`.
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="Accept" required=false %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Lead successfully created.
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
Unknown Account \(Dealer\).
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Unknown Account."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error.
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

#### Body Example

```javascript
{
    "id": 3387562,
    "first_name": "John",
    "last_name": "Doe",
    "civility": "mr",
    "second_contact": "ABC Motors",
    "second_contact_civility": null,
    "division": "new",
    "type": "walk_in",
    "source": "Lespacs",
    "address_line1": "123 av. Riverwood",
    "address_line2": "Suite 200",
    "postal_code": "J1E4Y7",
    "city": "Montreal",
    "province": "QC",
    "country": "CA",
    "locale": "en",
    "birth_date": "1990-04-10",
    "gender": 1,
    "account": {
        "id": 66,
        ...
    },
    "advisor": {
        "id": 51112,
        ...
    },
    "emails": [
        {
            "id": 3664451,
            ...
        },
        ...
    ],
    "phones": [
        {
            "id": 9465546,
            ...
        },
        ...
    ],
    "vehicles": [
        {
            "id": 4542214,
            ...
        },
        ...
    ],
    "created_at": "2018-04-09T18:05:00+00:00",
    "updated_at": "2018-04-09T18:07:00+00:00"
}
```

