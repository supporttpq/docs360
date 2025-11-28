# Don't sent ticket option

### **Overview**

The **"Don't Send Ticket"** checkbox is a control feature on the **New Booking** page that allows users to temporarily suppress automatic **"Update booking"** emails when making changes to a booking.

***

### **Purpose**

* To prevent customers from receiving multiple notification emails during internal or batch changes.
* To allow agents to **control when communication is sent** after modifications.
* Useful for correcting details, adding extras, or testing changes without notifying the customer each time.

***

### **Preconditions**

* The booking must already be in **"OK" status** (confirmed).
* A change must be triggered on the booking, such as adding a product or modifying passenger details.
* The user must have **editing rights** on the booking.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (4).png" alt=""><figcaption></figcaption></figure>

### **Field Description**

| **Field**             | **Description**                                                                                                                                  |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Don't Send Ticket** | A checkbox that appears **after changes** to a booking already in OK status. If checked, **Update Booking** emails will not be sent upon saving. |

***

### **Behavior & Logic**

1. The checkbox **only appears** when a change is made to a booking in **OK status** (e.g., adding a product).
2. When enabled (checked), it **suppresses the “Update booking” email** that would normally be sent upon saving the booking.
3. If the checkbox is **not checked**, the update email **will be sent** automatically upon saving.
4. After the booking is saved and the changes are applied:
   * The checkbox **resets (disables automatically)**.
   * The user must re-check it **again** for each future change if they want to suppress further update emails.
5. This checkbox **does not affect flight change emails**, which are **always sent as normal**.

***

### **Instructions**

1. Go to a booking that is already in **OK status**.
2. Make a change (e.g., add a product, edit passenger info).
3. The **"Don't Send Ticket"** checkbox will now appear.
4. To prevent an update email from being sent:
   * Check the box **before saving**.
5. Click **Save** to apply the changes.
6. If you make additional changes later, **you must re-enable the checkbox** before saving again.

***

### **Use Case Example**

* You add a meal supplement to a confirmed booking and do **not** want the customer to be notified yet.
* You check the **"Don't Send Ticket"** box before clicking **Save**.
* No email is sent to the customer.
* Later, you adjust the passenger's address without enabling the checkbox. This time, the update email **will be sent**.
