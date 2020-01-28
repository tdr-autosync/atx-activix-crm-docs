# Lead

The following describes the available resources for a Lead. Check out the [Lead object](https://docs.crm.activix.ca/objects/lead) documentation for a complete list of attributes.

If you wish to run a full-text search to retrieve a lead, please see the [Search](search.md#search-leads) section of the documentation.

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/leads" %}
{% api-method-summary %}
Create a lead
{% endapi-method-summary %}

{% api-method-description %}
Creates a lead. Returns the created lead.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true type="string" %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" required=true type="string" %}
Should be `application/json`.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" required=true type="string" %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="type" type="string" required=true %}
The type of lead possible values are **email**, **phone**, **walk\_in**, **loyalty**, **renewal**, **sms**, **event** or **pre\_booking**.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
    "first_name": "John",
    "last_name": "Doe",
    "type": "email",
    "advisor": {
        "first_name": "Jane",
        "last_name": "Smith"
    },
    "emails": [
        {
						"type": "home",
            "address": "hello@example.com"
        }
    ],
    "phones": [
        {
            "number": "+15144321214",
            "extension": 12345,
						"type": "mobile"
        }
    ],
    "vehicles": [
        {
            "make": "Aston Martin",
            "model": "DB11",
            "year": 2018,
            "type": "wanted"
        },
			  {
            "make": "DMC",
            "model": "DeLorean",
            "year": 1981,
            "type": "exchange"
        }
    ]
}
```

The `advisor`, `bdc`, `commercial`, `service_agent` and `service_advisor` objects are only used to associate a user using their `first_name`, `last_name`, `email` or `id`.

{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/leads/:id" %}
{% api-method-summary %}
Retrieve a lead
{% endapi-method-summary %}

{% api-method-description %}
Retrieves the details of an existing lead. You only need to provide the lead identifier that was returned upon lead creation.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the lead to retrieve.
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
Lead retrieved successfully.
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
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

The list of available nested objects for a `Lead` is available [here](../../objects-1/lead.md#nested-objects).

{% api-method method="put" host="https://api.crm.activix.ca/v2" path="/leads/:id" %}
{% api-method-summary %}
Update a lead
{% endapi-method-summary %}

{% api-method-description %}
Updates the specified lead by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated lead.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the lead to update.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true type="string" %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" required=true type="string" %}
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
    "id": 1234567,
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

The `phones` collection only appends phone to the lead. See [here](phone.md) if you want to manage them.  
The `emails` collection only appends email to the lead. See [here](email.md) if you want to manage them.  
The `vehicles` collection only appends vehicle to the lead. See [here](vehicle.md) if you want to manage them.

{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/leads" %}
{% api-method-summary %}
List all leads
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of your leads. The leads are returned sorted by creation date, with the most recent leads appearing first.
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

{% api-method-parameter name="include" type="array" required=false %}
The nested objects to include.
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
            "id": 3387562,
            "created_at": "2018-04-09T18:05:00+00:00",
            "updated_at": "2018-04-09T18:07:00+00:00",
            "first_name": "John",
            "last_name": "Doe",
            ...
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
        "first": "https://api.crm.activix.ca/v2/leads?filter%5Bname%5D=John%20doe&include%5B0%5D=leadEmails&include%5B1%5D=leadPhones&include%5B2%5D=leadVehicles&page=1",
        "last": "https://api.crm.activix.ca/v2/leads?filter%5Bname%5D=John%20doe&include%5B0%5D=leadEmails&include%5B1%5D=leadPhones&include%5B2%5D=leadVehicles&page=47",
        "prev": null,
        "next": "https://api.crm.activix.ca/v2/leads?filter%5Bname%5D=John%20doe&include%5B0%5D=leadEmails&include%5B1%5D=leadPhones&include%5B2%5D=leadVehicles&page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 47,
        "path": "https://api.crm.activix.ca/v2/leads",
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

This endpoint supports [pagination](../pagination.md) so you can request more objects, or iterate through all results.

The list of available nested objects for a `Lead` is available [here](../../objects-1/lead.md#nested-objects).

You may narrow the results based on specific parameters. See [here](../filtering.md) to learn more on filtering.

| Parameter | Type | Description | [Wildcards](../filtering.md#wildcards) | [Operators](../filtering.md#operators) |
| :--- | :--- | :--- | :--- | :--- |
| `name` | string | Filter on the name or second contact of the lead. | ✅ | ❌ |
| `email` | string | Filter on any of the associated [Email](../../objects-1/email.md) objects. | ✅ | ❌ |
| `phone` | string | Filter on any of the associated [Phone](../../objects-1/phone.md) objects. | ✅ | ❌ |
| `created` | date | Filter on the creation date of the lead. | ❌ | ✅ |
| `updated` | date | Filter on the last update date of the lead. | ❌ | ✅ |

{% api-method method="post" host="https://api.crm.activix.ca/v2" path="/screenpop" %}
{% api-method-summary %}
Screen pop
{% endapi-method-summary %}

{% api-method-description %}
This endpoint serves a unique purpose. It is used to open a dialog displaying information for a call simultaneously sent to the user's telephone.
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
{% api-method-parameter name="lead\_id" type="string" required=false %}
The lead ID.
{% endapi-method-parameter %}

{% api-method-parameter name="lead\_did" type="string" required=false %}
The lead DID \(normally a number in E.164 format\).
{% endapi-method-parameter %}

{% api-method-parameter name="user\_id" type="string" required=false %}
The user ID.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_did" type="string" required=false %}
The user DID \(normally a number in E.164 format\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "The screen pop was triggered successfully."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

You _must_ provide a `lead_id` or `lead_did` _and_ a `user_id` or `user_did`.

{% hint style="info" %}
N.B. The endpoint is available, but the feature is not yet implemented in Activix CRM.
{% endhint %}

