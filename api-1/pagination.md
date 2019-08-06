# Pagination

Some top-level API resources have support for bulk fetches via "list" API methods. For instance, you can [list leads](resources/lead.md#list-all-leads) or [search leads](resources/search.md#search-leads). These list API methods share a common structure using the `page` and `per_page` parameters.

By default, these API methods return 25 results. You may change this behavior using the `per_page` parameter. You may use the `page` parameter to retrieve a specific page among the results.

The response will also contain a `links` and `meta` section that will help you navigate across the results.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Arguments</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>page</code>
      </td>
      <td style="text-align:left">
        <p>The current desired page of results to be returned.</p>
        <p>Defaults to 1.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>per_page</code>
      </td>
      <td style="text-align:left">
        <p>A limit on the number of objects to be returned, between 1 and 100.</p>
        <p>Defaults to 25.</p>
      </td>
    </tr>
  </tbody>
</table>| Response Sections |  |
| :--- | :--- |
| `data` | Collection of objects representing the result of the request. |
| `links` | Relevant links that you can directly use to navigate across pages. |
| `meta` | Key informations about the results. Fairly self-explanatory. |

#### Response Example

Here is an exemple of the different sections that would be returned from a request.

```javascript
{
    "data": [
        ...
    ],
    "links": {
        "first": "http://api.crm.activix.ca/v2/...&page=1",
        "last": "http://api.crm.activix.ca/v2/...&page=8",
        "prev": null,
        "next": "http://api.crm.activix.ca/v2/...&page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 8,
        "path": "http://api.crm.activix.ca/v2/...",
        "per_page": "25",
        "to": 25,
        "total": 197
    }
}
```

