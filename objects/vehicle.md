# Vehicle

The representation of a vehicle is called a `Vehicle` object. Vehicles are identified by a unique incremental ID.

## The `Vehicle` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the vehicle. |
| `lead_id` | integer | The lead id associated with the phone number \(_required on store_\). |
| `related_id` | integer | Related id from the supplier. Used to link vehicle from the supplier to Activix. |
| `verified_by` | object | [​​User object](https://docs.crm.activix.ca/objects/user) representing the associated user who verified the vehicle \(_can't update it_\). |
| `accessories` | integer | Amount of vehicle accessories \(_used for sold vehicle_\). |
| `actual_value` | integer | Actual value of the current vehicle. |
| `allowed_mileage` | string | Allowed mileage of the current vehicle. |
| `balance` | integer | Actual balance value of the current vehicle. |
| `wanted_budget_max` | integer | Budget maximum for the wanted vehicle. |
| `wanted_budget_min` | integer | Budget minimum for the wanted vehicle. |
| `category` | string | Vehicle category of the vehicle. Possible values are **motorcycle**, **snowmobile**, **watercraft**, **boat**, **atv**, **van**, **truck**, **trsuvuck**, **automotive**, **motorized**, **utility**, **caravan**, **trailer**. |
| `category_rv` | string | Recreative vehicle category of the vehicle. Possible values are **motorized\_a**, **motorized\_b**, **motorized\_c**, **travel\_trailer**, **fifth\_wheel**, **trailer\_park**, **tent\_trailer**. |
| `client_number` | string | Vehicle client number. |
| `color_exterior` | string | Exterior color of the vehicle. |
| `color_interior` | string | Interior color of the vehicle. |
| `comment` | string | Comment about the vehicle. |
| `condition` | string | Condition of the vehicle. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was created. |
| `end_contract_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end contract date of the current vehicle. |
| `end_warranty_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end warranty date of the current vehicle. |
| `engine` | string | Engine of the vehicle \(3.0L for exemple\). |
| `extended_warranty` | string | Comment about the extended warranty for the vehicle. |
| `payment_frequency` | string | Payment frequency for the vehicle. Possible values are **monthly**, **two\_weeks**, **weekly**, **one\_payment**. |
| `fuel` | string | Fuel for the vehicle. Possible values are **gasoline**, **diesel**. |
| `funding` | string | Funding type for the vehicle. |
| `cash_down` | integer | Initial cash down for the vehicle. |
| `wanted_length_max` | integer | Wanted length max for the wanted vehicle. |
| `wanted_length_min` | integer | Wanted length min for the wanted vehicle. |
| `make` | string | The make of the vehicle. |
| `mileage` | integer | Current odometer of the vehicle. |
| `modality` | string | Modality payment for the vehicle. Possible values are **financing**, **cash**, **leasing**. |
| `model` | string | The model of the vehicle. |
| `offer_number` | string | The offer number of the vehicle. |
| `option` | string | Comment about the options of the vehicle. |
| `order_number` | string | Order number of the vehicle. |
| `payment` | integer | Periodic payment for the vehicle. |
| `preparation` | integer | Amount for the vehicle preparation. |
| `price` | integer | The price for the vehicle. |
| `profit` | integer | The profit on the vehicle. |
| `purchase_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the purchase date of the vehicle. |
| `rate` | numeric | Funding rate for the financement or leasing. |
| `recall` | string | Comment if the vehicle has a recall from the manufacturing. |
| `recorded_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the recorded date of the vehicle. |
| `residual` | string | Residual value of the current vehicle. |
| `security_deposit` | integer | Initial security deposit for the vehicle. |
| `sleeping` | integer | Sleeping number for the vehicle. |
| `sold` | boolean | Determine if a vehicle is sold. |
| `sold_by` | string | Name of the saler. |
| `sold_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the sale date of the vehicle. |
| `stock` | string | The dealers's stock \# of the vehicle. |
| `stock_state` | string | The dealers's stock state of the vehicle. Possible values are **locate**, **notAvailable**, **order**, **stock**. |
| `tire` | boolean | Determine if the vehicle came/come with spare tires. |
| `trade_notes` | string | Comment about the trade. |
| `trade_type` | string | Trade type of the vehicle. Possible values are **retail**, **wholesale**, **recycled**, **lost**, **excluded**, **other**. |
| `transmission` | string | Transmission of the vehicle. Possbile values are **auto**, **manual**, **sequential**. |
| `trim` | string | The trim of the vehicle. |
| `type` | string | The type of the vehicle. Possible values are **wanted** or **exchange**. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was last updated. |
| `value` | integer | The current value of the vehicle. |
| `vin` | string | The VIN number of the vehicle. |
| `warranty` | string | The VIN number of the vehicle. |
| `weight` | string | Comment about the warranty for the vehicle. |
| `year` | string | Four-digit representing the year of the vehicle |
| `wanted_year_max` | string | Four-digit representing the max year of the wanted vehicle |
| `wanted_year_min` | string | Four-digit representing the min year of the wanted vehicle |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

