# Vehicle

The representation of a vehicle is called a `Vehicle` object. Vehicles are identified by a unique incremental ID.

## The `Vehicle` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `id` | integer | Unique identifier for the vehicle. |
| `type` | string | The type of vehicle. Possible values are **`exchange`** and **`wanted`.** |
| `vin` | string | The VIN of the vehicle. |
| `stock` | string | The dealers's stock \# of the vehicle. |
| `make` | string | The make of the vehicle. |
| `model` | string | The model of the vehicle. |
| `year` | integer | Four-digit representing the year of the vehicle |
| `trim` | string | Trim of the vehicle. |
| `color_exterior` | string | Exterior color of the vehicle. |
| `color_interior` | string | Interior color of the vehicle. |
| `created_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was created. |
| `updated_at` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was last updated. |
|  |  |  |
| `id` | integer | Unique identifier for the vehicle. |
| `lead_id` | integer | The lead id associated with the phone number \(_required on store_\). |
| `related_id` | integer | Related id from the supplier. Used to link vehicle from the supplier to Activix. |
| `verified_by_id` | object | [​​User object](https://docs.crm.activix.ca/objects/user) representing the associated user who verified the vehicle \(_can't update it_\). |
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
| end\_contract\_date | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end contract date of the current vehicle. |
| end\_warranty\_date | string | [​​​ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end warranty date of the current vehicle. |
|  |  |  |

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}



