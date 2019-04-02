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
      <td style="text-align:left"><code>created_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was created.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>updated_at</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was last updated.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>account_id</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">ID of the account associated with the lead.</td>
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
        when the wanted vehicle was available.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>average_spending</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">The average spending per visit.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>be_back_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the latest be back date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>birth_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO date</a> (without
        time) representing when the lead&apos;s birth date.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>business</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">The service is for a business.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>call_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the call date <em>(for a phone up)</em>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>city</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">City/District/Suburb/Town/Village of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>civility</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The social title of the lead. Possible values are <b>mr</b>, <b>ms</b>, <b>miss</b>, <b>dr </b>or <b>me</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>code</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Code from the dealer about the work on the vehicle.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
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
      <td style="text-align:left">The method of creation of the lead. Possible values are <b>activix</b>, <b>auto_renewal</b>, <b>cdk</b>, <b>ct_wizard</b>, <b>ford_direct</b>, <b>manual</b>, <b>manual_import</b>, <b>n_c_i_digital</b>, <b>niotext</b>, <b>phone_system</b>, <b>porsche_digital</b>, <b>scan</b>, <b>scraper</b> or <b>serti</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>csi_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the planned csi date.</td>
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
      <td style="text-align:left"><code>division</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Division of the lead. Possible values are <b>new</b>, <b>used</b> or <b>service</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>end_service_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        the end service date.</td>
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
      <td style="text-align:left"><code>last_visit_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> presenting
        the last visit date.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>locale</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Two-letter <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes">ISO code</a> representing
        the locale (language) of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>loyalty</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Presenting the loyalty program for service.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>next_visit_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> presenting
        the next visit date.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>odometer_last_visit</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">The last vehicle mileage.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>open_work_order_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> presenting
        the service open work order date.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>planned_pick_up_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> presenting
        the service planned pick up date.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>postal_code</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Postal code of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>prepaid</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">Client has paid for his vehicle service.</td>
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
      <td style="text-align:left">Rating about the quality of the lead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>reached_client</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">The lead has been reached.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>refinanced_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the vehicle was refinanced.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>repair_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the vehicle was repaired.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>repair_order</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The repair order number.
        <br />
        <br /><em>N.B. Only for service leads.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>result</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>The result of the lead. Possible values are <b>pending</b>, <b>attempted </b>or <b>reached</b>.
          A <code>null</code> value is considered <b>pending</b>.
          <br />
        </p>
        <p><em>N.B. This value may be overridden by the result of a communication.</em>
        </p>
      </td>
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
      <td style="text-align:left"><code>service_cleaned</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">The vehicle has been cleaned for the service.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>service_interval_km</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">The vehicle service interval in km. Possible values are <b>1000</b>, <b>5000</b>, <b>6000</b>, <b>8000</b>, <b>12000</b>, <b>16000</b>, <b>18000</b>, <b>20000</b>, <b>24000</b>, <b>25000.</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>service_monthly_km</code>
      </td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Kilometers allowed per month.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>storage</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Information about where the vehicle is stored for the service.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sex</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The client sex. Possible values are <b>M, F</b>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>invoiced</code>
      </td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">An invoice is created for the lead&apos;s vehicle services.</td>
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
      <td style="text-align:left"><code>take_over_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the lead was taken over by a director.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The type of lead. Possible values are <b>email</b>, <b>phone</b>, <b>walk_in</b>, <b>loyalty</b>, <b>renewal</b>, <b>sms</b>, <b>event</b> and <b>pre_booking</b>.</td>
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
        when the unsubcribe call date was set.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unsubscribe_email_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the unsubcribe email date was set.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unsubscribe_sms_date</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO datetime</a> representing
        when the unsubcribe sms date was set.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>work_order</code>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The work order number for the vehicle service.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>account</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="https://docs.crm.activix.ca/objects/account">&#x200B;Account object</a> representing
        the associated account.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>advisor</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left">&#x200B;&#x200B;<a href="https://docs.crm.activix.ca/objects/user">User object</a> representing
        the associated advisor.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>bdc</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="https://docs.crm.activix.ca/objects/user">User object</a> representing
        the associated BDC agent.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>commercial</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="https://docs.crm.activix.ca/objects/user">User object</a> representing
        the associated F&amp;I.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>service_advisor</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="https://docs.crm.activix.ca/objects/user">User object</a> representing
        the associated service advisor.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>service_agent</code>
      </td>
      <td style="text-align:left">object</td>
      <td style="text-align:left"><a href="https://docs.crm.activix.ca/objects/user">User object</a> representing
        the associated service agent.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>emails</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="https://docs.crm.activix.ca/objects/email">email objects</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>phones</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="https://docs.crm.activix.ca/objects/phone">phone objects</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>vehicles</code>
      </td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">Array of <a href="https://docs.crm.activix.ca/objects/vehicle">vehicle objects</a>.</td>
    </tr>
  </tbody>
</table>{% hint style="info" %}
You may request additional attributes by contacting [Activix](https://activix.ca/en/contact-us).
{% endhint %}

