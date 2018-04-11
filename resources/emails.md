# Emails

The representation of an email is called an `Email` object. At the moment, you can only retrieve emails as part of other requests.

## The `Email` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the email. |
| `address` | string | The email address. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the email was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the email was last updated. |

