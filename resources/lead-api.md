# Leads

{% hint style="warning" %}
This documentation is in construction. Some sections might be missing.
{% endhint %}

The representation of a lead is called a `Lead` object. You can retrieve individual leads as well as list all leads. Leads are identified by an incremental ID.

## The lead object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the lead. |
| `first_name` | string | First\_name of the lead. |
| `last_name` | string | Last name of the lead. |
| `civility` | string | The social title of the lead. Possible values are **`mr`**, **`ms`**, **`miss`**, **`dr`**, **`me`.** |
| `second_contact` | string | Optional second contact for the lead. May be a person or a business. |
| `second_contact_civility` | string | The social title of the second contact for the lead. Possible values are **`mr`**, **`ms`**, **`miss`**, **`dr`**, **`me`**. |
| `division` | string | Division of the lead. Possible values are **`new`**, **`used`** or **`service`**. |
| `type` | string | The type of lead. Possible values are **`email`**, **`phone`**, **`walk_in`**, **`loyalty`**, **`renewal`**, **`sms`**, **`event`** and **`pre_booking`**. |
| `source` | string | The source where the lead originally from. |
| `address_line1` | string | Address \(line 1\). |
| `address_line2` | string | Address \(line 2\). |
| `postal_code` | string | ZIP or postal code. |
| `city` | string | City/District/Suburb/Town/Village. |
| `province` | string | Two letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166) representing the State/Province of the lead. |
| `country` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166-2) representing the country of the lead. |
| `locale` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) representing the locale \(language\) of the lead. |
| `birth_date` | string | [ISO date](https://en.wikipedia.org/wiki/ISO_8601) representing the date of birth of the lead. |
| `gender` | integer | Single-digit [ISO code](https://en.wikipedia.org/wiki/ISO/IEC_5218) representing the gender of the lead. |
| `advisor` | object | User object representing the associated advisor. |
| `phones` | array | Array of phone objects. |
| `emails` | array | Array of email objects. |
| `vehicles` | array | Array of vehicle objects. |

{% hint style="info" %}
You may request additional fields by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

{% api-method method="get" host="https://crm.activix.ca/api/v2" path="/leads/search" %}
{% api-method-summary %}
Search a lead
{% endapi-method-summary %}

{% api-method-description %}
Run a full-text search on leads.
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
			"phones": [
				{
					"id": 3554076,
					"number": "+14501234567",
					"created_at": "2018-04-09T18:05:00+00:00",
			"updated_at": "2018-04-09T18:07:00+00:00"
				}
			],
			"created_at": "2018-04-09T18:05:00+00:00",
			"updated_at": "2018-04-09T18:07:00+00:00"
		}
		...
	],
	"links": {
		"first": "https://crm.activix.ca/api/v2/leads/search?page=1",
		"last": "https://crm.activix.ca/api/v2/leads/search?page=47",
		"prev": null,
		"next": "https://crm.activix.ca/api/v2/leads/search?page=2"
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

