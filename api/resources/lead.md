# Lead

The following describes the available resources for a Lead. Check out the [Lead object](https://docs.crm.activix.ca/objects/lead) documentation for a complete list of attributes.

{% api-method method="get" host="https://crm.activix.ca/api/v2" path="/leads/search" %}
{% api-method-summary %}
Search a lead
{% endapi-method-summary %}

{% api-method-description %}
Run a full-text search on leads. Returns a collection Lead object.
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

