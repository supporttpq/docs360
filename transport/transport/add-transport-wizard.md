# Add Transport Wizard

### **Overview**

The **Add Transport Wizard** page allows users to create and configure new transport routes between departure and arrival locations.\
It defines essential parameters such as travel duration, transport mode, cancellation conditions, and brand associations.\
This wizard simplifies the setup of transport connections used in travel packages and ensures accurate data integration for all brands.

#### **Purpose**

The purpose of the **Add Transport Wizard** is to:

* Create new transport entries used in tour packages or product configurations.
* Define how and when transport services operate.
* Assign the transport to one or multiple brands in the system.
* Manage essential details like dates, travel intervals, and availability.

This ensures consistent and accurate transport data across booking systems and external integrations.

***

#### **Field Description**

<figure><img src="../../.gitbook/assets/image (431).png" alt=""><figcaption></figcaption></figure>

| **Field**                    | **Description**                                                                                                                                                                      |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Code**\*                   | Unique identifier for the transport route (e.g., _FL1234_ or _BUS001_). Used to distinguish between different connections.                                                           |
| **Return**\*                 | Specifies the return route code.                                                                                                                                                     |
| **Departure**\*              | Defines the departure location for the transport route.                                                                                                                              |
| **Arrival**\*                | Defines the destination location for the transport route.                                                                                                                            |
| **Cancelation Condition**\*  | Selects the applicable cancellation rule for this transport                                                                                                                          |
| **Transport Mode**\*         | Defines the type of transport (e.g., _Flight_, _Bus_, _Train_).                                                                                                                      |
| **Travel Length Correction** | Used to adjust the calculated travel duration if needed                                                                                                                              |
| **Free Sell**                | Checkbox that, when enabled, allows selling without seat or space limitations.                                                                                                       |
| **Interval**                 | Defines how often this transport repeats (e.g., every 1 day, 7 days, etc.).                                                                                                          |
| **Date From**                | The start date from which the transport becomes available for sale.                                                                                                                  |
| **Date To**                  | The last date when this transport is available.                                                                                                                                      |
| **Days**\*                   | Indicates the number of days the transport takes. It is used for automatic fix quota generation.                                                                                     |
| **API Text**                 | Custom text used for external API connections or partner systems.                                                                                                                    |
| **Override Period**          | When enabled, this control is used for generating departure date using different interval than default period.                                                                       |
| **Brands**                   | Section for assigning the transport to one or more brands (e.g., _Tourpaq DK_, _Tourpaq Live_). Each brand can be set as _Assigned_ or _Not assigned_ depending on access and usage. |

> _Fields marked with an asterisk (_) are mandatory.\*

***

#### **Instructions**

**1. Creating a New Transport**

1. Go to **Add Transport Wizard** from the Transport Management module.
2. Fill in all mandatory fields (**Code**, **Return**, **Departure**, **Arrival**, **Cancellation Condition**, **Transport Mode**, and **Days**).
3. Adjust **Travel Length Correction** if the route duration differs from the calculated time.
4. Define **Date From** and **Date To** for the operational period.
5. Select **Interval** to define repeating patterns.
6. Assign relevant **Brands** at the bottom of the page.

***

**2. Optional Configurations**

* **Free Sell** → Check this box if there are no seat restrictions (useful for unlimited capacity transfers).
* **Override Period** → Use only if this transport should replace existing entries for the same period.
* **API Text** → Add any text required for integrations or automation.

***

**3. Saving the Transport**

After all details are filled in:

1. Review the information to ensure correctness.
2. Press **Save**.
3. The new transport entry will be created and visible in the Transport List.

***

#### **How to Use – Example**

To add a weekly bus connection between _Copenhagen_ and _Aarhus_:

1. Enter **Code:** _BUS1001_ and **Return:** _BUS1002_.
2. Select **Departure:** _Copenhagen_ and **Arrival:** _Aarhus_.
3. Choose **Transport Mode:** _Bus_ and **Cancelation Condition:** _Standard Policy_.
4. Set **Interval:** 1 (operates weekly).
5. Set **Date From:** _27-10-2025_ and **Date To:** _27-10-2026_.
6. Enter **Days:** 7.
7. Assign to brand **Tourpaq DK**.
8. Save the new transport.

***

#### **Tips**

💡 _Use meaningful codes (e.g., BUS101 or FLT202) to easily identify routes._\
💡 _Ensure “Return” transport is properly linked to maintain accurate round-trip offers._\
💡 _For seasonal routes, adjust “Date From” and “Date To” each year to avoid inactive entries._\
💡 _Always assign the transport to the correct brand(s) so it appears in the relevant product setup._
