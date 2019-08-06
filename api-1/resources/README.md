# Resources

All API access is over HTTPS using one of the URLs listed below. All data is sent and received as JSON \(except some ADF endpoints that receives XML\).

_**Note:** we only support the SSL protocol TLS 1.2 to ensure the best possible security._

## Base URL

All URLs in this section expects one of the following URLs as a base. All testing should **only** be made using the "Development / Testing" URL.

#### Development / Testing

`https://api.dev.crm.activix.ca/v2`

#### Production

`https://api.crm.activix.ca/v2`

## Rate limiting

All API resources are rate limited at **200** requests **per minute**. If you make more than 200 requests in a minute, you will get back an `HTTP 429` error.

{% hint style="info" %}
Contact us if you need to make more than 200 requests per minute.
{% endhint %}

