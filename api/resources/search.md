# Search

The search sub-endpoint is used to run a full-text search.

The search endpoint returns 25 results by default. This endpoint supports [Pagination](../pagination.md) so your application can request more objects, or iterate through all results.

{% api-method method="get" host="https://api.crm.activix.ca/v2" path="/leads/search" %}
{% api-method-summary %}
Search Leads
{% endapi-method-summary %}

{% api-method-description %}
Searches for leads using the specified query. The leads are returned sorted by creation date, with the most recent leads appearing first.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer token.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
Should be `application/json`.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="query" type="string" %}
The search query \(name, phone or email\).
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Search completed successfully.
{% endapi-method-response-example-description %}

```javascript
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
        "first": "https://api.crm.activix.ca/v2/leads/search?query=John&page=1",
        "last": "https://api.crm.activix.ca/v2/leads/search?query=John&page=47",
        "prev": null,
        "next": "https://api.crm.activix.ca/v2/leads/search?query=John&page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 47,
        "path": "https://api.crm.activix.ca/v2/leads/search",
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

Currently, the search tries to find a matching result across these fields:

* `name`
* `second_contact`
* `number` in any of the phone objects
* `address` in any of the email objects
* `postal_code` 
  * must be 3 or 6 characters 
  * must not include spaces
  * search is case insensitive

### Examples

```text
/leads/search?query=john_doe
```

```text
/leads/search?query=5147894561
```

```text
/leads/search?query=myemail@activix.ca
```

```text
/leads/search?query=h2p
```

```text
/leads/search?query=h2p3h7
```

