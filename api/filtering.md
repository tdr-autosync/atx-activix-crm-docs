# Filtering

Some API resources support filters to allow you to narrow the results base on specific parameters. In general, the more specific you can make the requests, the faster they are executed. Therefore, it is important to use filters whenever possible.

Filters are specified using the filter query parameter \(see [examples](filtering.md#examples) below\).

If you require more generalized parameter matching across multiple fields, see the [Search](resources/search.md) APIs.

Available filters vary based on the requested resources.  
Currently, we only support filters for the [List all leads](resources/lead.md#list-all-leads) resource.

{% hint style="info" %}
Values must use [percent-encoding](http://en.wikipedia.org/wiki/Percent-encoding) \(also known as URL encoding\).
{% endhint %}

## Operators

Some filters support operators. Operators are expressed as a nested array in the `filter` parameter.

* Greater than: `gt`
* Greater than or equal: `gte`
* Less than: `lt`
* Less than or equal: `lte`

## Wildcards

Some filters support the `%` wildcard. This wildcard matches any sequence of zero or more characters.

{% hint style="warning" %}
The use of wildcards may impact the performance of the request. We **strongly** suggest to only use wildcards at the end of the filter to make the request as fast as possible.
{% endhint %}

## Examples

_List all leads created between the 1st and 10th September 2019_

```text
/leads?filter[created_at][gte]=2019-09-01&filter[created][lte]=2019-09-10
```

_List all leads updated on September 15, 2019_

```text
/leads?filter[updated_at]=2019-09-15
```

