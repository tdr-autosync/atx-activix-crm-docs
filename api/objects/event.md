# Event

The representation of an event is called an `Event` object.  
Events are identified by a unique incremental ID.

## The `Event` Object

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
      <td style="text-align:left">Unique identifier for the event.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lead_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="lead.md">lead</a> associated with the event.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>owner_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="user.md">owner</a> associated with the event.</td>
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
        when the event was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>end_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the event end date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>start_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the event start date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the event was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>canceled</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the event is canceled.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>completed</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the event is completed.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>confirmed</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the event is confirmed.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>description</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The description of the event.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>no_show</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the client didn&apos;t came.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>priority</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The priority of the event. Possible values are <b>normal </b>or <b>high</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>title</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The title of the event.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The title of the event. Possible values are <b>appointment</b>, <b>phone_appointment</b>, <b>delivery </b>or <b>other</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

