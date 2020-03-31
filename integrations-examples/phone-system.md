# Phone system

Activix CRM has an internal phone system used for our click-to-call and Phone Up features. The internal phone system may be replaced by an in-house phone system for better reliability and more flexibility.

We expect the phone system to integrate with Activix CRM's API to ensure the same quality of information in the CRM.

## Prerequisites

* The in-house system must be able to provide call information in **real time**.
* In order for the integration to be as seamless as possible, we recommend using Activix CRM's user ID in order to assign the communication to the correct user.

## Features

### Click-to-call \(outgoing\)

In order to integrate with the click-to-call feature, the in-house system must provide a REST API endpoint that will allow us to generate a call.

The system must update the CRM with the call information when the call ends.

{% file src="../.gitbook/assets/activix-api-outgoing-call-flow.pdf" caption="Outgoing call flow" %}



### Phone Up \(incoming\)

{% file src="../.gitbook/assets/activix-api-incoming-call-flow.pdf" caption="Incoming call flow" %}

