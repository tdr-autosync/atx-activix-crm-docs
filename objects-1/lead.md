# Lead

The representation of a lead is called a `Lead` object. Leads are identified by a unique incremental ID.

## The `Lead` Object

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
      <td style="text-align:left">Unique identifier for the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>account_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the <a href="account.md#the-account-object">account</a> associated
        with the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>customer_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">
        <p>This is currently only used to associate leads together.</p>
        <p><em>It is <code>null</code> if there is no associated leads.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>source_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the source associated with the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>appointment_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">&#x200B;ISO datetime</a> representing
        the appointment date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>available_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x200B;&#x200B;&#x200B;<a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the wanted vehicle is available.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>be_back_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the latest be back date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>birth_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO date</a> (without
        time) representing the lead&apos;s birth date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
          the call date.</p>
        <p><em>Usefull for <b>phone up</b> only.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>csi_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the planned CSI date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>delivered_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the vehicle delivered date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>delivery_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the vehicle delivery date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>paperwork_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the paperwork for the customer is completed.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>presented_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the customer visited the dealer.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>promised_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when promised date for the vehicle pick up.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>refinanced_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the vehicle was refinanced.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>road_test_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the road test date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sale_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was sold.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>take_over_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was taken over by a director.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unsubscribe_all_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the &quot;Do not disturb&quot; date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unsubscribe_call_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the unsubscribe call date was set.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unsubscribe_email_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the unsubscribe email date was set.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unsubscribe_sms_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the unsubscribe sms date was set.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>address_line1</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Address (line 1).</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>address_line2</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Address (line 2).</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>city</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">City of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>civility</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The social title of the lead. Possible values are <b>mr</b>, <b>ms</b>, <b>miss</b>, <b>dr</b>, <b>me</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>country</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Two-letter <a href="https://en.wikipedia.org/wiki/ISO_3166-2">ISO code</a> representing
        the country of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>created_method</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The method of creation of the lead. Possible values are <b>activix</b>, <b>auto_renewal</b>, <b>cdk</b>, <b>ct_wizard</b>, <b>ford_direct</b>, <b>manual</b>, <b>manual_import</b>, <b>n_c_i_digital</b>, <b>niotext</b>, <b>phone_system</b>, <b>porsche_digital</b>, <b>scan</b>, <b>scraper</b>, <b>serti</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>division</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Division of the lead. Possible values are <b>new</b>, <b>used</b>, <b>service</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>first_name</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">First name of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>gender</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Single-digit <a href="https://en.wikipedia.org/wiki/ISO/IEC_5218">ISO code</a> representing
        the gender of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>last_name</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Last name of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>locale</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Two-letter <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes">ISO code</a> representing
        the locale (language) of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>postal_code</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Postal code of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>province</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Two letter <a href="https://en.wikipedia.org/wiki/ISO_3166">ISO code</a> representing
        the State/Province of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rating</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Rating about the quality of the lead. Must be between 1-5.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>result</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The result of the lead. Possible values are <b>pending</b>, <b>attempted</b>, <b>reached</b>.
          A <code>null</code> value is considered <b>pending</b>.</p>
        <p><em>N.B. This value may be overridden by the result of a communication.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>second_contact</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Optional second contact for the lead. May be a person or a business.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>second_contact_civility</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The social title of the second contact for the lead. Possible values are <b>mr</b>, <b>ms</b>, <b>miss</b>, <b>dr</b>, <b>me</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>segment</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The lead segment. Possible values are <b>conquest</b>, <b>promo</b>, <b>notSold</b>, <b>service</b>, <b>loyalty</b>, <b>reminder</b>, <b>endWarranty</b>, <b>endLcap</b>, <b>endLnette</b>, <b>csi</b>, <b>noShow</b>, <b>other</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>source</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The source where the lead came from.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>status</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The lead status. Possible values are <b>duplicate</b>, <b>invalid</b> or <b>lost</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The type of lead. Possible values are <b>email</b>, <b>phone</b>, <b>walk_in</b>, <b>loyalty</b>, <b>renewal</b>, <b>sms</b>, <b>event</b> and <b>pre_booking</b>.</td>
    </tr>
  </tbody>
</table>### Service attributes

Leads of type `service` may have these additional attributes.

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `end_service_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing the end service date. |
| `last_visit_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the last visit date. |
| `next_visit_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the next visit date. |
| `open_work_order_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the service open work order date. |
| `planned_pick_up_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) presenting the service planned pick up date. |
| `repair_date` | string | [ISO datetime](https://en.wikipedia.org/wiki/ISO_8601) representing when the vehicle was repaired. |
|  |  |  |
| `average_spending` | integer | The average spending per visit. |
| `business` | boolean | Determine if the service is for a business. |
| `code` | string | Code from the dealer about the work on the vehicle. |
| `invoiced` | boolean | Determine if an invoice is created for the vehicle services. |
| `loyalty` | boolean | Determine if the loyalty program was presented. |
| `odometer_last_visit` | integer | The last vehicle mileage. |
| `prepaid` | boolean | Client has paid for his vehicle service. |
| `reached_client` | boolean | The lead has been reached. |
| `repair_order` | string | The repair order number. |
| `service_cleaned` | boolean | The vehicle has been cleaned for the service. |
| `service_interval_km` | integer | The vehicle service interval in km. Possible values are **1000**, **5000**, **6000**, **8000**, **12000**, **16000**, **18000**, **20000**, **24000**, **25000.** |
| `service_monthly_km` | integer | Kilometers allowed per month. |
| `storage` | string | Information about where the vehicle is stored for the service. |
| `work_order` | string | The work order number for the vehicle service. |



## Nested Objects

The `Lead` object may have the following [nested objects](../api-1/relations.md).

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
      <td style="text-align:left"><code>account</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="account.md">&#x200B;Account object</a> representing the associated
        account.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>advisor</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left">&#x200B;&#x200B;<a href="user.md">User object</a> representing the associated
        advisor.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>bdc</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="user.md">User object</a> representing the associated BDC agent.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>commercial</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="user.md">User object</a> representing the associated F&amp;I.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>service_advisor</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="user.md">User object</a> representing the associated service advisor.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>service_agent</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="user.md">User object</a> representing the associated service agent.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>emails</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="email.md">email objects</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>events</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="events.md">event objects</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>phones</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="phone.md">phone objects</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>products</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">
        <p>Array of <a href="product.md">product objects</a>.</p>
        <p><em>N.B. At this time, only service products are returned.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>tasks</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="tasks.md">task objects</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>vehicles</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="vehicle.md">vehicle objects</a>.</td>
    </tr>
  </tbody>
</table>