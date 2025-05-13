# Edit Payment Rule

<figure><img src="../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

This page allows users to configure the payment schedule for travel bookings, including deposit and subsequent payment rules.

### **Sections Overview**

#### **1. Payment Rule Configuration**

| Field                    | Description                                                                                |
| ------------------------ | ------------------------------------------------------------------------------------------ |
| **Payment Rule Name**    | Name of the payment rule for easy identification (e.g., "2400,- deposittest").             |
| **Deposit Value**        | The fixed deposit amount to be collected (e.g., 24002).                                    |
| **Deposit Percentage**   | The deposit amount as a percentage of the total booking value (e.g., 2%).                  |
| **Second Payment Value** | Additional value for a second payment. This field is disabled if the checkbox is selected. |
| **Deposit Due**          | Number of days after booking when the deposit is due (e.g., 32 days).                      |
| **Second Payment Due**   | Number of days before departure when the second payment is due (e.g., 2 days).             |
| **Last Payment Due**     | Number of days before departure when the final payment is due (e.g., 602 days).            |

The user has the possibility to set different payment rules on a brand-specific basis. If a brand has no values set, the values from the Default tab will be used.&#x20;

<figure><img src="../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

#### **2. Exception Rules**

These rules override default payment behavior under specific conditions.

| Rule ID | Description                                                                                                                                       |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1.1** | If the second or rest of payment due date is earlier than booking date + deposit due, then adjust accordingly unless departure is within 14 days. |
| **1.2** | Adjusts payment dates based on booking and departure proximity (within 14 days or 3 days).                                                        |
| **1.3** | If departure is within 3 days of booking, payment due equals booking date.                                                                        |
| **2.1** | If second payment is due before the deposit, then second payment due = deposit due date.                                                          |
| **2.2** | If rest of payment due is earlier than the second payment, then rest of payment due = second payment due date.                                    |

#### **3. Payment Simulation**

This section allows users to simulate the configured payment rule and preview how payments will be scheduled based on booking and departure dates.

The payment rules may differ depending on the booking date and the departure date:

* Allow the configuration of multiple payment rule sets for transport services, each tied to specific booking and departure date ranges.
* Allow the configuration of multiple payment rule sets for individual brands, each based on distinct combinations of booking and departure dates.
