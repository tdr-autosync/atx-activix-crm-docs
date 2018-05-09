# Vehicle

The representation of a vehicle is called a `Vehicle` object. Vehicles are identified by a unique incremental ID.

## The `Vehicle` Object

| **Attribute** | **Type** | **Description** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
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

{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}



