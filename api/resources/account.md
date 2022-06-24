# Account

The following describes the available resources for the Account to which an API user belongs to.

{% swagger method="get" path="/account" baseUrl="https://api.crm.activix.ca/v2" summary="Retrieve an account" %}
{% swagger-description %}
The list of available `nested objects` for an account is available [here](../objects/account.md#nested-objects).


{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}
Bearer Token.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" type="string" required="true" %}
Should be 

`application/json`

.
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Accept" type="string" required="true" %}
Should be 

`application/json`

.
{% endswagger-parameter %}
{% endswagger %}

**Body Example**

```json
{
    "data": [
        {
            "id": 123,
            "created_at": "2015-05-29T19:42:58+00:00",
            "updated_at": "2022-03-31T12:51:59+00:00",
            "name": "Account name"
        }
    ]
}
```
