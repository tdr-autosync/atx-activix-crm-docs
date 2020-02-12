# Authentication

The majority of our resources are protected using the common [OAuth 2](https://oauth.net/2/) standard.

You may request an API key by contacting the [Activix](https://www.activix.ca/en/contact-us) [Support](https://www.activix.ca/en/contact-us) team. 

Your API key provides many privileges. However, once it is generated it cannot be recovered if lost \(only new keys can be made\); be sure to keep it secure! Also, do not share your secret API key publicly.

To authenticate a request, you must include an `Authorization` header like so:

```http
Authorization: Bearer {your_key}
```

