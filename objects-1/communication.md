# Communication

The representation of a communication is called a `Communication` object.  Communications are identified by a unique incremental ID.  
  
A communication can be added or updated based on an existing lead ID.

## The `Communication` Object

| **Attribute** | **Type** | **Description** | Values may be added over time |
| :--- | :--- | :--- | :--- |
| `id` | integer | Unique identifier for the communication. |  |
| `lead_id` | integer | ID of the [lead](lead.md) associated with the communication. |  |
| `user_id` | integer | ID of the [user](user.md) associated with the communication. |  |
|  |  |  |  |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the communication was created. |  |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the communication was last updated. |  |
|  |  |  |  |
| `method` | string | Possible values are **phone**, **email, messenger** or **sms**. | Yes |
| `type` | string | Possible values are **outgoing** or **incoming**. |  |

### Call attributes

Communications with method `phone` may have these additional attributes.

| **Attribute** | **Type** | **Description** | Values may be added over time |
| :--- | :--- | :--- | :--- |
| `call_duration` | integer | The duration of the call \(in seconds\). |  |
| `call_phone` | string | The client's phone number in [E.164](https://www.twilio.com/docs/glossary/what-e164) format. |  |
| `call_status` | string | The current status of the call. Possible value are **answered**, **attempted**, **calling**, **error**, **interrupted**, **pending** or **unanswered** \(see below for more details\). | Yes |

### Possible `call_status` values

| Value | Description |
| :--- | :--- |
| `answered` | The client answered the call. This confirms that the call is completed. |
| `attempted` | The user attempted to reach the client, but he didn't answer. |
| `calling` | The user is currently talking with the client. |
| `error` | An error occurred while trying to call the client. This is normally due to a server problem. |
| `interrupted` | The call was interrupted by the client. This happens when a client hangs up before the user can pick up. Applicable for incoming calls only. |
| `pending` | This is the default status when the call is first initiated using click-to-call. |
| `unanswered` | The call was not answered by any user. Applicable for calls generated using click-to-call. |

