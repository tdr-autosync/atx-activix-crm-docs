# Communication

The representation of a communication is called a `Communication` object.  
Communications are identified by a unique incremental ID.  
  
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
| `method` | string | Possible values are **phone**, **email**, **sms** or **video**.  _New values might be added in the future._ |
| `type` | string | Possible values are **outgoing** or **incoming**. |

### Call attributes

Communications with the method `phone` may have these additional attributes:

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
      <td style="text-align:left">The customer&apos;s phone number in <a href="https://www.twilio.com/docs/glossary/what-e164">E.164</a> format.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_status</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The current status of the call. Possible value are <b>answered</b>, <b>attempted</b>, <b>calling</b>, <b>error</b>, <b>interrupted</b>, <b>pending </b>or <b>unanswered</b> (see
          below for more details).</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

### Email attributes

Communications with the method `email` may have these additional attributes:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>email_subject</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The subject of the email.</p>
        <p><em>Can&apos;t be retrieved for privacy reasons.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>email_body</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The body of the email.</p>
        <p><em>Can&apos;t be retrieved for privacy reasons.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>email_user</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The user&apos;s email address used in the email.</p>
        <p><em>Can&apos;t be retrieved for privacy reasons.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

### Video attributes

Communications with the method `video` may have these additional attributes:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>url</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The URL of the video.</p>
        <p><em>Can&apos;t be retrieved for privacy reasons.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Possible `call_status` values

<table>
  <thead>
    <tr>
      <th style="text-align:left">Value</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>answered</code>
      </td>
      <td style="text-align:left">The customer answered the call. This confirms that the call is completed.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>attempted</code>
      </td>
      <td style="text-align:left">The user attempted to reach the customer, but he didn&apos;t answer.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>calling</code>
      </td>
      <td style="text-align:left">The user is currently talking with the customer.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>error</code>
      </td>
      <td style="text-align:left">An error occurred while trying to call the customer. This is normally
        due to a server problem.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>interrupted</code>
      </td>
      <td style="text-align:left">The call was interrupted by the customer. This happens when a customer
        hangs up before the user can pick up.
        <br /><em>Applicable for incoming calls only.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>pending</code>
      </td>
      <td style="text-align:left">
        <p>This is the default status when the call is first initiated using click-to-call.</p>
        <p><em>Applicable for click-to-call only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unanswered</code>
      </td>
      <td style="text-align:left">The call was not answered by any user.
        <br /><em>Applicable for click-to-call only.</em>
      </td>
    </tr>
  </tbody>
</table>

