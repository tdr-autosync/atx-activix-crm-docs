# Auto-lead Data Format \(ADF\)

Activix CRM supports the Auto-lead Data Format industry standard to accept lead submissions from third-party services.

This type of submission is most often delivered via **email** with the ADF XML as the body of the email.

{% hint style="info" %}
[Contact us](https://www.activix.ca/en/contact-us) to get the email address at which to submit the lead.
{% endhint %}

## Format Definition

The official specifications for the format may be found [here](http://adfxml.info/adf_spec.pdf).

We added a few tags to add support for data that is not normally included in the format.  
You will find details about theses tags in the following tables.

#### Prospect information

List of custom parameters for the parent prospect tag \(in addition to the existing `status` parameter\).

<table>
  <thead>
    <tr>
      <th style="text-align:left">Tag</th>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Valid Values</th>
      <th style="text-align:left">Purpose</th>
      <th style="text-align:left">Updated</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>&lt;prospect&gt;</code>
      </td>
      <td style="text-align:left">*</td>
      <td style="text-align:left">*</td>
      <td style="text-align:left">*</td>
      <td style="text-align:left">*</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">type</td>
      <td style="text-align:left">
        <p><em>quote</em>
        </p>
        <p>order</p>
      </td>
      <td style="text-align:left">Type of request. Order requests are managed separately from quote requests.</td>
      <td
      style="text-align:left">May 2020</td>
    </tr>
  </tbody>
</table>

_\* See official specifications_

#### Finance information

List of custom tags for the finance sub-category that is part of the vehicle category.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Tag</th>
      <th style="text-align:left">Params</th>
      <th style="text-align:left">Valid Values</th>
      <th style="text-align:left">Purpose</th>
      <th style="text-align:left">Updated</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>&lt;term&gt;</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">Length of the finance agreement in months.</td>
      <td style="text-align:left">April 2020</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>&lt;rate&gt;</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">Annual percentage rate of the finance agreement.</td>
      <td style="text-align:left">April 2020</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>&lt;frequency&gt;</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><em>monthly</em>
          <br />semi-monthly
          <br />bi-weekly</p>
        <p>weekly</p>
      </td>
      <td style="text-align:left">Payment frequency of the finance agreement.</td>
      <td style="text-align:left">April 2020</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>&lt;mileageallowance&gt;</code>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">Allowable mileage for a one year period.</td>
      <td style="text-align:left">April 2020</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">units</td>
      <td style="text-align:left">
        <p><em>km</em>
        </p>
        <p>mi</p>
      </td>
      <td style="text-align:left">Unit for the allowable mileage.</td>
      <td style="text-align:left">April 2020</td>
    </tr>
  </tbody>
</table>

#### Provider information

List of custom tags for the provider category.

| Tag | Params | Valid Values | Purpose | Updated |
| :--- | :--- | :--- | :--- | :--- |
| `<form>` |  | free text | Name of the form that the lead filled to generate the request. | April 2018 |
| `<referrer>` |  | free text | Name of the website \(or service\) that referred the lead. E.g. Google | April 2020 |
| `<searchterm>` |  | free text | Exact word or set of words that the lead searched. | April 2020 |
| `<keyword>` |  | free text | Word or set of words that matched the searched term. | April 2020 |
| `<navigationhistory>` |  | free text | Navigation history of the lead across the website. | April 2020 |
| `<campaign>` |  | free text | Name of the ad campaign \(SEM\) that generated the lead. | Sept. 2020 |

## Example

This is an example that may help you better understand the format of the ADF standard.

```markup
<?xml version="1.0" encoding="utf-8"?>
<?adf version="1.0"?>
<adf>
    <prospect status="new" type="quote">
        <id sequence="1" source="Activix">12345</id>
        <requestdate>2020-04-28T15:30:20-05:00</requestdate>
        <vehicle interest="buy" status="new">
            <year>2020</year>
            <make>Volvo</make>
            <model>XC90</model>
            <vin>2GTEK19R7V1511644</vin>
            <stock>V12345</stock>
            <trim>R-Design</trim>
            <doors>5</doors>
            <bodystyle>SUV</bodystyle>
            <transmission>A</transmission>
            <odometer status="original" units="km">1500</odometer>
            <condition>excellent</condition>
            <colorcombination>
                <interiorcolor>Red</interiorcolor>
                <exteriorcolor>Black</exteriorcolor>
                <preference>1</preference>
            </colorcombination>
            <colorcombination>
                <interiorcolor>Black</interiorcolor>
                <exteriorcolor>Gray</exteriorcolor>
                <preference>2</preference>
            </colorcombination>
            <option>
                <optionname>Sport seats</optionname>
                <manufacturercode>F0823343</manufacturercode>
                <stock>33323</stock>
                <weighting>+50</weighting>
                <price type="msrp" currency="CAD">1460.99</price>
            </option>
            <price type="msrp" currency="CAD">59999.99</price>
            <pricecomments>Anniversary Edition</pricecomments>
            <finance>
                <method>finance</method>
                <amount type="downpayment" currency="CAD">10000</amount>
                <amount type="monthly" currency="CAD">425.25</amount>
                <term>24</term>
                <rate>3.9</rate>
                <frequency>bi-weekly</frequency>
                <mileageallowance units="km">20000</mileageallowance>
            </finance>
            <comments>Demo car</comments>
        </vehicle>
        <customer>
            <contact>
                <id sequence="1" source="Activix">12345</id>
                <name part="first">Test</name>
                <name part="last">Activix 2</name>
                <gender>2</gender>
                <birthday>2015-04-24</birthday>
                <locale>fr</locale>
                <email>test@activix.ca</email>
                <phone type="phone" time="day">+14382881008</phone>
                <phone type="phone" time="evening">+14382881008</phone>
                <phone type="cellphone" time="nopreference">+14382881008</phone>
                <address>
                    <street line="1"></street>
                    <street line="2"></street>
                    <city></city>
                    <regioncode>QC</regioncode>
                    <postalcode>J1B2N3</postalcode>
                    <country>CA</country>
                </address>
            </contact>
            <timeframe>
                <description>Changing car soon.</description>
                <earliestdate>2020-05-01T15:30:00-04:00</earliestdate>
            </timeframe>
            <comments>Can you deliver the car to my house?</comments>
        </customer>
        <vendor>
            <vendorname>ABC Motors</vendorname>
            <contact>
                <name part="first">Jane</name>
                <name part="last">Doe</name>
                <email>jane@abcmotors.com</email>
                <phone type="cellphone">+15144447859</phone>
            </contact>
        </vendor>
        <provider>
            <name>Activix</name>
            <service>ABC Motors' Website</service>
            <email>support@activix.ca</email>
            <phone type="phone" time="day">+18664306767</phone>
            <url>https://abcmotors.com/volvo/xc90</url>
            <form>Financing request</form>
            <referrer>Google</referrer>
            <campaign>Red Tag Sale</campaign>
            <searchterm>Volvo XC</searchterm>
            <keyword>Volvo Laval</keyword>
            <navigationhistory>
                04/28/2020 - 22:10:25 - https://abcmotors.com
                04/28/2020 - 22:11:03 - [Popup open] EMAILID_AvailabilityUsed
                04/28/2020 - 22:11:03 - [Popup close] EMAILID_AvailabilityUsed
                04/28/2020 - 22:11:03 - /new/xc90 MENU_clicked_URL
            </navigationhistory>
        </provider>
    </prospect>
</adf>
```

