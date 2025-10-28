# Transport Payment Rules

### **Overview**

The **Transport Payment Rules** page allows administrators to define and manage payment structures for transport services such as flights, buses, or other transfers.\
Each rule determines how and when payments are collected for a booking — for example, through a deposit and a second (final) payment.

This configuration ensures flexibility across different brands, products, or transport types (e.g., charter vs. scheduled flights).

***

### **Purpose**

The purpose of this module is to:

* Set up transport-specific payment rules to control deposit and balance payment behavior.
* Define how much the customer needs to pay initially (deposit) and how much remains due at a later stage.
* Standardize payment policies across transport types or brands.

These rules are later linked to transport setups or booking configurations, ensuring that the correct payment schedule is automatically applied during booking.

***

### Table Structure

<figure><img src=".gitbook/assets/image (433).png" alt=""><figcaption></figcaption></figure>

| Column             | Description                                                                            |
| ------------------ | -------------------------------------------------------------------------------------- |
| **Payment Rule**   | The name or description of the rule, often indicating the client, carrier, or purpose. |
| **Deposit**        | The initial payment amount (typically in a specific currency like DKK or EUR).         |
| **Second Payment** | Any additional payment amount due at a later stage.                                    |
| 🗑️ (Delete Icon)  | Removes the payment rule permanently from the list.                                    |

### &#x20;**Buttons and Actions**

| Button     | Description                                                                                                                                 |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Create** | Opens a new form to define a transport payment rule. When creating a rule, specify a clear name, deposit amount, and second payment amount. |
| **Delete** | Removes a payment rule from the list. Rules currently used in active configurations should not be deleted.                                  |

### **Instructions**

1. Go to **Transport Payment Rules**.
2. Click **Create** to open a new payment rule form.
3. Enter:
   * **Payment Rule Name** – clear, descriptive name (e.g., “Charter 50/50 Rule”).
   * **Deposit** – amount or percentage collected at booking.
   * **Second Payment** – amount or percentage collected later.
   * **Deposit due** - Number of days before departure when the **first payment** required to confirm a booking.
   * Second payment due - Number of days before departure when the second payment is requierd.
   * Last payment due - Number of days before departure when the final payment must be done
4. Click **Save** to confirm.
5. The rule will appear in the overview list and can be selected when configuring transport definitions.

### **Exception rules**

1.1. If second payment due date / rest of payment due date < booking date + deposit due, then second payment due date / rest of payment due date = booking date + 2, except if departure date < booking date + 14

1.2. If departure date < booking date + 14, then second payment due date / rest of payment due date = booking date + 1, except if departure date < booking date + 3

1.3. If departure date < booking date + 3, then second payment due date / rest of payment due date = booking date

2.1. If second payment due date < deposit due date, then second payment due date = deposit due date

2.2. If rest of payment due date < second payment due date, then rest of payment due date = second payment due date

### Features

* **Create Rule Button -** Located in the top right, this button opens a form to create a new transport payment rule.
* **Sorted Columns -** Columns like _Deposit_ and _Second Payment_ can be sorted to easily identify highest/lowest values.
* Click on Payment Rule name  to view/edit the rule
