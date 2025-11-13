# How to set autobilling for handling

### **Overview**

Autobilling for Handling enables automatic generation of invoices related to handling services provided by suppliers.\
The configuration is managed within the supplier’s profile and determines whether handling charges are invoiced separately or included within the hotel’s invoice.

***

### **Purpose**

This setup ensures that handling costs are invoiced according to supplier agreements and accounting preferences.\
It provides flexibility to:

* Automatically bill handling services using their own schedule, or
* Combine handling charges with the hotel’s main invoice.

<figure><img src="../.gitbook/assets/image (22) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **How It Works**

When **Automatic Billing** is enabled in the supplier’s handling configuration, Tourpaq:

1. Uses the selected **creditor** to generate invoices.
2. Applies the configured **account debit** and **schedule** (daily, weekly, monthly, or days after).
3. Determines whether handling should be **invoiced separately** or **included in the hotel invoice** based on the _Add Own Schedule_ setting.

***

### **Instructions**

#### **Configure Handling Autobilling**

| **Step**                          | **Action**                                                                                                                                                                            |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Access Supplier Settings**   | Navigate to **Users → Suppliers** and select the desired supplier.                                                                                                                    |
| **2. Open Handling Section**      | Scroll to the **Handling** tab in the supplier profile.                                                                                                                               |
| **3. Select a Creditor**          | Choose the creditor to whom invoices for handling will be issued.                                                                                                                     |
| **4. Set Account Debit**          | Enter the account debit number to be displayed on the invoice.                                                                                                                        |
| **5. Define Schedule**            | Choose the billing frequency: **Daily**, **Weekly**, **Monthly**, or **Days After**.                                                                                                  |
| **6. Determine Invoice Behavior** | <p>- <strong>Add Own Schedule (Checked):</strong> Handling is invoiced separately.<br>- <strong>Add Own Schedule (Unchecked):</strong> Handling is included in the hotel invoice.</p> |
| **7. Save Configuration**         | Click **Save** to apply the autobilling settings.                                                                                                                                     |

<figure><img src="../.gitbook/assets/image (23) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Add a Handling Price**

| **Step**                        | **Action**                                                        |
| ------------------------------- | ----------------------------------------------------------------- |
| **1. Go to New Price**          | Open the **New Price** section for handling.                      |
| **2. Set Arrival Date**         | Define the date of arrival for which the handling price applies.  |
| **3. Define Booking Dates**     | Enter the applicable booking date range.                          |
| **4. Enter Price**              | Specify the handling price.                                       |
| **5. Set Age Range (Optional)** | Define **Start Age** and **End Age** if handling is age-specific. |
| **6. Save Price**               | Click **Save Price**, then **Save** to confirm.                   |

***

### **Result**

Once configured, the system automatically generates handling invoices according to the defined creditor, schedule, and billing behavior.\
This ensures accurate, timely, and supplier-specific handling invoicing within Tourpaq.
