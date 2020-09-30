# Task

The representation of a task is called a `Task` object. Tasks are identified by a unique incremental ID.

## The `Task` Object

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
      <td style="text-align:left">Unique identifier for the task.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lead_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="lead.md">lead</a> associated with the task.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>owner_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="user.md">owner</a> associated with the task.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>completed_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the task was completed.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the task was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the date of the task.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the task was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>completed</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the task is completed.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>description</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The description of the task.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>priority</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The priority of the task. Possible values are <b>normal </b>or <b>high</b>.</p>
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
        <p>The type of the event. Possible values are <b>call</b>, <b>email</b>, <b>sms</b> or <b>csi</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

## Nested Objects

The `Task` object may have the following [nested objects](../nested-objects.md).

| Attribute | Type | Description |
| :--- | :--- | :--- |
| lead | object | [Lead object](lead.md) representing the associated lead. |
| owner | object | [User object](user.md) representing the associated task owner. |

