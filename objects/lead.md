# Lead

The representation of a lead is called a `Lead` object. Leads are identified by a unique incremental ID.

## The `Lead` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- |
| `id` | integer | Unique identifier for the lead. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `address_line1` | string | Address \(line 1\). |
| `address_line2` | string | Address \(line 2\). |
| `appointment_date` | string | [​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the appointment date. |
| `appt_call_date` | string | [​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the appointment call date. |
| `appt_confirmation_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the appointment was confirmed. |
| `appt_validated` | bool | Determine if the appointment is validated by the user. |
| `available_date` | string | ​​​[ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the wanted vehicle was available. |
| `be_back_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `birth_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `call_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `called_count` | integer | Represents the number of call from the call center. |
| `city` | string | City/District/Suburb/Town/Village. |
| `civility` | string | The social title of the lead. Possible values are **mr**, **ms**, **miss**, **dr**, **me**. |
| `country` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166-2) representing the country of the lead. |
| `csi_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing planned csi date. |
| `delivered_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the vehicle delivered date. |
| `delivery_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the vehicle delivery date. |
| `division` | string | Division of the lead. Possible values are **new**, **used** or **service**. |
| `end_contract_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end contract date of the exchange vehicle. |
| `first_name` | string | First name of the lead. |
| `gender` | string | Single-digit [ISO code](https://en.wikipedia.org/wiki/ISO/IEC_5218) representing the gender of the lead. |
| `last_name` | string | Last name of the lead. |
| `last_presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `locale` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) representing the locale \(language\) of the lead. |
| `next_presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `odometer_last_visit` | integer | Vehicle odometer from the last visit. |
| `postal_code` | string | ZIP or postal code. |
| `presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `province` | string | Two letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166) representing the State/Province of the lead. |
| `rating` | integer | Lead rating about the quality. |
| `refinanced_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was refinanced. |
| `road_test_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the road test date. |
| `sale_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was sold. |
| `second_contact` | string | Optional second contact for the lead. May be a person or a business. |
| `second_contact_civility` | string | The social title of the second contact for the lead. Possible values are **mr**, **ms**, **miss**, **dr**, **me**. |
| `sex` | string | User sex of the lead. |
| `source` | string | The source where the lead originally from. |
| `status` | string | The lead status. Possible values are **duplicate**, **invalid** or **lost**. |
| `take_over_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `type` | string | The type of lead. Possible values are **email**, **phone**, **walk\_in**, **loyalty**, **renewal**, **sms**, **event** and **pre\_booking**. |
| `unsubscribe_all_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the "Do not disturb" date. |
| `unsubscribe_call_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe call date was set. |
| `unsubscribe_email_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe email date was set. |
| `unsubscribe_sms_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe sms date was set. |
| `walk_around` | bool | Represents the walk around vehicle from the advisor to the client. |
| `account` | object | [​Account object](https://docs.crm.activix.ca/objects/account) representing the associated account. |
| `advisor` | obejct | ​​[User object](https://docs.crm.activix.ca/objects/user) representing the associated advisor. |
| `bdc` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated BDC agend. |
| `commercial` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated account. |
| `creator` | object | [User object](https://docs.crm.activix.ca/objects/user) representing who created the lead. |
| `service_advisor` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated service advisor. |
| `service_agent` | object | [User object](https://docs.crm.activix.ca/objects/user) representing the associated service agent. |
| `emails` | array | Array of [email objects](https://docs.crm.activix.ca/objects/email). |
| `phones` | array | Array of [phone objects](https://docs.crm.activix.ca/objects/phone). |
| `vehicles` | array | Array of [vehicle objects](https://docs.crm.activix.ca/objects/vehicle). |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

