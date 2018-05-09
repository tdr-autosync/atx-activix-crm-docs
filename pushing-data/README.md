# Pushing Data

Activix CRM have many ways to send data to a third-party service. In this section, we'll explain how we can push data to a web service in real time.

## Requirements

For us to send data to an external web service over HTTP, we require the following:

* The provided URL must be secured using HTTPS.
* The requests must be authenticated \(see Authentication section below\).
* The web service must accept and return data in the JSON format.

## Authentication

We support two method of authentication ; [OAuth 2](https://oauth.net/2/) and [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication).



