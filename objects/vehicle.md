# Vehicle

The representation of a vehicle is called a `Vehicle` object. Vehicles are identified by a unique incremental ID.

## The `Vehicle` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the vehicle. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was last updated. |
| `lead_id` | integer | ID of the lead associated with the vehicle. |
| `related_id` | integer | Related ID from the supplier. Used to link vehicle from the supplier with Activix CRM. |
| `accessories` | integer | Dollar value of accessories sold. |
| `allowed_odometer` | string | Allowed odometer of the vehicle. |
| `balance` | integer | Actual balance value of the vehicle. |
| `budget_max` | integer | Maximum budget for the vehicle _\(wanted vehicle only\)_. |
| `budget_min` | integer | Minimum budget for the wanted vehicle _\(wanted vehicle only\)_. |
| `cash_down` | integer | The down payment for the vehicle. |
| `category` | string | Category of the vehicle. Possible values are **motorcycle**, **snowmobile**, **watercraft**, **boat**, **atv**, **van**, **truck**, **trsuvuck**, **automotive**, **motorized**, **utility**, **caravan**, **trailer**. |
| `category_rv` | string | RV category of the vehicle. Possible values are **motorized\_a**, **motorized\_b**, **motorized\_c**, **travel\_trailer**, **fifth\_wheel**, **trailer\_park**, **tent\_trailer**. |
| `client_number` | string | Vehicle client number. |
| `color_exterior` | string | Exterior color of the vehicle. |
| `color_interior` | string | Interior color of the vehicle. |
| `comment` | string | Comment about the vehicle. |
| `condition` | string | Condition of the vehicle. Possible values are **rough**, **average**, **clean**, **extra\_clean**. |
| `end_contract_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end contract date of the vehicle. |
| `end_warranty_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end warranty date of the vehicle. |
| `engine` | string | Engine capacity of the vehicle. |
| `extended_warranty` | string | Comment about the extended warranty for the vehicle. |
| `fuel` | string | Fuel type used by the vehicle. Possible values are **gasoline**, **diesel**. |
| `length_max` | integer | Maximum desired length in feets of the vehicle _\(wanted vehicle only\)_. |
| `length_min` | integer | Minimum desired length in feets of the vehicle _\(wanted vehicle only\)_. |
| `license_plate` | string | Vehicle license plate. Max characters are 9. |
| `make` | string | The make of the vehicle. |
| `odometer` | string | Current odometer of the vehicle. |
| `modality` | string | Modality payment for the vehicle. Possible values are **financing**, **cash**, **leasing**. |
| `model` | string | The model of the vehicle. |
| `offer_number` | string | The offer number of the vehicle. |
| `option` | string | Comment about the options of the vehicle. |
| `order_number` | string | Order number of the vehicle. |
| `payment` | integer | Periodic payment for the vehicle. |
| `payment_frequency` | string | Payment frequency for the vehicle. Possible values are **monthly**, **two\_weeks**, **weekly**, **one\_payment**. |
| `preparation` | integer | Amount for the vehicle preparation. |
| `price` | integer | The price for the vehicle. |
| `profit` | integer | The profit on the vehicle. |
| `purchase_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the purchase date of the vehicle. |
| `rate` | numeric | Funding rate for the financement or leasing. |
| `recall` | string | Comment if the vehicle has a recall from the manufacturing. |
| `recorded_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the recorded date of the vehicle. |
| `residual` | string | Residual value of the vehicle. |
| `security_deposit` | integer | Initial security deposit for the vehicle. |
| `sleeping` | integer | Sleeping number for the vehicle. |
| `sold` | boolean | Determine if a vehicle is sold. |
| `sold_by` | string | Name of the seller. |
| `sold_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the sale date of the vehicle. |
| `stock` | string | The dealers's stock \# of the vehicle. |
| `stock_state` | string | The dealers's stock state of the vehicle. Possible values are **locate**, **notAvailable**, **order**, **stock**. |
| `term` | string | The term in months of the modality of the vehicle. |
| `tire` | boolean | Determine if the vehicle came/come with spare tires. |
| `transmission` | string | Transmission of the vehicle. Possbile values are **auto**, **manual**, **sequential**. |
| `trim` | string | The trim of the vehicle. |
| `type` | string | The type of the vehicle. Possible values are **wanted** or **exchange**. |
| `value` | integer | The current value of the vehicle. |
| `vin` | string | The VIN of the vehicle. |
| `warranty` | string | Comment about the warranty for the vehicle. |
| `weight` | string | Weight of the vehicle. |
| `year` | string | Four-digit representing the year of the vehicle |
| `year_max` | integer | Four-digit representing the maximum desired year of the vehicle _\(wanted vehicle only\)_. |
| `year_min` | integer | Four-digit representing the minimum desired year of the vehicle _\(wanted vehicle only\)_. |
| `verified_by` | object | [​​User object](https://docs.crm.activix.ca/objects/user) representing the user who verified the vehicle. |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

