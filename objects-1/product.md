# Product

The representation of a product is called a `Product` object.

## The `Product` Object

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
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the product was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the product was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>category</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The category of the product.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>minutes</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">
        <p>Time representing the work duration.</p>
        <p><em>For <b>service</b> products only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>name</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Name of the product.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>notes</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Notes.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>premium</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if it is a premium product.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>price</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Price of the product.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sold</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the product is sold.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">The type of product. Possible values are <b>commercial</b>, <b>service</b>.</td>
    </tr>
  </tbody>
</table>