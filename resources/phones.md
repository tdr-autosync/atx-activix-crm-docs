# Phones

The representation of a phone is called a `Phone` object. At the moment, you can only retrieve phones as part of other requests.

## The `Phone` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the phone. |
| `number` | string | Phone number in [E.164](https://www.twilio.com/docs/glossary/what-e164) format |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the phone was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the phone was last updated. |



