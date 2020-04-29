# Account

The representation of an account is called an `Account` object.  
Accounts are identified by a unique incremental ID.

An account may be a dealer or a group of dealer \(related to other "sub" accounts\).

## The `Account` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the account. |
|  |  |  |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the account was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the account was last updated. |
|  |  |  |
| `name` | string | Name of the account. |

