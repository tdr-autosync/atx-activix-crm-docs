# Lead

The following describes the available resources for a Lead. Check out the [Lead object](https://docs.crm.activix.ca/objects/lead) documentation for a complete list of attributes.

{% api-method method="get" host="https://crm.activix.ca/api/v2" path="/leads/search" %}
{% api-method-summary %}
Search a lead
{% endapi-method-summary %}

{% api-method-description %}
Run a full-text search on leads. Returns a collection of Lead object.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="query" type="string" required=false %}
The search query \(name, phone or email\).
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "data": [
        {
            "id": 3387562,
            "created_at": "2018-04-09T18:05:00+00:00",
            "updated_at": "2018-04-09T18:07:00+00:00",
            "first_name": "John",
            "last_name": "Doe",
            ...
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
            ]
        },
        ...
    ],
    "links": {
        "first": "https://crm.activix.ca/api/v2/leads/search?query=John&page=1",
        "last": "https://crm.activix.ca/api/v2/leads/search?query=John&page=47",
        "prev": null,
        "next": "https://crm.activix.ca/api/v2/leads/search?query=John&page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 47,
        "path": "https://crm.activix.ca/api/v2/leads/search",
        "per_page": 25,
        "to": 25,
        "total": 1161
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

The search returns 25 results by default. The results are sorted by latest `created_at`. This endpoint supports pagination so you can request more objects, or iterate through all results.

Currently, the search try to find a matching result in these fields:

* `name`
* `second_contact`
* `number` in any of the phone objects
* `address` in any of the email objects

{% api-method method="post" host="https://crm.activix.ca/api/v2" path="/leads" %}
{% api-method-summary %}
Create a lead
{% endapi-method-summary %}

{% api-method-description %}
Create a lead. Returns the created lead.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" required=true %}
OAuth 2 or Basic Auth authentication credentials.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" %}
Should be application/json.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" %}
Should be application/json.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Lead created successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 3387562,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "first_name": "John",
        "last_name": "Doe",
        ...
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
    "account_id": 44,
    "first_name": "John",
    "last_name": "Doe",
    "lead_type": "email",
    ...
    "advisor": {
        "first_name": "John",
        "last_name": "Doe"
    },
    "emails": [
        {
            "address": "hello@example.com"
        },
        ...
    ],
    "phones": [
        {
            "number": "+15144321214"
            "extension": 12345,
        },
        ...
    ],
    "vehicles": [
        {
            "make": "Aston Martin",
            "model": "DB11",
            "year": 2018,
            "type": "wanted"
            ...
        },
        ...
    ]
}
```

The `advisor`, `bdc`, `commercial`, `service_agent` and `service_advisor` objects are only used to associate a user using their `first_name`, `last_name`, `email` or `id`.

{% api-method method="put" host="https://crm.activix.ca/api/v2" path="/leads/:id" %}
{% api-method-summary %}
Update a lead
{% endapi-method-summary %}

{% api-method-description %}
Update a lead. Returns the updated lead.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the lead to update.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentification" required=true %}
OAuth 2 or Basic Auth authentication credentials.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" %}
Should be application/json.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" %}
Should be application/json.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Lead updated successfully.
{% endapi-method-response-example-description %}

```javascript
{
    "data": {
        "id": 3387562,
        "created_at": "2018-04-09T18:05:00+00:00",
        "updated_at": "2018-04-09T18:07:00+00:00",
        "first_name": "John",
        "last_name": "Doe",
        ...
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
    "first_name": "John",
    "last_name": "Doe",
    ...
    "advisor": {
        "first_name": "John",
        "last_name": "Doe"
    },
    ...
}
```

The `advisor`, `bdc`, `commercial`, `service_agent` and `service_advisor` objects are only used to associate a user using their `first_name`, `last_name`, `email` or `id`.

The `phones` collection only appends phone to the lead. Go to the ["Phone" documentation](https://docs.crm.activix.ca/api/resources/phone) if you want to manage them.

The `emails` collection only appends email to the lead. Go to the ["Email" documentation](https://docs.crm.activix.ca/api/resources/email) if you want to manage them.

The `vehicles` collection only appends vehicle to the lead. Go to the ["Vehicle" documentation](https://docs.crm.activix.ca/api/resources/vehicle) if you want to manage them.
