# Security measures

Starting with **version 3.7**, several new **security improvements** have been implemented to enhance user data protection and system integrity.

#### HTTPS Connection

All login operations are now secured using the **HTTPS protocol**, ensuring that all communication between the client and server is **encrypted** and protected from interception or tampering.

#### MD5 Encryption

User passwords are now stored in the database using **MD5 encryption**, providing an additional layer of security by preventing the storage of plain-text credentials.

#### Password Strength Validation

The **Edit User** and **Change Password** pages now include real-time password strength validation.\
When a user enters a new password, the system displays an indicator showing whether the password is:

* **Too short**
* **Weak**
* **Good**
* **Strong**

The system will only accept passwords rated as **Good** or **Strong**, ensuring better protection against unauthorized access.

<figure><img src=".gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>
