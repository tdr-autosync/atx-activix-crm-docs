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

#### Provider information

List of custom tags for the provider category.

| Tag | Valid Values | Purpose |
| :--- | :--- | :--- |
| `<form>` | free text | Name of the form that the lead filled to generate the request. |
| `<referer>` | free text | Name of the website \(or service\) that referred the lead. E.g. Google |
| `<term>` | free text | Exact word or set of words that the lead searched. |
| `<keywork>` | free text | Word or set of words that matched the searched term. |
| `<navigationhistory>` | free text | Navigation history of the lead across the website |

## Example

This is an example that may help you better understand the format of the ADF standard.

```markup
<?xml version="1.0" encoding="utf-8"?>
<?adf version="1.0"?>
<adf>
    <prospect status="new">
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
            <price type="quote" currency="CAD">59999.99</price>
            <pricecomments>Anniversary Edition</pricecomments>
            <option>
                <optionname>Sport seats</optionname>
                <manufacturercode>F0823343</manufacturercode>
                <stock>33323</stock>
                <weighting>+50</weighting>
                <price type="msrp" currency="CAD">1460.99</price>
            </option>
            <finance>
                <method>finance</method>
                <amount type="downpayment" currency="CAD">10000</amount>
                <amount type="monthly" currency="CAD">850.25</amount>
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
            <referer>Google</referer>
            <term>Volvo XC</term>
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

