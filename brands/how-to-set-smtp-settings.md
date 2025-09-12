# How to set SMTP Settings

### **Overview / Purpose**

SMTP settings define how Tourpaq sends emails to customers. This includes booking confirmations, payment notifications, and other automated communications. Proper configuration ensures reliable email delivery and customer engagement.

***

### **How It Works**

* Tourpaq uses an **SMTP account** from a third-party provider to send emails.
* Administrators enter the provider’s account details into the system.
* Once configured, all outgoing emails are sent using this SMTP connection.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Key Features / Functions**

* **Server Address**: The SMTP server provided by your email provider (e.g., `smtp.gmail.com`).
* **Username**: The login username for the SMTP account.
* **Password**: The password associated with the SMTP account.
* **Port Number**: The port used to communicate with the SMTP server (commonly 587 or 465).
* **Save Settings**: Click **Save** to apply the configuration and enable email sending.

***

### **Examples / Scenarios**

1. Using a Gmail SMTP account:
   * Server: `smtp.gmail.com`
   * Port: `587`
   * Username/password: your Gmail credentials
   * Click **Save** → emails are now sent via Gmail.
2. Using a company email server:
   * Server: `mail.company.com`
   * Port: `465`
   * Username/password: corporate email credentials
   * Click **Save** → all customer notifications are sent through the company server.

***

### **Notes / Best Practices**

* Verify credentials and server details with your email provider before configuration.
* Test the SMTP connection after saving to ensure emails are delivered successfully.
* Consider using a dedicated email account for automated system emails to prevent conflicts.
* Keep your SMTP password secure and update it if the provider requires a reset.
