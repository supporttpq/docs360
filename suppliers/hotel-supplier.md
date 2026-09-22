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

#### 4. Configure hotel schedulers

The **Schedulers** tab configures the automated reports Tourpaq sends about a hotel supplier's bookings.

It has two sub-tabs: **Extra Schedulers**,and **Hotel Schedulers**, for the hotel's own recurring reports.

The steps below cover **Hotel Schedulers**.

1. Navigate to **Users → Suppliers**, open the hotel supplier, and go to the **Schedulers** tab.
2. Select the **Hotel Schedulers** sub-tab, then click **Add schedule**.
3. Set **Interval** to how often the report repeats: Daily, Weekly, Monthly, or Annually.
4. Set the trigger window: enter either **Bookings Made** or **Days After** (the two are mutually exclusive).
5. Set **Hour** to the time of day the schedule runs.
6. Choose the **Reporting** format to send.
7. Choose the delivery **Method**: Mail or FTP.
8. For Mail, enter the recipient **Email**. For FTP, select the FTP Syst**em.**
9. Enable **Empty List** if the report should still be sent when it has no rows.
10. Click the save icon at the start of the row.

The schedule appears in the **Hotel Schedulers** table and runs automatically from its next scheduled **Hour**.

Use the trash icon to delete a schedule, or the pencil icon to edit one; the **Resend** link resends the most recent report on demand, and **View** under **Schedulers** shows the delivery history for that row.

**Hotel Schedulers fields**

<figure><img src="../.gitbook/assets/hotel-schedulers-add-schedule (1).png" alt="A Hotel Schedulers row filled in with Interval Daily, Days After 1, Hour 14:56, Email reservations@elgreco-kreta.gr, Reporting Hotel Manifest CSV, and Method Mail, before saving"><figcaption></figcaption></figure>

_The Hotel Schedulers row for a new schedule, before saving._

| Field         | Description                                                                            | Notes                                                                                                 |
| ------------- | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Interval      | How often the report repeats.                                                          | Daily, Weekly, Monthly, or Annually.                                                                  |
| Bookings Made | Sends the report after a set number of bookings, instead of on a fixed number of days. | Mutually exclusive with Days After.                                                                   |
| Days After    | Sends the report a set number of days after a reference point.                         | Mutually exclusive with Bookings Made. Exact reference point not yet confirmed — see TO VERIFY below. |
| Hour          | The time of day the schedule runs.                                                     |                                                                                                       |
| Reporting     | The report format to generate, for example Hotel Manifest CSV.                         | Whether the available formats depend on the Hotel list tab is not yet confirmed                       |
| Method        | How the report is delivered: Mail or FTP.                                              |                                                                                                       |
| Email         | The recipient's email address for the report.                                          |                                                                                                       |

#### 5. General settings

* In the **General Tab**, define:
  * **Email:** For receiving supplier communications
  * **Reservation Department Emails:** Used for dynamic hotel confirmations
* Click **Update** to save all changes.

### Related pages

* [.](./ "mention")
* [users](../users/users/ "mention")
* [hotels](../hotel/hotels/ "mention")
