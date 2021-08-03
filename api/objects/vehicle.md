# Vehicle

The representation of a vehicle is called a `Vehicle` object.  
Vehicles are identified by a unique incremental ID.

## The `Vehicle` Object

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Attribute</b>
      </th>
      <th style="text-align:left"><b>Type</b>
      </th>
      <th style="text-align:left"><b>Description</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Unique identifier for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lead_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the lead associated with the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the vehicle was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>end_contract_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">&#x200B;&#x200B;&#x200B;ISO datetime</a> representing
        the end contract date of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>end_warranty_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">&#x200B;&#x200B;&#x200B;ISO datetime</a> representing
        the end warranty date of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>purchase_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">&#x200B;&#x200B;&#x200B;ISO datetime</a> representing
        the purchase date of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>recorded_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">&#x200B;&#x200B;&#x200B;ISO datetime</a> representing
        the recorded date of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sold_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">&#x200B;&#x200B;&#x200B;ISO datetime</a> representing
        the sale date of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the vehicle was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>accessories</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Dollar value of accessories sold.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>actual_value</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Dollar value of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>allowed_odometer</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Allowed odometer of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>balance</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Actual balance value of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>cash_down</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">The down payment for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>category</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Category of the vehicle. Possible values are <b>motorcycle</b>, <b>snowmobile</b>, <b>watercraft</b>, <b>boat</b>, <b>atv</b>, <b>van</b>, <b>truck</b>, <b>suv</b>, <b>automotive</b>, <b>motorized</b>, <b>utility</b>, <b>caravan</b>, <b>trailer</b>,<b> hybride</b> or<b> mechanical</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>category_rv</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>RV category of the vehicle. Possible values are <b>motorized_a</b>, <b>motorized_b</b>, <b>motorized_c</b>, <b>travel_trailer</b>, <b>fifth_wheel</b>, <b>trailer_park</b> or <b>tent_trailer</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>certified</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the vehicle is a certified pre-owned</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>client_number</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Vehicle client number.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>color_exterior</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Exterior color of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>color_interior</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Interior color of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>comment</code>
      </td>
      <td style="text-align:left">text</td>
      <td style="text-align:left">Comment about the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>condition</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Condition of the vehicle. Possible values are <b>rough</b>, <b>average</b>, <b>clean</b> or <b>extra_clean</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>engine</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Engine capacity of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>extended_warranty</code>
      </td>
      <td style="text-align:left">text</td>
      <td style="text-align:left">Comment about the extended warranty for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>fuel</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Fuel type used by the vehicle. Possible values are <b>gasoline </b>or <b>diesel</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>license_plate</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Vehicle license plate number.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>make</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The make of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>modality</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Modality payment for the vehicle. Possible values are <b>financing</b>, <b>cash</b> or <b>leasing</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>model</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The model of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>odometer</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Current odometer value the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>offer_number</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The offer number of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>option</code>
      </td>
      <td style="text-align:left">text</td>
      <td style="text-align:left">Options of the vehicle. May be formatted as you wish.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>order_number</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Order number of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>payment</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Periodic payment amount for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>payment_frequency</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Payment frequency for the vehicle. Possible values are <b>monthly</b>, <b>bi_monthly</b>, <b>two_weeks</b>, <b>weekly</b> or <b>one_payment</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>preparation</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Amount for the vehicle preparation.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>price</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">The price of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>profit</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">The profit on the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rate</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Funding rate for the financement or leasing.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>recall</code>
      </td>
      <td style="text-align:left">text</td>
      <td style="text-align:left">Comment if the vehicle has a recall from the manufacturing.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>residual</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Residual value of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>security_deposit</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">Initial security deposit for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sleeping</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Sleeping number for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sold</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if a vehicle is sold.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sold_by</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Name of the seller.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>stock</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The dealers&apos;s stock # of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>stock_state</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The dealers&apos;s stock state of the vehicle. Possible values are <b>locate</b>, <b>notAvailable</b>, <b>order</b> or <b>stock</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>term</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The term in months of the modality of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>tire</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Determine if the vehicle comes/came with spare tires.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>transmission</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Transmission of the vehicle. Possible values are <b>auto</b>, <b>manual</b> or <b>sequential</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>trim</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The trim of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The type of vehicle. Possible values are <b>wanted</b> or <b>exchange</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>value</code>
      </td>
      <td style="text-align:left">numeric</td>
      <td style="text-align:left">The current value of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>vin</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The VIN of the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>warranty</code>
      </td>
      <td style="text-align:left">text</td>
      <td style="text-align:left">Comment about the warranty for the vehicle.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>weight</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Weight of the vehicle. Possible values are <b>under_3000</b>, <b>between_3000_5000</b> or <b>over_5000</b>.</p>
        <p><em>New values might be added in the future.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>year</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Four-digit number representing the year of the vehicle</td>
    </tr>
  </tbody>
</table>

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

The `Vehicle` object may have the following [nested objects](../nested-objects.md).

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `verified_by` | object | [​​User object](user.md) representing the user who verified the vehicle. |

## Custom values

The `Vehicle` object may have custom values for specific use cases. The custom values are declared in a sub-object named `customs`.

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `amount_evaluation_value` | float | Evaluation value from calculator. |
| `appraiser` | string | Evaluation appraiser from calculator |

