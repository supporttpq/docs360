# Service Case Settings

### **Overview**

The _Service Case_ settings section allows you to configure the email connection used by the system to fetch and manage service-case–related emails. These settings ensure that the system can access the designated mailbox, read incoming messages, and link them to service cases within the platform.

***

### **Purpose**

* To define the IMAP server and authentication details for the brand’s service case mailbox.
* To control the sender identity for outgoing communication.
* To ensure seamless retrieval and processing of support/service-related emails.

***

### **Instructions**

Fill in each field according to your company’s email configuration. All fields marked with **\*** are mandatory.\
After completing the fields, save the configuration to activate the connection.

***

### **Fields Description**

<figure><img src="../.gitbook/assets/image (500).png" alt=""><figcaption></figcaption></figure>

| **Field Name**          | **Description**                                                                                                                               |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Imap Server Name \*** | The IMAP server address used to retrieve incoming emails. Example: `imap.gmail.com`. Ensure this matches your email provider’s IMAP settings. |
| **From Name \***        | The display name shown to recipients when automated or service-case emails are sent from the system. Example: `Tourpaq DK`.                   |
| **Email Address \***    | The email account used for fetching service case messages. This is the mailbox the system will connect to via IMAP.                           |
| **Password \***         | The password for the email account. Required for authentication so the system can log into the mailbox.                                       |
