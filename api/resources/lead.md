# Lead

The following describes the available resources for a Lead. Check out the [Lead object](https://docs.crm.activix.ca/objects/lead) documentation for a complete list of attributes.

If you wish to run a full-text search to retrieve a lead, please see the [Search](search.md#search-leads) section of the documentation.

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/leads" method="post" summary="Create a lead" %}
{% swagger-description %}
Creates a lead. Returns the created lead.
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
{% endswagger-parameter %}

{% swagger-parameter in="query" name="trigger_alerts" type="boolean" %}
If 

`true`

, triggers the new lead alert (like a normal request would).

\


Default is 

`false`

.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="string" %}
The type of lead possible values are 

**email**

, 

**phone**

, 

**walk_in**

, 

**loyalty**

, 

**renewal**

, 

**sms**

, 

**event**

, 

**pre_booking**

 or 

**web_order**

.
{% endswagger-parameter %}

{% swagger-response status="201" description="Lead created successfully." %}
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
{% endswagger-response %}
{% endswagger %}

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

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/leads/:id" method="get" summary="Retrieve a lead" %}
{% swagger-description %}
Retrieves the details of an existing lead. You only need to provide the lead identifier that was returned upon lead creation.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
The ID of the lead to retrieve.
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

{% swagger-response status="200" description="Lead retrieved successfully." %}
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
{% endswagger-response %}
{% endswagger %}

The list of available nested objects for a `Lead` is available [here](../objects/lead.md#nested-objects).

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/leads/:id" method="put" summary="Update a lead" %}
{% swagger-description %}
Updates the specified lead by setting the values of the parameters passed. Any parameters not provided will be left unchanged. The request returns the updated lead.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
The ID of the lead to update.
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

{% swagger-response status="200" description="Lead updated successfully." %}
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
{% endswagger-response %}
{% endswagger %}

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

The `phones` collection only appends phone to the lead. See [here](phone.md) if you want to manage them.\
The `emails` collection only appends email to the lead. See [here](email.md) if you want to manage them.\
The `vehicles` collection only appends vehicle to the lead. See [here](vehicle.md) if you want to manage them.

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/leads" method="get" summary="List all leads" %}
{% swagger-description %}
Returns a list of your leads. The leads are returned sorted by creation date, with the most recent leads appearing first.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
Bearer token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" type="string" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="page" type="integer" %}
The page result you wish to see.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="per_page" type="integer" %}
The number of desired results.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="include" type="array" %}
The nested objects to include.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="filter" type="array" %}
The filters you wish to apply.
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
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
{% endswagger-response %}
{% endswagger %}

This endpoint supports [pagination](../pagination.md) so you can request more objects, or iterate through all results.

The list of available nested objects for a `Lead` is available [here](../objects/lead.md#nested-objects).

You may narrow the results based on specific parameters. See [here](../filtering.md) to learn more on filtering.

| Parameter     | Type   | Description                                                             | [Wildcards](../filtering.md#wildcards) | [Operators](../filtering.md#operators) |
| ------------- | ------ | ----------------------------------------------------------------------- | -------------------------------------- | -------------------------------------- |
| `name`        | string | Filter on the name or second contact of the lead.                       | ✅                                      | ❌                                      |
| `email`       | string | Filter on any of the associated [Email](../objects/email.md) objects.   | ✅                                      | ❌                                      |
| `phone`       | string | Filter on any of the associated [Phone](../objects/phone.md) objects.   | ✅                                      | ❌                                      |
| `postal_code` | string | Filter on the postal code of the lead.                                  | ❌                                      | ❌                                      |
| `created_at`  | date   | Filter on the creation date of the lead.                                | ❌                                      | ✅                                      |
| `updated_at`  | date   | Filter on the last update date of the lead.                             | ❌                                      | ✅                                      |
| `sale_date`   | date   | Filter on the sale date of the lead.                                    | ❌                                      | ✅                                      |
| `division`    | enum   | <p>Filter on the division of the lead.</p><p>See below for details.</p> | ❌                                      |                                        |

###

#### Division filter

Leads can be filtered by `division` using the following values:

* new
* used
* service
* none

The division filtering uses the `or` operator. Multiple values can be filtered simultaneously by using comma separated values (i.e. `used,none`).

You may find usage examples [here](https://docs.crm.activix.ca/api/filtering#examples).

{% hint style="warning" %}
The use of division filters may impact the performance of the request. We **strongly** suggest including this filter after a date filter has been applied to optimize the efficiency of the request.
{% endhint %}

{% swagger baseUrl="https://api.crm.activix.ca/v2" path="/screenpop" method="post" summary="Screen pop" %}
{% swagger-description %}
This endpoint serves a unique purpose. It is used to open a dialog displaying information for a call simultaneously sent to the user's telephone.
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
{% endswagger-parameter %}

{% swagger-parameter in="body" name="lead_id" type="string" %}
The lead ID.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="lead_did" type="string" %}
The lead DID (normally a number in E.164 format).
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_id" type="string" %}
The user ID.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="user_did" type="string" %}
The user DID (normally a number in E.164 format)
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```javascript
{
    "message": "The screen pop was triggered successfully."
}
```
{% endswagger-response %}
{% endswagger %}

You _must_ provide a `lead_id` or `lead_did` _and_ a `user_id` or `user_did`.
