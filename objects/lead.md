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
| `average_spending` | integer | The average spending per visit. |
| `be_back_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the latest be back date. |
| `birth_date` | string | [ISO date](https://en.wikipedia.org/wiki/ISO_8601) \(without time\) representing when the lead's birth date. |
| `business` | boolean | The client has a business. |
| `call_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the call date _\(for a phone up\)_. |
| `city` | string | City/District/Suburb/Town/Village of the lead. |
| `civility` | string | The social title of the lead. Possible values are **mr**, **ms**, **miss**, **dr**, **me**. |
| `code` | string | Revival code. |
| `country` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166-2) representing the country of the lead. |
| `created_method` | string | The method of creation of the lead. Possible values are **activix**, **auto\_renewal**, **cdk**, **ct\_wizard**, **ford\_direct**, **manual**, **manual\_import**, **n\_c\_i\_digital**, **niotext**, **phone\_system**, **porsche\_digital**, **scan**, **scraper**, **serti**. |
| `csi_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the planned csi date. |
| `delivered_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the vehicle delivered date. |
| `delivery_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the vehicle delivery date. |
| `division` | string | Division of the lead. Possible values are **new**, **used** or **service**. |
| `end_service_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end service date. |
| `first_name` | string | First name of the lead. |
| `gender` | integer | Single-digit [ISO code](https://en.wikipedia.org/wiki/ISO/IEC_5218) representing the gender of the lead. |
| `last_name` | string | Last name of the lead. |
| `last_presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the last presented date. |
| `locale` | string | Two-letter [ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) representing the locale \(language\) of the lead. |
| `loyalty` | boolean |  |
| `next_presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the next presented date. |
| `odometer_last_visit` | integer | The last mileage  |
| `open_work_order_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the service open work order date. |
| `planned_pick_up_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the service planned pick up date. |
| `postal_code` | string | Postal code of the lead. |
| `prepaid` | boolean | Client has paid for his vehicle service. |
| `presented_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was last updated. |
| `promised_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when promised date for the vehicle pick up. |
| `province` | string | Two letter [ISO code](https://en.wikipedia.org/wiki/ISO_3166) representing the State/Province of the lead. |
| `rating` | integer | Rating about the quality of the lead. |
| `reached_client` | boolean | The client is reached. |
| `refinanced_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was refinanced. |
| `repair_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was repaired. |
| `repair_order` | string | The repair order number. |
| `road_test_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the road test date. |
| `sale_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was sold. |
| `second_contact` | string | Optional second contact for the lead. May be a person or a business. |
| `second_contact_civility` | string | The social title of the second contact for the lead. Possible values are **mr**, **ms**, **miss**, **dr**, **me**. |
| `segment` | string | The lead segment. Possible values are **conquest**, **promo**, **notSold**, **service**, **loyalty**, **reminder**, **endWarranty**, **endLcap**, **endLnette**, **csi**, **noShow**, **other.** |
| `service_cleaning_car` | boolean | The vehicle has been cleaned for the service. |
| `service_interval_km` | integer | The vehicle service interval in km. Possible values are **1000**, **5000**, **6000**, **8000**, **12000**, **16000**, **18000**, **20000**, **24000**, **25000.** |
| `storage` | string | Information about where the vehicle is stored for the service. |
| `sex` | string | The client sex. Possible values are **M, F**. |
| `invoiced` | boolean | An invoice is created for the lead's vehicle services. |
| `source` | string | The source where the lead came from. |
| `status` | string | The lead status. Possible values are **duplicate**, **invalid** or **lost**. |
| `take_over_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the lead was taken over by a director. |
| `type` | string | The type of lead. Possible values are **email**, **phone**, **walk\_in**, **loyalty**, **renewal**, **sms**, **event** and **pre\_booking**. |
| `unsubscribe_all_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the "Do not disturb" date. |
| `unsubscribe_call_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe call date was set. |
| `unsubscribe_email_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe email date was set. |
| `unsubscribe_sms_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the unsubcribe sms date was set. |
| `work_order` | string | The work order for the vehicle service. |
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

