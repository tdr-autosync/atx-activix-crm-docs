# Lead

The representation of a lead is called a `Lead` object. Leads are identified by a unique incremental ID.

## The `Lead` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the lead. |
| `first_name` | string | First\_name of the lead. |
| `last_name` | string | Last name of the lead. |
| `civility` | string | The social title of the lead. Possible values are **`mr`**, **`ms`**, **`miss`**, **`dr`**, **`me`**. |
| `second_contact` | string | Optional second contact for the lead. May be a person or a business. |
| `second_contact_civility` | string | The social title of the second contact for the lead. Possible values are **`mr`**, **`ms`**, **`miss`**, **`dr`**, **`me`**. |
| `division` | string | Division of the lead. Possible values are **`new`**, **`used`** or **`service`**. |
| `type` | string | The type of lead. Possible values are **`email`**, **`phone`**, **`walk_in`**, **`loyalty`**, **`renewal`**, **`sms`**, **`event`** and **`pre_booking`**. |
| `source` | string | The source where the lead originally from. |
| `address_line1` | string | Address \(line 1\). |
| `address_line2` | string | Address \(line 2\). |
| `postal_code` | string | ZIP or postal code. |
| `city` | string | City/District/Suburb/Town/Village. |
| `province` | string | Two letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166) representing the State/Province of the lead. |
| `country` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166-2) representing the country of the lead. |
| `locale` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) representing the locale \(language\) of the lead. |
| `birth_date` | string | [ISO date](https://en.wikipedia.org/wiki/ISO_8601) representing the date of birth of the lead. |
| `gender` | integer | Single-digit [ISO code](https://en.wikipedia.org/wiki/ISO/IEC_5218) representing the gender of the lead. |
| `account` | object | [Account object](https://docs.crm.activix.ca/objects/account) representing the associated account. |
| `advisor` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated advisor. |
| `phones` | array | Array of [phone objects](https://docs.crm.activix.ca/objects/phone). |
| `emails` | array | Array of [email objects](https://docs.crm.activix.ca/objects/email). |
| `vehicles` | array | Array of [vehicle objects](https://docs.crm.activix.ca/objects/vehicle). |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

