# Phone

The representation of a phone is called a `Phone` object. Phones are identified by a unique incremental ID.

## The `Phone` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the phone. |
| `number` | string | Phone number in [E.164](https://www.twilio.com/docs/glossary/what-e164) format |
| `extension` | integer | The phone's extension. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the phone was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the phone was last updated. |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

