# Password expiration

### **Overview / Purpose**

To improve security and comply with best practices, Tourpaq allows administrators to set a **password validity period** for users. Once enabled, users are required to change their password after a defined number of days, ensuring stronger account protection.

***

### **How It Works**

* Administrators can enable password validity settings per user.
* A **validity period** (number of days) is defined during configuration.
* The system tracks the password age and enforces changes when the set time expires.
* Notifications and redirects help guide the user through the renewal process.

***

### **Key Features / Functions**

* **Enable Password Validity**:
  * Go to **Edit User Page**
  * Check **“Enable password validity days”**
  * Enter the number of days (e.g., 30)
* **Automatic Tracking**:
  * The countdown starts from the moment the feature is enabled.
  * The countdown resets each time the user successfully changes their password.
* **User Alerts & Enforcement**:
  * System notifications are triggered based on days remaining until expiration.

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

### **Examples / Scenarios**

1. **Password expiration in more than 10 days**
   * No alerts are shown.
2. **Password expiration in less than 10 days**
   * The user receives an **alert after logging in** to remind them that their password is about to expire.

<figure><img src="../../.gitbook/assets/10_days-28e9f119cefa05cc22920bb8531e9fef.jpg" alt=""><figcaption></figcaption></figure>

3. **Password expiration in less than 3 days**
   * The user is **redirected to the Change Password page** after login and must update the password.

<figure><img src="../../.gitbook/assets/3_days-c28af95d0ce4d00aed320ee9a5569f7e.jpg" alt=""><figcaption></figcaption></figure>

4. **Password expired**

* The user sees an **expiration message at login**.
* The user must contact an **administrator** to reset the password before they can access the system again.

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>
