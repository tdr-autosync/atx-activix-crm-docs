# Authentication

The majority of our resources are protected using the common [OAuth 2](https://oauth.net/2/) standard.

You may request an API key by contacting [Activix](https://activix.ca/en/contact-us).

Your API key carry many privileges and cannot be recovered \(only new keys can be made\), so be sure to keep it secure! Do not share your secret API key publicly.

To authenticatie a request, you must include an `Authorization` header like so:

```http
Authorization: Bearer {your_key}
```

