# Vehicle

The representation of a vehicle is called a `Vehicle` object. Vehicles are identified by a unique incremental ID.

## The `Vehicle` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the vehicle. |
| `lead_id` | integer | ID of the lead associated with the vehicle. |
|  |  |  |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was created. |
| `end_contract_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end contract date of the vehicle. |
| `end_warranty_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end warranty date of the vehicle. |
| `purchase_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the purchase date of the vehicle. |
| `recorded_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the recorded date of the vehicle. |
| `sold_date` | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the sale date of the vehicle. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was last updated. |
|  |  |  |
| `accessories` | numeric | Dollar value of accessories sold. |
| `allowed_odometer` | string | Allowed odometer of the vehicle. |
| `balance` | numeric | Actual balance value of the vehicle. |
| `cash_down` | numeric | The down payment for the vehicle. |
| `category` | string | Category of the vehicle. Possible values are **motorcycle**, **snowmobile**, **watercraft**, **boat**, **atv**, **van**, **truck**, **suv**, **automotive**, **motorized**, **utility**, **caravan**, **trailer**, **hybride**, **mechanical**. |
| `category_rv` | string | RV category of the vehicle. Possible values are **motorized\_a**, **motorized\_b**, **motorized\_c**, **travel\_trailer**, **fifth\_wheel**, **trailer\_park**, **tent\_trailer**. |
| `client_number` | string | Vehicle client number. |
| `color_exterior` | string | Exterior color of the vehicle. |
| `color_interior` | string | Interior color of the vehicle. |
| `comment` | text | Comment about the vehicle. |
| `condition` | string | Condition of the vehicle. Possible values are **rough**, **average**, **clean**, **extra\_clean**. |
| `engine` | string | Engine capacity of the vehicle. |
| `extended_warranty` | text | Comment about the extended warranty for the vehicle. |
| `fuel` | string | Fuel type used by the vehicle. Possible values are **gasoline** and **diesel**. |
| `license_plate` | string | Vehicle license plate number. |
| `make` | string | The make of the vehicle. |
| `modality` | string | Modality payment for the vehicle. Possible values are **financing**, **cash**, **leasing**. |
| `model` | string | The model of the vehicle. |
| `odometer` | string | Current odometer value the vehicle. |
| `offer_number` | string | The offer number of the vehicle. |
| `option` | text | Options of the vehicle. May be formatted as you wish. |
| `order_number` | string | Order number of the vehicle. |
| `payment` | numeric | Periodic payment amount for the vehicle. |
| `payment_frequency` | string | Payment frequency for the vehicle. Possible values are **monthly**, **two\_weeks**, **weekly**, **one\_payment**. |
| `preparation` | numeric | Amount for the vehicle preparation. |
| `price` | numeric | The price of the vehicle. |
| `profit` | numeric | The profit on the vehicle. |
| `rate` | numeric | Funding rate for the financement or leasing. |
| `recall` | text | Comment if the vehicle has a recall from the manufacturing. |
| `residual` | numeric | Residual value of the vehicle. |
| `security_deposit` | numeric | Initial security deposit for the vehicle. |
| `sleeping` | integer | Sleeping number for the vehicle. |
| `sold` | boolean | Determine if a vehicle is sold. |
| `sold_by` | string | Name of the seller. |
| `stock` | string | The dealers's stock \# of the vehicle. |
| `stock_state` | string | The dealers's stock state of the vehicle. Possible values are **locate**, **notAvailable**, **order** or **stock**. |
| `term` | string | The term in months of the modality of the vehicle. |
| `tire` | boolean | Determine if the vehicle comes/came with spare tires. |
| `transmission` | string | Transmission of the vehicle. Possible values are **auto**, **manual**, **sequential**. |
| `trim` | string | The trim of the vehicle. |
| `type` | string | The type of vehicle. Possible values are **wanted**, **exchange**. |
| `value` | numeric | The current value of the vehicle. |
| `vin` | string | The VIN of the vehicle. |
| `warranty` | text | Comment about the warranty for the vehicle. |
| `weight` | string | Weight of the vehicle. Possible values are **under\_3000**, **between\_3000\_5000**, **over\_5000**. |
| `year` | integer | Four-digit number representing the year of the vehicle |

### Wanted vehicle attributes

Leads of type `wanted` may have these additional attributes.

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `budget_max` | numeric | Maximum budget for the vehicle. |
| `budget_min` | numeric | Minimum budget for the wanted vehicle. |
| `length_max` | integer | Maximum desired length in feet of the vehicle. |
| `length_min` | integer | Minimum desired length in feet of the vehicle \(_wanted vehicle only\)_. |
| `year_max` | integer | Four-digit number representing the maximum desired year of the vehicle. |
| `year_min` | integer | Four-digit number representing the minimum desired year of the vehicle. |



## Nested Objects

The `Vehicle` object may have the following [nested objects](../api-1/relations.md).

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `verified_by` | object | [​​User object](user.md) representing the user who verified the vehicle. |

