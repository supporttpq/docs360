# How to set autobilling for discounts/supplements

### **Overview**

Autobilling for Discounts and Supplements automates the generation of invoices for additional charges or reductions applied to bookings.\
Each discount or supplement can be configured to bill independently according to its own schedule, ensuring accurate and transparent supplier invoicing.

***

### **Purpose**

The purpose of this configuration is to:

* Automate the invoicing process for discounts and supplements applied to bookings.
* Allow financial departments to track and reconcile these adjustments with suppliers efficiently.
* Maintain consistency with the same autobilling principles used for hotels and extras.

By enabling autobilling, the system ensures that every discount or supplement is invoiced automatically, according to its defined billing frequency.

<figure><img src="../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

### **How It Works**

When autobilling is activated for a **discount** or **supplement**, the system:

1. Uses the configured **creditor** to generate the invoice.
2. Applies the specified **department** and **account debit** codes to the invoice.
3. Follows the defined **billing schedule** (daily, weekly, monthly, or days after service).
4. Creates a **separate invoice** for each discount or supplement using its dedicated schedule.

If autobilling is **disabled**, no automatic invoices are generated, and the discount/supplement remains unbilled until manual processing.

***

### **Instructions**

#### **Access Configuration**

Navigate to:\
**Discounts / Supplements → Automatic Billing section**

#### **Configure Autobilling Settings**

| **Field**             | **Description**                                                                                                                                                                                                    |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Department Code**   | Enter the department code to be shown on the invoice.                                                                                                                                                              |
| **Account Debit**     | Specify the account debit number that should appear on the invoice.                                                                                                                                                |
| **Creditor**          | Select the creditor to whom the invoice will be issued. This field is mandatory for autobilling.                                                                                                                   |
| **Automatic Billing** | _(Checkbox)_ Activate this option to enable automatic invoicing for the discount or supplement.                                                                                                                    |
| **Schedule**          | Choose how often invoices are generated: **Daily**, **Weekly**, **Monthly**, or **Days After** (same as hotels and extras). Using a dedicated schedule ensures a separate invoice for this discount or supplement. |

#### **Save Configuration**

Click **Save** to apply and activate autobilling for the selected discount or supplement.

***

### **Result**

Once configured:

* The system automatically generates and sends invoices to the selected creditor according to the chosen schedule.
* Each discount or supplement is invoiced independently, ensuring accurate supplier settlements and financial transparency.
