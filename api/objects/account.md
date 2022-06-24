# Account

The representation of an account is called an `Account` object.\
Accounts are identified by a unique incremental ID.

An account may be a dealer or a group of dealers (related to other "sub" accounts).

## The `Account` Object

| **Attribute** | **Type** | **Description**                                                                                         |
| ------------- | -------- | ------------------------------------------------------------------------------------------------------- |
| `id`          | integer  | Unique identifier for the account.                                                                      |
|               |          |                                                                                                         |
| `created_at`  | string   | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the account was created.      |
| `updated_at`  | string   | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the account was last updated. |
|               |          |                                                                                                         |
| `name`        | string   | Name of the account.                                                                                    |

## Nested Objects

The `account` object may have the following nested objects.

|                 |       |                            |
| --------------- | ----- | -------------------------- |
| automations     | array | List of active automations |
| `custom_fields` | array | List of custom\_fields     |
| `users`         | array | List of active users       |
| sources         | array | List of sources            |
