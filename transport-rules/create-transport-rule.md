# Create Transport Rule

### Overview

The **Create Transport Rule** page allows you to define and configure transport rules that can be applied to bookings. A transport rule specifies validity dates, departure and arrival locations, transport types, pricing information, and additional settings that affect how the transport is handled in the booking workflow.

### Purpose

Transport rules are used to:

* Define available transport routes and validity periods.
* Configure pricing and payment rules for specific transports.
* Adjust check-in dates, hotel nights, and travel length based on transport details.
* Manage visibility, cancellation conditions, and filtering in the system.

### Field Explanation

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### General

* **Code**\* – Unique identifier for the transport rule (mandatory).
* **Date From**\* – Start date for the validity of the rule (mandatory).
* **Date To**\* – End date for the validity of the rule (mandatory).

Users can modify the selected dates after the initial save, as long as the transports have not yet been generated.\
This ensures flexibility during setup while still preserving data integrity once the generation process begins.

* **Departure**\* – Departure location (mandatory).
* **Arrival**\* – Arrival location (mandatory).
* **Stay Days\*** – Define stay duration (mandatory). The values displayed in this field are defined in Setup -> [Transport Stay Days](../setup/transport-stay-days.md).
* **Cancelation condition\*** - Select the cancellation condition that applies to this transport rule (mandatory).
* **Payment Rule** – Select a payment rule applicable to this transport.
* **Use change rule service** – If checked, activates the change rule service for this transport.

When a user clicks the **“+”** button to add new stay days, the system automatically preselects the first available stay day from the drop-down list.

This behavior allows users to repeatedly press **“+”** and quickly add all remaining stay days in sequence, creating a faster and more efficient workflow.

* **Allotment** – Configure allotment rules (optional, tab).

#### Transportation

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Pick-up point required** – If checked, the booking must include a pick-up point.
* **Travel Length Correction +/-** – Adjust the travel duration by a specified number of days.
* **Shift check-in date +/-** – Shifts the hotel check-in date forward or backward.
* **Hotel nights correction +/-** – Adjust the total number of hotel nights based on transport.
* **Transport mode** – Select the transport mode from the drop-down list.
*   **Alternative flight number** – Set the number of alternative flights for each transport set in the rule. The filter can be edited and takes effect after the transport has been generated.

    <figure><img src="../.gitbook/assets/image (623).png" alt=""><figcaption></figcaption></figure>

#### Price Information

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Infant price** – Defines the transport price that will be applied to passengers categorized as **infants**.
  * Currency follows the system or transport currency configuration.
  * The price is automatically copied to all transports generated from the rule.

**Overview**

The **Infant Price** field allows the user to define a fixed transport price for infants within a **Transport Rule**.\
This value is automatically applied to all transports generated from the rule.

The price is stored on the generated transport as an **infant price entry**, which defines the booking validity period and the departure validity period for the infant transport cost.

This ensures that infant transport pricing is consistently applied across all transports created from the rule.

**Purpose**

The purpose of the **Infant Price** setting is to automate infant transport pricing so that:

* every transport generated from a **Transport Rule** automatically receives the correct infant price
* pricing remains synchronized if the **Transport Rule** is later modified
* manual pricing adjustments on each transport are not required

This guarantees consistent pricing and reduces the risk of configuration errors.

**System Behavior**

**A. When a Transport Rule is created**

When a new **Transport Rule** is saved:

1. The system generates transports according to the configured rule.
2. The **Infant Price** defined in the rule is automatically added to each generated transport.

**B.** **When a Transport Rule is updated**

If the **Transport Rule** is updated, the system synchronizes the **Infant Price** across all transports generated from that rule.

The following updates are applied automatically:

* **Infant Price change**
  * If the **Infant Price** value is modified, the price is updated for all generated transports.
* **Date period change**
  * If **Date From** is modified, the **Departure From** value on the infant price of generated transports is updated.
  * If **Date To** is modified:
    * **Departure To** is updated
    * **Booking To** is updated.

**C. Extended date period**

* If the rule period is extended, newly generated transports will also receive the configured infant price.

{% hint style="info" %}
Important Notes

* The synchronization only applies to transports **generated from the Transport Rule**.
* Updating the rule ensures all related transports remain aligned with the latest pricing configuration.
{% endhint %}

When a transport is generated from a Transport Rule, the system creates a corresponding **infant price configuration** on the transport.

The dates from the Transport Rule are mapped to the infant price configuration as follows:

| Transport Rule      | Generated Transport Infant Price |
| ------------------- | -------------------------------- |
| Date From           | Departure From                   |
| Date To             | Departure To                     |
| Today (system date) | Booking From                     |
| Date To             | Booking To                       |

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This mapping ensures that the infant price is valid for the entire transport rule period.

If the **Infant Price** is removed from the **Transport Rule**, the system automatically deletes the **auto-generated Infant Price configuration** on the generated transport to keep it aligned with the rule configuration.

The **Infant Price** can be edited directly on a specific transport. However, any subsequent update made in the **Transport Rule** will override the value defined on the transport.

#### Outbound

* **Transport Type** – Select the transport type for the outbound journey (Real transport / External provider).
*   Depending on the selected transport type, the system offers several fields, such as:

    *   Real Transport

        <figure><img src="../.gitbook/assets/image (614).png" alt=""><figcaption></figcaption></figure>

        * Transport type - Specifies the type of transport to which the rule applies
        * Alternative airport - Defines whether alternative arrival airports are allowed.
        * Real Transport - Allows you to select a real transport.
    *   External Provider

        <figure><img src="../.gitbook/assets/image (615).png" alt=""><figcaption></figcaption></figure>

        * Transport type - Specifies the type of transport to which the rule applies
        * Alternative airport - Defines whether alternative arrival airports are allowed.
        * Provider - Specifies the transport provider (e.g., Paxport API, Travelport API, Amadeus API, Railhub Provider).
        * Max stops number - Defines the maximum number of stopovers allowed for the outbound journey.
        * Max connection time (min) - Specifies the maximum allowed connection time between segments, in minutes.
        * Max travel time (hours) - Defines the maximum total duration of the outbound journey.
        * Max Price - Sets the maximum allowed price for the outbound transport.
        * Baggage - Checkbox indicating whether baggage inclusion is required.



{% hint style="info" %}
Max stops number, Max connection time, Max travel time, Max price and Baggage field became editable only after the transports have been generated.
{% endhint %}

#### Homebound

* **Transport Type** – Select the transport type for the return journey (Real transport / External provider).

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

* The same fields are available as for outbound.

{% hint style="info" %}
Max stops number, Max connection time, Max travel time fields became editable only after the transports have been generated.
{% endhint %}

#### Settings

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Status** – Defines the rule’s visibility in the system (e.g., Visible / Hidden).
* **Hide as filter on lists** – If checked, this rule will not appear as a filter option in lists.
* **Cancelation condition\*** - Select the cancellation condition that applies to this transport rule (mandatory).
* **Payment Rule** – Select a payment rule applicable to this transport.
* **Use change rule service** – If checked, activates the change rule service for this transport.

### FAQ

#### Can I change **Date From** / **Date To** after saving?

Yes. You can edit the dates until transports have been generated.

#### Where do the **Stay Days** values come from?

They are maintained in Setup -> **Transport Stay Days**.

#### Why does clicking **“+”** in **Stay Days** preselect a value?

It speeds up setup. You can add stay days quickly in sequence.

#### What does **Pick-up point required** enforce?

It forces the booking flow to include a pick-up point.

#### Why can’t I find the rule in list filters?

Check **Status** and **Hide as filter on lists**.
