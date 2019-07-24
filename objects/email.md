# Email

The representation of an email is called an `Email` object. Emails are identified by a unique incremental ID.

## The `Email` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the email. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the email was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the email was last updated. |
| `lead_id` | integer | ID of the lead associated with the email. |
| `address` | string | The email address. |
| `type` | boolean | The type of email. Possible values are **home** or **work**. |
| `valid` | boolean | Determines if the email is valid _\(read only\)_. |

