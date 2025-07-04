# Communication Configuration – Transport Supplier

This guide explains how to configure the communication setup for a transport supplier in the system.

***

### 🔧 Accessing the Configuration Page

Navigate to:\
Transport **Supplier → \[Transport Supplier Name] → Communication tab**

***

### 📑 Field Descriptions

| Field                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Out/Home**                          | Select the direction of the transport communication: `Outbound` or `Homebound`.                                                                                                                                                                                                                                                                                                                                                                 |
| **Hour**                              | Set the scheduled hour (HH:MM) for communication dispatch.                                                                                                                                                                                                                                                                                                                                                                                      |
| **Reporting Type**                    | Choose the reporting format. Example: `Paxport`.                                                                                                                                                                                                                                                                                                                                                                                                |
| **Minutes B.D.**                      | Set the minutes before departure when the communication should be triggered.                                                                                                                                                                                                                                                                                                                                                                    |
| **Days B.D.**                         | Enter how many days before departure the email should be sent.                                                                                                                                                                                                                                                                                                                                                                                  |
| **Days B.D.To**                       | Enter the end of the interval how many days before departure to, the email shold be sent                                                                                                                                                                                                                                                                                                                                                        |
| **Minutes Interval**                  | Define the time gap between repeated messages (is active only if the DAYS B.D & DAYS B.D.TO is set).                                                                                                                                                                                                                                                                                                                                            |
| **Alternative**                       | Select an alternative reporting type                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Method**                            | Choose the method of communication (Email, FTP).                                                                                                                                                                                                                                                                                                                                                                                                |
| **Email**                             | Enter the recipient's email address.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Subject**                           | Define the subject line of the email.                                                                                                                                                                                                                                                                                                                                                                                                           |
| **FTP System**                        | If using FTP, select the appropriate FTP configuration/system. (is defined in System Setup FTP menu)                                                                                                                                                                                                                                                                                                                                            |
| **Use F.No**                          | Checkbox: Use flight number if enabled.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Stop Sale**                         | Checkbox: Mark if this triggers a Stop Sale action.                                                                                                                                                                                                                                                                                                                                                                                             |
| **ADL (Adding Deletion List for A7)** | <p>Checkbox: Enable ADL flag if needed. ADL reporting must is done whenever there are changes to a flight after the initial reporting is sent.</p><p>Example:</p><p>The full list is sent 08:00 4 days before departure</p><p>There is a last minute booking done 3 days before departure => ADL sent</p><p>There is a cancellation 2 days before departure => ADL sent</p><p>There is a name change 2 days before departure => ADL is sent</p> |
| **Resend**                            | Work only with ADL checkbox marked and offer the posibility to resend any ADl report for a specific date.                                                                                                                                                                                                                                                                                                                                       |
| **Comm. (View)**                      | Click `View` to see detailed communication reporting                                                                                                                                                                                                                                                                                                                                                                                            |

***

### ➕ Creating a New Communication Rule

1. Click the **Create** button in the top-right.
2. Fill in the required fields based on the transport and business rules.
3. Press **Save** to add the new communication setup.

***

### 🗑️ Deleting a Rule

Click the trash bin icon next to a rule to delete it. A confirmation prompt will appear.

***

***

### ✅ Best Practices

* Use clear and consistent **Subject** lines to distinguish communication types.
* Set up **Alternative methods** in case the main method fails.
* Use **Resend** to ensure delivery for critical messages.
* Periodically review and clean up outdated or unused rules.
