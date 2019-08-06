# Task

The representation of a task is called a `Task` object. Tasks are identified by a unique incremental ID.

## The `Task` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the task. |
| `lead_id` | integer | ID of the [lead](lead.md) associated with the task. |
| `owner_id` | integer | ID of the [owner](user.md) associated with the task. |
|  |  |  |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the task was created. |
| `date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the date of the task. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the task was last updated. |
|  |  |  |
| `completed` | boolean | Determine if the task is completed. |
| `description` | string | The description of the task. |
| `priority` | string | The priority of the task. Possible values are **normal**, **high**. |
| `title` | string | The title of the event. |
| `type` | string | The title of the event. Possible values are **call**, **email**, **sms**, **csi**. |

