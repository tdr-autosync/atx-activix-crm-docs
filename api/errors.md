# Errors

Activix uses conventional HTTP response codes to indicate the success or failure of an API request. In general: Codes in the `2xx` range indicate success. Codes in the `4xx` range indicate an error that failed given the information provided \(e.g., a required parameter was omitted, a charge failed, etc.\). Codes in the `5xx` range indicate an error with Activix CRM's servers \(these are rare\).

## HTTP status code summary

| `200` | `OK` - Everything worked as expected. |
| :--- | :--- |
| `400` | `Bad Request` - The request was unacceptable, often due to malformed request syntax. |
| `401` | `Unauthorized` - No valid API key provided. |
| `403` | `Forbidden` - The provided API key does not have access to the resource. |
| `404` | `Not Found` - The requested resource doesn't exist. |
| `422` | `Unprocessable Entity` - One of the parameter is missing or invalid. |
| `429` | `Too Many Requests` - Too many requests hit the API too quickly. We recommend an exponential backoff of your requests. |
| `500, 502, 503, 504` | `Server Errors` - Something went wrong on Activix CRM's end. \(These are rare.\) |

