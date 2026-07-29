# Hotel supplier

### Overview

Suppliers in Tourpaq represent external service providers, typically hotels, who manage allotments and bookings through the system. To function correctly, each supplier requires an unassigned **Supplier user type**, which allows them to log in, manage offerings, and receive communications.

### How it works

#### 1. Create supplier user

1. Navigate to **Users → Users**.
2. Click **New User**.
3. Fill in the user details:
   * **Role:** Supplier
   * **Username**
   * **Password**
   * **First Name / Last Name**
   * **Seller ID**
   * **Associated Agencies**
4. Assign any **additional roles or permissions** required for the supplier.
5. Click **Save**.

<figure><img src="../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure>

#### 2. Create supplier record

1. Go to **Users → Suppliers**.
2. Click **Create New Supplier**.
3. Fill in:
   * **Supplier Name**
   * **User ID** (link to the user created in the previous step)
4. Click **Save**.
5. The supplier record is now active in the system.

#### 3. Assign hotels to supplier

1. Navigate to **Hotel List**.
2. Select hotels the supplier will manage.
3. Set **Schedulers** (these are the emails used for hotel communications).

<figure><img src="../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>

4.  In the **Handling Tab**, set:

    * **Creditor**
    * **Schedule**
    * **Account Debit**

    5\. Click **Save**.

    > Handling fees configured here will appear in the **Profit Tab** of bookings.

<figure><img src="../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure>

* Hotels assigned to the supplier will be displayed in the list to be assigned as having handling if required.

<figure><img src="../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

#### 4. General settings

* In the **General Tab**, define:
  * **Email:** For receiving supplier communications
  * **Reservation Department Emails:** Used for dynamic hotel confirmations
* Click **Update** to save all changes.
