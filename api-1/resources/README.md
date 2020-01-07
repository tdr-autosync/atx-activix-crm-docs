# Resources

All API access is executed over HTTPS using one of the URLs listed below. All data is sent and received as JSON \(except some ADF endpoints that receive XML\).

_**Note:** we only support the SSL protocol TLS 1.2 to ensure the best possible security._

## Base URL

All URLs in this section expect one of the following URLs as a base. All testing should be done using **only**  the "Development / Testing" URL.

#### Development / Testing

`https://api.dev.crm.activix.ca/v2`

#### Production

`https://api.crm.activix.ca/v2`

## Rate limiting

All API resources are rate limited at **200** requests **per minute**. If you make more than 200 requests in a minute, you will get an `HTTP 429` error.

{% hint style="info" %}
Contact us if you need to make more than 200 requests per minute.
{% endhint %}

