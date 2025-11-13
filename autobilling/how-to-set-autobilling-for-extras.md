# How to set autobilling for extras

### **Overview**

Autobilling for Extras automates the invoicing process for additional services such as golf, insurance, transfers, or any other extra linked to a booking.\
The configuration is managed directly on the **Extra General** page, under the **Automatic Billing** section. Once enabled, invoices are automatically generated and sent to the assigned creditor based on the defined billing schedule.

***

### **Purpose**

The purpose of the Extras Autobilling configuration is to:

* Ensure that all extra services are billed **automatically** and **independently** from hotel or transport invoices.
* Maintain **consistency and traceability** in supplier invoicing.
* Simplify the **export process** to the accounting system by aligning each extra with its creditor and accounting codes.

This setup allows financial teams to manage and control invoicing without manual intervention.

<figure><img src="../.gitbook/assets/image (20) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **How It Works**

When Autobilling is activated for an Extra:

1. The system uses the **selected creditor** and its **currency** to generate the invoice.
2. The **department and account codes** are included in the invoice lines if configured.
3. The billing frequency (daily, weekly, monthly, or days after service) determines when invoices are created.
4. If **autobilling is disabled**, the extra will instead be included in the **hotel’s invoice**.

Invoices are automatically exported and processed according to the same scheduling logic used for **hotel autobilling**.

***

### **Instructions**

#### **Access the Extra Configuration**

Navigate to:\
**Extras → Extra General → Automatic Billing section**

#### **Configure Autobilling Settings**

| **Field**                           | **Description**                                                                                                                                                                  |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Department Code**                 | Enter the department code to be displayed on the invoice.                                                                                                                        |
| **Account Debit / Account Deposit** | _(Optional)_ If filled, these fields will appear on the generated invoice and help with accounting allocation.                                                                   |
| **Creditor**                        | Select the creditor responsible for the extra. This is **mandatory** for autobilling to function. Once selected, the extra automatically uses the creditor’s currency.           |
| **Automatic Billing**               | _(Checkbox)_ Activate this option to enable autobilling for the extra.                                                                                                           |
| **Schedule**                        | Choose the frequency of invoice generation: **Daily**, **Weekly**, **Monthly**, or **Days After** (similar to hotel autobilling). You can also schedule invoices for past dates. |

#### **Save the Configuration**

Click **Save** to apply the autobilling settings.

***

### **Result**

If **Autobilling** is enabled:

* The extra will be invoiced **separately** according to the selected schedule.

If **Autobilling** is disabled:

* The extra will be **included in the hotel’s invoice** instead.

This ensures flexibility in how additional services are billed and supports both standalone and combined invoicing scenarios.
