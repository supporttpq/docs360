# Passengers informations

#### **Overview**

The _Passenger Information_ section is used to define informational notes or errata that apply to bookings for specific stay periods. These messages typically provide additional details for customers or internal staff (e.g., special conditions, restrictions, or exceptions).

#### **Purpose**

* To communicate relevant information related to bookings and stays (e.g., transport notes, exceptions, overlapping rules).
* To ensure passengers and staff are aware of important details connected to their travel.
* To manage conditions within specific booking and stay periods.

#### **Fields Explanation**

<figure><img src="../../.gitbook/assets/image (399).png" alt=""><figcaption></figcaption></figure>

#### **1. Stay From -** The start date of the hotel or travel stay period for which this information applies.

* **Usage**: Notes will only apply if the passenger’s stay begins on or after this date.
* **Example**: _29-10-2025_ → Information applies starting October 29, 2025.

#### **2. Stay To -** The end date of the hotel or travel stay period for which this information applies.

* **Usage**: Ensures the message is only relevant until this date.
* **Example**: _29-10-2025_ → Information is valid up to October 29, 2025.

#### **3. Booking Date From -** The earliest date when bookings must be made for the passenger's information to apply.

* **Usage**: Prevents the rule from applying to earlier bookings.
* **Example**: _04-06-2025_ → Only bookings made on or after June 4, 2025, are affected.

#### **4. Booking Date To -** The latest date when bookings can be made for the information to apply.

* **Usage**: Ensures the rule is limited to a certain booking period.
* **Example**: _04-06-2025_ → Only bookings made up to June 4, 2025, are affected.

#### **5. Information -** The actual message or note that will be displayed/associated with the booking.

* **Usage**: Describes transport notes, errata, or booking conditions.
* **Example values**:
  * _Transport test_ → internal test note.
  * _Transport errata def overlapping_ → indicates overlapping transport information.

#### **6. Acknowledge -** Indicates whether this information must be confirmed (acknowledged) by the user or system.

* **Values**:
  * ✅ (Enabled) → Acknowledgement required; ensures the message is seen.
  * ❌ (Disabled) → Acknowledgement not required.
*   **Example**:&#x20;

    <figure><img src="../../.gitbook/assets/image (400).png" alt=""><figcaption></figcaption></figure>

#### **Instructions for Use**

1. **Click “Create”** to define a new passenger information entry.
2. **Fill in stay and booking dates** to specify the valid period.
3. **Enter the information text** with clear and concise notes (e.g., transport conditions, exceptions).
4. **Enable or disable acknowledgment** depending on whether users must confirm having seen the information.
5. **Save** the configuration to apply it to the system.
6. **Edit (pencil)** to update or **delete (bin)** to remove an entry when it is no longer relevant.

{% hint style="info" %}
It won’t be possible to define 2 records for periods of time that overlap.
{% endhint %}
