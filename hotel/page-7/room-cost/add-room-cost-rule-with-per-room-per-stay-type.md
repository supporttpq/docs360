# Add room cost rule with "Per Room Per Stay" type

### ✅ Overview

This page describes the **Hotel Room Cost Rule flow.** It explains each step a user must take to configure hotel costs, verify bookings, and ensure proper cost allocation and creditor integration.

The flow is used to define, apply, and validate **cost calculation rules** for hotel bookings — ensuring consistency across invoicing, profit margins, and multi-currency accounting.

***

### 🎯 Purpose

The purpose of this feature is to:

* Define how room costs are calculated for a hotel (per stay, per day, etc.)
* Ensure those costs are applied correctly to bookings
* Confirm the system calculates totals and currency conversions as expected
* Link hotel costs to creditors for accurate payment tracking

This process is essential for financial accuracy in the platform and prevents issues with supplier payouts and client billing.

***

### ⚙️ Preconditions

Before beginning this process:

* A hotel must already exist in the system.
* You must have permission to create and edit room cost rules.
* You should understand how bookings are structured in the system.
* Currency exchange rates should be available (for creditor validation).
* The user must have access to both the **Hotel module** and **Booking module**.

***

### 🧩 Step-by-Step Instructions & Field Descriptions

#### 1. **Access the Hotels Page**

* **Step**: Navigate to `Hotel → Hotels`.
* **Expected**: The hotel list is displayed.
* **Purpose**: Begin by selecting the hotel for which you'll define or validate cost rules.

***

#### 2. **Select a Hotel**

* **Step**: Choose a hotel from the list.
* **Expected**: The hotel detail page opens.
* **Tip**: Use filters to quickly find the hotel you need.

***

#### 3. **Go to Room Costs**

* **Step**: Click on **Room Costs** section.
* **Expected**: A list of room cost rules (if any) appears.

***

#### 4. **Create a New Rule**

* **Step**: Click **Create**.
* **Expected**: A blank row appears where new data can be entered.
* **Fields** to fill include:
  * **Stay Type** (e.g., Per Room Per Stay)
  * **Validity Period** (arrival date range)
  * **Cost** (amount)
  * **Currency** (local or creditor)
  * **Occupancy Conditions**

***

#### 5. **Set Stay Type to Per Room Per Stay**

* **Why it matters**: This rule type ignores the number of nights and calculates cost per stay.
* **Expected**: A field called **Stay Days No** becomes visible.

***

#### 6. **Create a Booking Matching the Rule**

* **Step**: Make a test booking using the selected room and date range.
* **Expected**: Booking is created and appears with status **OK**.

***

#### 7. **Check Booking Profit**

* **Step**: Click **Profit** in the booking.
* **Expected**: Booking margin and cost structure are shown.

***

#### 8. **Check Hotel Cost Breakdown**

* **Step**: Click **Hotel Cost**.
* **Expected**: Displays cost line items from the hotel rule.

***

#### 9. **Check Room Cost Row**

* **Expected**: If the rule is per stay, the system will divide cost by number of days internally for calculation purposes.

***

#### 10. **Verify Room Cost in Invoice Hotel Details Cost**

* **Step**: Look at the invoice preview section.
* **Expected**: Room cost value here should match the one defined in the hotel’s rule.

***

#### 11. **Check Invoice Total**

* **Step**: Scroll to total under **Invoice Hotel Details Cost**.
* **Expected**: Total reflects the rule-based cost.

***

#### 12. **Check Rule Details Popup**

* **Step**: Click **Details** on the Room Cost row.
* **Expected**: A popup appears showing the rule applied.
* **Validation**: Ensure rule matches the one entered in hotel config.

***

#### 13. **Return to Hotel Details**

* **Step**: Go back to the hotel’s main page.
* **Why**: To configure the creditor (payee) for the hotel.

***

#### 14. Select **a Creditor**

* **Step**: Select a creditor entity (organization that receives payment).
* **Expected**: Selected creditor appears in the input.

***

#### 15. **Save Changes**

* **Step**: Click **Save**.
* **Expected**: Hotel creditor is saved.

***

#### 16. **Return to Booking**

* **Step**: Open the previously created booking again.
* **Why**: To verify how the creditor affects cost display.

***

#### 17. **Re-check Profit**

* **Expected**: Profit page reloads with updated cost logic.

***

#### 18. **Re-check Hotel Cost**

* **Expected**: Costs now reflect **creditor’s currency** (if different).

***

#### 19–21. **Verify Room Cost with Currency Exchange**

* **Expected**:
  * Room Cost row shows converted cost.
  * Invoice section reflects cost in creditor's currency.
  * Totals include accurate currency-exchanged values.

***

#### 22. **Open Rule Details Again**

* **Purpose**: Confirm rule and cost are **identical** to original rule but shown in the creditor's currency now.

***

### 🔍 Summary of Key Concepts

| Concept               | Description                                                                |
| --------------------- | -------------------------------------------------------------------------- |
| **Room Cost Rule**    | Defines how much a room costs per stay, per day, or per person.            |
| **Stay Type**         | Determines cost calculation basis.                                         |
| **Creditor**          | The entity we pay for the hotel – may use different currency.              |
| **Invoice Details**   | Shows costs calculated and broken down for payment/billing.                |
| **Currency Handling** | Costs may be stored in local currency but invoiced in creditor’s currency. |

***

### 🛠️ Troubleshooting Tips

* If totals don’t match, double-check rule period and occupancy.
* If currency isn’t converted, confirm a creditor is assigned.
* If booking status isn’t OK, verify availability or data entry.
