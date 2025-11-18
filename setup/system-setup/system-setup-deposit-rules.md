# System Setup – Deposit Rules

### **Overview**

The Deposit Rules section in the System Setup module allows administrators to define and manage payment rules associated with bookings. These rules determine the amount and schedule of deposits, second payments, and final payments for bookings in the system. Each rule is tied to a specific booking date and can be enabled or disabled based on business requirements.

This feature ensures that payments are tracked correctly, helping to maintain cash flow, reduce booking cancellations, and provide clear guidelines for customer payments.

***

### **Purpose**

The purpose of Deposit Rules is to:

* Define the deposit amount (fixed value or percentage) required at the time of booking.
* Set the second payment value and due date if applicable.
* Control the timing of the final payment.
* Enable or disable rules based on current policies.
* Ensure consistent application of payment terms across bookings.

By using Deposit Rules, the finance team and booking agents can enforce payment schedules automatically, reducing errors and improving customer experience.

***

### **Field Descriptions**

<figure><img src="../../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

| Field                    | Description                                                                                                                                                                      |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Booking Date**         | The date for which this deposit rule is applicable. This typically corresponds to the booking creation or start date of a package.                                               |
| **Deposit Value**        | The fixed amount required as the first deposit at booking.                                                                                                                       |
| **Deposit Percentage**   | The percentage of the total booking cost required as a deposit. Used when deposits are calculated as a percentage instead of a fixed value.                                      |
| **Second Payment Value** | The amount required as the second payment, if applicable.                                                                                                                        |
| **Disabled**             | Indicates if the rule is currently active or inactive. A green check (✔) means active, while a red cross (✖) means disabled. Disabled rules will not be applied to new bookings. |
| **Deposit Due**          | The number of days after booking that the deposit must be paid.                                                                                                                  |
| **Second Payment Due**   | The number of days after booking that the second payment must be paid.                                                                                                           |
| **Last Payment Due**     | The number of days before the departure date that the last payment must be completed.                                                                                            |
| **Delete (Trash Icon)**  | Allows administrators to delete a specific deposit rule. Use this with caution, as deleted rules cannot be recovered.                                                            |

***

### **Instructions for Use**

1. Navigate to **System Setup → Deposit Rules**.
2. Review the list of existing deposit rules. Each rule shows its booking date, payment values, due dates, and status.
3. To **create a new deposit rule**, click the **Create** button in the top-right corner. Enter the following:
   * Booking Date
   * Deposit Value or Deposit Percentage
   * Second Payment Value (if applicable)
   * Payment due periods (Deposit, Second Payment, Last Payment)
   * Set the rule as active or disabled
4. To **edit an existing rule**, click the respective row or an "Edit" button if available (depending on system implementation).
5. To **delete a rule**, click the trash icon at the end of the row. Confirm deletion to remove it permanently.
6. Ensure all payment values and percentages are correct before saving. Incorrect rules can cause booking issues or payment discrepancies.
