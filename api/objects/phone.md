# Phone

The representation of a phone is called a `Phone` object.  
Phones are identified by a unique incremental ID.

Each `Lead` can only have one `Phone` of each type.

## The `Phone` Object

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
      <td style="text-align:left">Unique identifier for the phone.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lead_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the lead associated with the phone.</td>
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
        when the phone was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the phone was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>extension</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Extension of the phone.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>number</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Phone number in <a href="https://www.twilio.com/docs/glossary/what-e164">E.164</a> format.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">
        <p>The type of phone. Possible values are <b>home</b>, <b>work</b> or <b>mobile</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>valid</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determines if the phone number is valid <em>(read only)</em>.</td>
    </tr>
  </tbody>
</table>

