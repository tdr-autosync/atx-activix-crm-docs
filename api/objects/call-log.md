# Call Log

The representation of a call log is called a `Call Log` object.  
Call Log are identified by a unique incremental ID.

A call log is used to store a call that occurred on an external system.

## The `Call Log` Object

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
      <td style="text-align:left">Unique identifier for the call log.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>communication_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="communication.md">communication</a> associated with the
        call log.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the call log was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the call log was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>start_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the call log was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>end_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the call log was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>duration</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">The duration of the call (in seconds).</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>direction</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Possible values are <b>outgoing </b>or <b>incoming</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>from</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The <b>from</b> phone number in <a href="https://www.twilio.com/docs/glossary/what-e164">E.164</a> format.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>to</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The <b>to</b> phone number in <a href="https://www.twilio.com/docs/glossary/what-e164">E.164</a> format.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>status</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The current status of the call. Possible value are <b>answered</b>, <b>attempted</b>, <b>calling</b>, <b>error</b>, <b>interrupted</b>, <b>pending </b>or <b>unanswered</b> (see
          below for more details).</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>media_url</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The web URL of the media file of the call. Possible file types are <b>wav</b> or <b>mp3</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>description</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">A description of the call log if any is provided.</td>
    </tr>
  </tbody>
</table>

## Possible `status` values

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

## Nested Objects

The `Call Log` object may have the following [nested objects](../nested-objects.md).

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `lead` | object | [​Lead object](lead.md) representing the associated lead. |

