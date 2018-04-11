# Resources \(v2\)

All API access is over HTTPS using one of the URLs listed below. All data is sent and received as JSON \(except some ADF endpoints that receives XML\).

Blank fields are included as `null` instead of being omitted when sending response.

## Base URL

All URLs in this section expects one of the following URLs as a base. All testing should **only** be made using the "Development / Testing" URL.

### Development / Testing

`https://dev.crm.activix.ca/api/v2`

### Production

`https://crm.activix.ca/api/v2`

## Dates

Unless otherwise specified, all timestamps return in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.

```text
YYYY-MM-DDTHH:MM:SSZ
```

We use the UTC timezone for all timestamps.

