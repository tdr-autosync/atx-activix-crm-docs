# Communication

The representation of a communication is called a `Communication` object.  Communications are identified by a unique incremental ID.  
  
A communication can be added or updated based on an existing lead ID.

## The `Communication` Object

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
      <td style="text-align:left"><code>id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Unique identifier for the communication.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the communication was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the communication was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lead_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="lead.md">lead</a> associated with the communication.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>user_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="user.md">user</a> associated with the communication.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>method</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Possible values are <b>phone</b>, <b>email</b>, <b>sms</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Possible values are <b>outgoing</b>, <b>incoming</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>email_subject</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The subject of the email.</p>
        <p><em>For <b>email</b> communications only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>email_body</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The body of the email.</p>
        <p><em>For <b>email</b> communications only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>email_client</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The client&apos;s email address.</p>
        <p><em>For <b>email</b> communications only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>email_user</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The user&apos;s email address.</p>
        <p><em>For <b>email</b> communications only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_duration</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">
        <p>The duration of the call (in seconds).</p>
        <p><em>For <b>phone</b> communications only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_phone</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The client&apos;s phone number in <a href="https://www.twilio.com/docs/glossary/what-e164">E.164</a> format.</p>
        <p><em>For <b>phone</b> communications only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_status</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The current status of the call. Possible value are <b>answered</b>, <b>attempted</b>, <b>calling</b>, <b>error</b>, <b>interrupted</b>, <b>pending</b>, <b>unanswered</b> (see
          below for more details).</p>
        <p><em>For <b>phone</b> communications only.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

### Possible `status` values

| Value | Description |
| :--- | :--- |
| `answered` | The client answered the call. This confirms that the call is completed. |
| `attempted` | The user attempted to reach the client, but he didn't answer. |
| `calling` | The user is currently talking with the client. |
| `error` | An error occurred while trying to call the client. This is normally due to a server problem. |
| `interrupted` | The call was interrupted by the client. This happens when a client hangs up before the user can pick up. Applicable for incoming calls only. |
| `pending` | This is the default status when the call is first initiated using click-to-call. |
| `unanswered` | The call was not answered by any user. Applicable for calls generated using click-to-call. |

