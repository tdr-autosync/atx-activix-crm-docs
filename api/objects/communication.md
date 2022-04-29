# Communication

The representation of a communication is called a `Communication` object.\
Communications are identified by a unique incremental ID.\
\
A communication can be added or updated based on an existing lead ID.

## The `Communication` Object

| **Attribute** | **Type** | **Description**                                                                                                                                                                              |
| ------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id`          | integer  | Unique identifier for the communication.                                                                                                                                                     |
| `lead_id`     | integer  | ID of the [lead](lead.md) associated with the communication.                                                                                                                                 |
| `user_id`     | integer  | ID of the [user](user.md) associated with the communication.                                                                                                                                 |
| `created_at`  | string   | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the communication was added to the Activix CRM (not editable). To set a creation date, see field \`executed\_at\`. |
| `updated_at`  | string   | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the communication was last updated.                                                                                |
| executed\_at  | string   | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the communication was actually conducted. This field is editable through the API.                                  |
|               |          |                                                                                                                                                                                              |
| `method`      | string   | <p>Possible values are <strong>phone</strong>, <strong>email</strong>, <strong>sms</strong> or <strong>video</strong>. <br><em>New values might be added in the future.</em></p>             |
| `type`        | string   | Possible values are **outgoing** or **incoming**.                                                                                                                                            |
| `description` | string   | The details of the communication.                                                                                                                                                            |

### Call attributes

Communications with the method `phone` may have these additional attributes:

| **Attribute**   | **Type** | **Description**                                                                                                                                                                                                                                                                                                                                |
| --------------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `call_duration` | integer  | The duration of the call (in seconds).                                                                                                                                                                                                                                                                                                         |
| `call_phone`    | string   | The customer's phone number in [E.164](https://www.twilio.com/docs/glossary/what-e164) format.                                                                                                                                                                                                                                                 |
| `call_status`   | string   | <p>The current status of the call. Possible value are <strong>answered</strong>, <strong>attempted</strong>, <strong>calling</strong>, <strong>error</strong>, <strong>interrupted</strong>, <strong>pending</strong> or <strong>unanswered</strong> (see below for more details).</p><p><em>New values might be added in the future.</em></p> |

### Email attributes

Communications with the method `email` may have these additional attributes:

| Attribute       | Type   | Description                                                                                               |
| --------------- | ------ | --------------------------------------------------------------------------------------------------------- |
| `email_subject` | string | <p>The subject of the email.</p><p><em>Can't be retrieved for privacy reasons.</em></p>                   |
| `email_body`    | string | <p>The body of the email.</p><p><em>Can't be retrieved for privacy reasons.</em></p>                      |
| `email_user`    | string | <p>The user's email address used in the email.</p><p><em>Can't be retrieved for privacy reasons.</em></p> |

### Video attributes

Communications with the method `video` may have these additional attributes:

| Attribute | Type   | Description                                                                         |
| --------- | ------ | ----------------------------------------------------------------------------------- |
| `url`     | string | <p>The URL of the video.</p><p><em>Can't be retrieved for privacy reasons.</em></p> |

## Possible `call_status` values

| Value         | Description                                                                                                                                                         |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `answered`    | The customer answered the call. This confirms that the call is completed.                                                                                           |
| `attempted`   | The user attempted to reach the customer, but he didn't answer.                                                                                                     |
| `calling`     | The user is currently talking with the customer.                                                                                                                    |
| `error`       | An error occurred while trying to call the customer. This is normally due to a server problem.                                                                      |
| `interrupted` | <p>The call was interrupted by the customer. This happens when a customer hangs up before the user can pick up.<br><em>Applicable for incoming calls only.</em></p> |
| `pending`     | <p>This is the default status when the call is first initiated using click-to-call.</p><p><em>Applicable for click-to-call only.</em></p>                           |
| `unanswered`  | <p>The call was not answered by any user.<br><em>Applicable for click-to-call only.</em></p>                                                                        |
