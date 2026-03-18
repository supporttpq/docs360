# Passenger Information

### Overview

The **Passenger Information** section under a hotel in Tourpaq is used to configure mandatory or informative messages that are shown to customers during the booking flow.

These messages are typically destination specific and may contain legal requirements, local regulations, check in rules, or important operational notes. The configuration is controlled per hotel and can be limited by stay period, booking period, room type, and brand.

### Purpose

The Passenger Information module serves the following purposes:

* Inform customers about legal or destination specific requirements
* Display hotel specific conditions before booking confirmation
* Ensure compliance with local regulations
* Reduce post booking misunderstandings
* Force customer acknowledgement when required

Typical use cases:

* Tourist tax information
* Local registration requirements
* Special check in conditions
* Destination specific documentation requirements

### Fields Explanation

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This table displays all configured passenger information entries for the selected hotel and brand.

| Field                      | Description                                                                                                                                                        |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Stay From / Stay To**    | Defines the stay date range. The message applies only to passengers staying within this period.                                                                    |
| **Booking Date From / To** | Defines the booking creation date range. Only bookings created in this range will receive the message.                                                             |
| **Information**            | The message text that will be shown to passengers. Example: _“_&#x50;assenger information in Barcelon&#x61;_.”_                                                    |
| **Acknowledge**            | Indicates whether the passenger must acknowledge or confirm they have read the information. When enabled (✔), the system requires confirmation from the passenger. |
| **Room Type**              | <p>Defines whether the information applies to:</p><ul><li>All rooms</li><li>Specific room types</li></ul>                                                          |
| **Edit / Delete**          | Use the pencil icon ✏️ to edit or the trash icon 🗑️ to delete an entry.                                                                                           |

#### Buttons

| Button            | Action                                                                                                                          |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Create**        | Opens a form to add a new passenger information entry. You can define the date ranges, message, and acknowledgment requirement. |
| **Save / Update** | Saves changes to the selected brand and transport.                                                                              |

{% hint style="info" %}
### Passenger information allows overlapping periods

Ex: If fixed info is made for the entire season (01.05.26 - 31.08.26) - Reception closed at night, and another info is made for a short period (01.05.26 - 30.06.26) - Pool closed for May - June. Even if the periods overlapping, the system will allow and displayed both on the ticket.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Notes

* Passenger Information is hotel specific.
* Rules are controlled by both stay period and booking period.
* Incorrect configuration may result in missing legal information or unnecessary booking friction.
* Changes affect future bookings within defined booking date ranges.
