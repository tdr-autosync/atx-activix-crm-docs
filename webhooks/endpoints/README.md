# Webhook Endpoints

## Requirements

For us to send data to an external web service over HTTP, we require the following:

* The provided URL must be secured using HTTPS.
* The requests must be authenticated \(see Authentication section below\).
* The web service must accept and return data in the JSON format.

## Authentication

For authentication purposes, Activix will provide you a secure key. Activix will use this key to generate a signature that will be included as the `X-Activix-Signature` header in the request.

To verify the webhook is originating from Activix CRM you need to:

* Encode the request body with the HMAC algorithm \(using the secure key and SHA256 digest mode\).
* Compare the resulting hexdigest to the signature.

The signature is for the exact content of the request body. Make sure that your processing code does not modify the body before checking the signature.

The body of the request is in UTF-8 JSON format.

