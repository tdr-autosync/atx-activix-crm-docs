# Phone

The representation of a phone is called a `Phone` object. Phones are identified by a unique incremental ID.

## The `Phone` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the phone. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the phone was created. |
| `extension` | integer | The phone's extension. |
| `lead_id` | integer | The lead id associated with the phone number _\(required_ on store_\)._ |
| `mobile` | boolean | Determine if the number is a mobile number. |
| `number` | string | Phone number in [E.164](https://www.twilio.com/docs/glossary/what-e164) format. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the phone was last updated. |
| `valid` | boolean | Determine if the number is a valid phone number \(_only returned value_\) |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

