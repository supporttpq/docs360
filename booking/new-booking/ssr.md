# SSR - Special Service Requests for Airlines

### **Overview**

**SSR (Special Service Request) codes** are standardized codes used in communication with airlines to indicate specific services or requirements for a passenger. These can cover, for example, meal preferences, mobility assistance, medical needs, or special baggage (such as sports equipment).

***

### **Purpose**

* Ensure airlines are informed of passenger-specific needs in advance.
* Improve the traveller experience by fulfilling requests such as special meals or assistance at the airport.
* Comply with airline reporting standards and procedures for special requests.

***

### **Preconditions**

* The booking must include a transport component (for example, a flight).
* The associated **reporting type** for the selected transport must support SSR codes. If not, the SSR field will not offer code selection.

***

### **Instructions**

1. **Open the booking**
   * Go to the **Booking** module.
   * Open the booking where the SSR needs to be added or changed.
2. **Go to the SSR tab**
   * Click the **SSR** tab within the booking.
3. **Add or edit SSR codes**
   * Click **Edit** to start entering SSR codes.
   *   Select the appropriate SSR code from the **drop-down list**.

       > Example: _VGML_ (Vegetarian/Vegan Meal), _SPML_ (Special Meal), _AVIH_ (Animal in Hold), _SPORT_ (Sports equipment).
   * If the drop-down is empty or missing expected values, the reporting type may not allow SSR codes for that transport, or the codes are not configured.
4. **Save the changes**
   * When the correct code has been selected, click **Save** to apply the changes.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (7).png" alt=""><figcaption></figcaption></figure>

#### **Important Notes**

* **SSR codes are sent to the airline** as part of reporting lists – accuracy and relevance are critical.
* If multiple passengers require different SSR codes, they may need to be assigned individually, depending on your configuration.
* SSR availability and behaviour may vary by transport provider and system setup.

***

#### **Examples of SSR Codes**

| **Code** | **Meaning**                 |
| -------- | --------------------------- |
| VGML     | Vegetarian/Vegan meal       |
| SPML     | Special meal                |
| AVIH     | Animal in hold              |
| WCHR     | Wheelchair required         |
| SPORT    | Sports equipment as baggage |

***

### **FAQ**

#### **Do SSR codes automatically guarantee the requested service?**

No. SSR codes are **requests** sent to the airline. They indicate what the passenger needs, but final confirmation depends on the airline’s rules and availability. Always verify critical services (for example, medical assistance) directly with the airline if required by your procedures.

***

#### **Why is the SSR drop-down empty for my booking?**

Common reasons:

* The **reporting type** for the selected transport does not support SSR codes.
* SSR codes have not been configured for that transport/provider in your setup.

If you believe SSR should be available, contact your system administrator to check the configuration.

***

#### **Can I add more than one SSR code for the same passenger?**

This depends on your configuration and airline rules. Some setups allow multiple SSR codes per passenger (for example, one for a special meal and one for a wheelchair). If you cannot add additional codes, check internal guidelines or consult your administrator.

***

#### **Do SSR codes show on the customer’s ticket?**

Typically, SSR codes themselves are **not printed in a customer-friendly way** on the ticket. Use the **Comments** section in the booking if you need to add readable information for the customer, and rely on SSR only for communication with the airline.
