# Event

The representation of an event is called an `Event` object. Events are identified by a unique incremental ID.

## The `Event` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the event. |
| `lead_id` | integer | ID of the [lead](lead.md) associated with the event. |
| `owner_id` | integer | ID of the [owner](user.md) associated with the event. |
|  |  |  |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the event was created. |
| `end_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the event end date. |
| `start_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the event start date. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the event was last updated. |
|  |  |  |
| `canceled` | boolean | Determine if the event is canceled. |
| `completed` | boolean | Determine if the event is completed. |
| `confirmed` | boolean | Determine if the event is confirmed. |
| `description` | string | The description of the event. |
| `no_show` | boolean | Determine if the client didn't came. |
| `priority` | string | The priority of the event. Possible values are **normal**, **high**. |
| `title` | string | The title of the event. |
| `type` | string | The title of the event. Possible values are **appointment**, **phone\_appointment**, **delivery**, **other**. |



