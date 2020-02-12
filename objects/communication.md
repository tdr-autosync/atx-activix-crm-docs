# Communication

The representation of a communication is called a `Communication` object.  Communications are identified by a unique incremental ID.  
  
A communication can be added or updated based on an existing lead ID.

## The `Communication` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the communication. |
| `lead_id` | integer | ID of the [lead](lead.md) associated with the communication. |
| `user_id` | integer | ID of the [user](user.md) associated with the communication. |
|  |  |  |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the communication was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the communication was last updated. |
|  |  |  |
| `method` | string | Possible values are **phone**, **email** or **sms**.  _New values might be added in the future_ |
| `type` | string | Possible values are **outgoing** or **incoming**. |

### Call attributes

Communications with method `phone` may have these additional attributes.

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Attribute</b>
      </th>
      <th style="text-align:left"><b>Type</b>
      </th>
      <th style="text-align:left"><b>Description</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>call_duration</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">The duration of the call (in seconds).</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_phone</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The client&apos;s phone number in <a href="https://www.twilio.com/docs/glossary/what-e164">E.164</a> format.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_status</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The current status of the call. Possible value are <b>answered</b>, <b>attempted</b>, <b>calling</b>, <b>error</b>, <b>interrupted</b>, <b>pending </b>or <b>unanswered</b> (see
          below for more details).</p>
        <p><em>New values might be added in the future</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>### Possible `call_status` values

| Value | Description |
| :--- | :--- |
| `answered` | The client answered the call. This confirms that the call is completed. |
| `attempted` | The user attempted to reach the client, but he didn't answer. |
| `calling` | The user is currently talking with the client. |
| `error` | An error occurred while trying to call the client. This is normally due to a server problem. |
| `interrupted` | The call was interrupted by the client. This happens when a client hangs up before the user can pick up. Applicable for incoming calls only. |
| `pending` | This is the default status when the call is first initiated using click-to-call. |
| `unanswered` | The call was not answered by any user. Applicable for calls generated using click-to-call. |

