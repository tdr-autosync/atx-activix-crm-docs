# Lead

The representation of a lead is called a `Lead` object. Leads are identified by a unique incremental ID.

## The `Lead` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the lead. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `account_id` | integer | ID of the account associated with the lead. |
| `address_line1` | string | Address \(line 1\). |
| `address_line2` | string | Address \(line 2\). |
| `appointment_date` | string | [​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the appointment date. |
| `available_date` | string | ​​​[ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the wanted vehicle was available. |
| `be_back_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the latest be back date. |
| `birth_date` | string | [ISO date](https://en.wikipedia.org/wiki/ISO_8601) \(without time\) representing when the lead's birth date. |
| `call_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the call date _\(for a phone up\)_. |
| `city` | string | City/District/Suburb/Town/Village of the lead. |
| `civility` | string | The social title of the lead. Possible values are **mr**, **ms**, **miss**, **dr**, **me**. |
| `country` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166-2) representing the country of the lead. |
| `created_method` | string | The method of creation of the lead. Possible values are **activix**, **auto\_renewal**, **cdk**, **ct\_wizard**, **ford\_direct**, **manual**, **manual\_import**, **n\_c\_i\_digital**, **niotext**, **phone\_system**, **porsche\_digital**, **scan**, **scraper**, **serti**. |
| `csi_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the planned csi date. |
| `delivered_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the vehicle delivered date. |
| `delivery_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the vehicle delivery date. |
| `division` | string | Division of the lead. Possible values are **new**, **used** or **service**. |
| `first_name` | string | First name of the lead. |
| `gender` | integer | Single-digit [ISO code](https://en.wikipedia.org/wiki/ISO/IEC_5218) representing the gender of the lead. |
| `last_name` | string | Last name of the lead. |
| `locale` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) representing the locale \(language\) of the lead. |
| `postal_code` | string | Postal code of the lead. |
| `presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `province` | string | Two letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166) representing the State/Province of the lead. |
| `rating` | integer | Rating about the quality of the lead. |
| `refinanced_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was refinanced. |
| `road_test_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the road test date. |
| `sale_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was sold. |
| `second_contact` | string | Optional second contact for the lead. May be a person or a business. |
| `second_contact_civility` | string | The social title of the second contact for the lead. Possible values are **mr**, **ms**, **miss**, **dr**, **me**. |
| `sex` | string | The client sex. Possible values are **M, F**. |
| `source` | string | The source where the lead came from. |
| `status` | string | The lead status. Possible values are **duplicate**, **invalid** or **lost**. |
| `take_over_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was taken over by a director. |
| `type` | string | The type of lead. Possible values are **email**, **phone**, **walk\_in**, **loyalty**, **renewal**, **sms**, **event** and **pre\_booking**. |
| `unsubscribe_all_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the "Do not disturb" date. |
| `unsubscribe_call_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe call date was set. |
| `unsubscribe_email_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe email date was set. |
| `unsubscribe_sms_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe sms date was set. |
| `account` | object | [​Account object](https://docs.crm.activix.ca/objects/account) representing the associated account. |
| `advisor` | object | ​​[User object](https://docs.crm.activix.ca/objects/user) representing the associated advisor. |
| `bdc` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated BDC agent. |
| `commercial` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated F&I. |
| `service_advisor` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated service advisor. |
| `service_agent` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated service agent. |
| `emails` | array | Array of [email objects](https://docs.crm.activix.ca/objects/email). |
| `phones` | array | Array of [phone objects](https://docs.crm.activix.ca/objects/phone). |
| `vehicles` | array | Array of [vehicle objects](https://docs.crm.activix.ca/objects/vehicle). |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

