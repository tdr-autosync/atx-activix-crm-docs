# Email

The representation of an email is called an `Email` object. Emails are identified by a unique incremental ID.

## The `Email` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the email. |
| `address` | string | The email address. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the email was created. |
| `lead_id` | integer | The lead id associated with the email _\(required on store\)_. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the email was last updated. |
| `valid` | boolean | Define if the email is valid \(_only returned value_\). |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

