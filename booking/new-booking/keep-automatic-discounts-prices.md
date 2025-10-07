# Keep automatic discounts prices

#### **Overview**

When editing a booking, the system can handle prices for discounts, extras, and travel insurance in two different ways:

* **Option 1**: Keep the prices that were used at the time of booking (default behavior).
* **Option 2**: Update the prices automatically based on current availability and rates.

The behavior is controlled by a setting in the **Back Office** interface via a checkbox.

***

#### **Keep Automatic Discount Prices Checkbox**

* Located on the **booking page** in the Back Office.
* Labeled: **Keep automatic discount prices**
* Determines how the booking engine treats pricing for:
  * Discounts/Supplements
  * Extras
  * Travel Insurance

***

#### **How It Works**

| Checkbox State  | System Behavior                                                                                                     |
| --------------- | ------------------------------------------------------------------------------------------------------------------- |
| ✅ **Checked**   | The original prices are retained for discounts, extras, and insurance, regardless of pricing updates in the system. |
| ⬜ **Unchecked** | Prices are refreshed and updated to the current system prices when booking details are modified.                    |

* The **initial state** of this checkbox is controlled by a **general company setting**, but it can be overridden on individual bookings.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (3).png" alt=""><figcaption></figcaption></figure>

#### **When the Setting&#x20;**_**Does Not Apply**_

In certain scenarios, prices will always be updated regardless of the checkbox state:

* When the **departure date** is changed
* When the **transport** is changed
* When the **hotel** is changed

These changes reset key elements of the booking and therefore require updated pricing.
