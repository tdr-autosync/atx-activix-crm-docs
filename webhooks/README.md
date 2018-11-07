# Webhooks

Activix CRM have many ways to send data to a third-party service. In this section, we'll explain how we can push data to a web service in real time.

## Requirements

For us to send data to an external web service over HTTP, we require the following:

* The provided URL must be secured using HTTPS.
* The requests must be authenticated \(see Authentication section below\).
* The web service must accept and return data in the JSON format.

## Authentication

Activix will provide you a secure key to secure the request send by Activix. When you will receive the request from Activix, you have to verify if the request really comes from Activix. You will receive a signature and it's referer to a hash\_mac encrypted in SHA-256 compound with the secure key and the body sent. You have to compare the signature sent with the signature that you generated with the body and the secure key to verify that the request comes from Activix and it is not altered.

## Exemple

_Secure key provide by Activix:_ `DkHmA6h9Z4HZVxugCwE2QCTiOKaBwBxgz6QHCuztUZFsqvPovfa4lkLs2FprQe4QNghSfIjd8CD  
wqLiIujanY9LcCDOLBuweQZ19cT7R3f4EvvUCIvXepmebIuVMAodzidqpKfxvGyVoWHSgspTlNv  
cjlvlIPMK0sFGOomeoVr7H91SYt4A2Qk8RG4SPLCWaBbWeI1ZWxOi6jcuBF3YukH40B7LsOfWy9  
dxMdtBWNszsOGChoXOSNxoevdAOdIMA`  
  
_Body from Activix:_  
 `{  
   
    "id": 465783,   
    "account_id": 44,   
    "first_name": "John",   
    "last_name": "Doe",   
    "lead_type": "web"  
}`   
  
Signature = _hash mac encrypted in SHA-256:_   
`8bbc079a4c323565f113de0e84d5433ba4b8a399cfd4a07a54d6c524f61aae35`

You will receive the signature in the header and the json lead object in the body.   
You have to compare the received signature with the signature generated from your side with the secure key provided and the body sent.

