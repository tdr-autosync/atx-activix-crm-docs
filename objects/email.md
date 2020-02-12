# Email

The representation of an email is called an `Email` object. Emails are identified by a unique incremental ID.  Each `Lead` can only have one `Email` of each type.

## The `Email` Object

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
      <td style="text-align:left">Unique identifier for the email.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lead_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="lead.md#the-lead-object">lead</a> associated with the
        email.</td>
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
        when the email was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the email was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>address</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The email address</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The type of email. Possible values are <b>home</b> or <b>work</b>.</p>
        <p><em>New values might be added in the future</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>valid</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the email is valid <em>(read only)</em>.</td>
    </tr>
  </tbody>
</table>