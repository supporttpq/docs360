---
description: >-
  Set up a hotel supplier in Tourpaq Office: link a Supplier user, choose its
  reports, schedule report delivery, and configure handling fees for its hotels.
---

# Hotel supplier

A hotel supplier is usually a hotel group or handling agent that receives booking reports from you and may charge a handling fee per booking. This page covers setting one up end to end.

#### Overview

A **hotel supplier** is a supplier record that represents an external hotel provider. It is linked to a user with the **Supplier** role, which lets the supplier log in to Tourpaq.

The supplier record has six tabs:

* **General** — name, address, contact details, and the linked user.
* **Emails** and **Customer Info** — see the TO VERIFY note under Field Reference.
* **Hotel list** — the report types available for this supplier.
* **Schedulers** — automated delivery of those reports by email or FTP.
* **Handling** — the handling fee, its creditor, and the hotels it applies to.

#### Purpose

Use a hotel supplier to:

* Give a hotel provider its own login to Tourpaq.
* Send the provider its booking reports automatically, on a schedule, by email or FTP.
* Charge a handling fee on bookings for selected hotels, shown in the booking's **Profit** tab.

#### Preconditions

* You have the user rights to create users and suppliers.
* The hotels the supplier will handle already exist — see Hotels.
* If you charge a handling fee, the creditor exists — see How to create a creditor.
* You know the supplier's report requirements: which reports, how often, and whether by email or FTP.
* For FTP delivery, the FTP system is already configured.

#### How-to

{% stepper %}
{% step %}
**Create the supplier user**

1. Go to **Users → Users** and click **New User**.
2. Set **Role** to `Supplier`.
3. Enter **Username**, **Password**, **First Name** and **Last Name**.
4. Enter **Seller ID** and select the **Associated Agencies**.
5. Add any further roles or permissions the supplier needs, then click **Save**.

The user now exists and can be linked to a supplier record. See Users.
{% endstep %}

{% step %}
**Create the supplier record**

1. Go to **Users → Suppliers** and click **Create**.
2. On the **General** tab, enter the **Name** and **Town**. Both are required.
3. In **User ID**, select the Supplier user from the previous step.
4. Under **Contacts**, enter **Fax2** (required) and the **Email** and **Reservation Depth Email** addresses.
5. Click **Update**.

The supplier appears in the list on Suppliers.

<figure><img src="../.gitbook/assets/23.09.2026_12.33.05_REC.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Choose the available reports**

1. Open the supplier and go to the **Hotel list** tab.
2. Select each report type the supplier should receive, such as **Rooming List** or **Hotel List PDF (EN)**.
3. Click **Save**.

<figure><img src="../.gitbook/assets/23.09.2026_12.35.13_REC.png" alt="" width="492"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Schedule report delivery**

1. Go to the **Schedulers** tab and select the **Hotel Schedulers** sub-tab.
2. Click **Add schedule**.
3. Set **Interval**, then enter either **Bookings Made** or **Days After**. Not both.
4. Set **Hour**, choose the **Reporting** format and choose the **Method**.
5. For `Mail`, enter the recipient **Email**. For `FTP`, select the **FTP System**.
6. Select **Empty List** if the report should be sent even when it has no rows.
7. Click the save icon at the start of the row.

The schedule appears in the **Hotel Schedulers** table and runs from its next scheduled **Hour**. To change it, click the pencil icon.
{% endstep %}

{% step %}
**Configure handling**

1. Go to the **Handling** tab and open the **Handling Options** sub-tab.
2. Select the **Creditor** and enter the **Account Debit**.
3. Select **Add Own Schedule** if required.
4. On the **Prices** sub-tab, click **Create** and enter the arrival and booking date ranges, the **Price**, and the age range it applies to.
5. On the **Hotels** sub-tab, select the hotels the handling fee applies to.
6. Click **Save**.

Handling fees appear in the **Profit** tab of matching bookings.
{% endstep %}
{% endstepper %}

The supplier can now log in, receives its scheduled reports, and handling fees apply to new bookings at the selected hotels.

#### Field Reference

**General tab**

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FnolFu1ggHPMz5sEKLULH%2Fimage.png?alt=media&#x26;token=0507d37c-ad04-4f93-8753-1c4ac471e68b" alt="The General tab of a supplier record, with address fields and User ID on the left and the Contacts panel on the right; Name, Town and Fax2 are marked required"><figcaption><p>The General tab of the supplier record.</p></figcaption></figure>

| Field                                             | Description                                                              |
| ------------------------------------------------- | ------------------------------------------------------------------------ |
| **Name**                                          | The supplier name shown in lists and reports.                            |
| **Address1**, **Address2**, **City**, **Country** | The supplier's postal address.                                           |
| **Town**                                          | The supplier's town.                                                     |
| **Status**                                        | Whether the supplier is shown in the supplier list.                      |
| **User ID**                                       | Links the supplier to its Supplier user login.                           |
| **Informative text on voucher on supplier**       | Text printed on vouchers for this supplier's services.                   |
| **Logo**                                          | The supplier logo.                                                       |
| **Phone1**, **Phone2**, **Fax1**                  | Contact numbers.                                                         |
| **Fax2**                                          | A second fax number.                                                     |
| **Latitude**, **Longitude**                       | The supplier's location.                                                 |
| **Email**                                         | The address for general supplier communications.                         |
| **Reservation Depth Email**                       | The reservation department address used for dynamic hotel confirmations. |
| **Link Address**                                  | A web address for the supplier.                                          |
| **Quest. Filter**                                 | TO VERIFY.                                                               |

**Hotel list tab**

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FTqnyyhdnMw8CFDwtVHnD%2Fimage.png?alt=media&#x26;token=abf62d93-918a-43dd-a6af-bd7bb7ececc1" alt="The Hotel list tab showing a checklist of report types, including Hotel List, Rooming List, Guide List and several PDF and XML variants, all selected"><figcaption><p>The Hotel list tab with every report type selected.</p></figcaption></figure>

| Field                  | Description                                                                                                               |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Report type checkboxes | Selects each report type for this supplier, for example **Rooming List**, **Transfer List (EN)** or **Changes List XML**. |

**Schedulers tab**

The **Schedulers** tab has two sub-tabs: **Extra Schedulers** and **Hotel Schedulers**. This page covers **Hotel Schedulers**. For **Extra Schedulers**, see Extra supplier.

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2F0noc3HyF5F56y3Sg4c9D%2Fhotel-schedulers-add-schedule.png?alt=media&#x26;token=c0a459ea-3d42-4d29-9f8b-c233465631e3" alt="A Hotel Schedulers row filled in with Interval Daily, Days After 1, Hour 14:56, a recipient email, Reporting Hotel Manifest CSV, and Method Mail, before saving"><figcaption><p>A new Hotel Schedulers row, before saving.</p></figcaption></figure>

| Field             | Description                                                      | Notes                                                                              |
| ----------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **Interval**      | How often the report repeats.                                    | `Daily`, `Weekly`, `Monthly` or `Annually`.                                        |
| **Bookings Made** | Sends the report once a set number of bookings is reached.       | You cannot use it together with **Days After**.                                    |
| **Days After**    | Sends the report a set number of days after a reference point.   | You cannot use it together with **Bookings Made**. TO VERIFY: the reference point. |
| **Hour**          | The time of day the schedule runs.                               | .                                                                                  |
| **Reporting**     | The report format to generate, for example `Hotel Manifest CSV`. |                                                                                    |
| **Method**        | How the report is delivered.                                     | `Mail` or `FTP`.                                                                   |
| **Email**         | The recipient address.                                           |                                                                                    |
| **FTP System**    | The FTP destination.                                             |                                                                                    |
| **Empty List**    | Sends the report even when it has no rows.                       |                                                                                    |
| **Resend**        | Sends the most recent report again, straight away.               |                                                                                    |
| **View**          | Shows the delivery history for the row.                          |                                                                                    |

{% hint style="warning" %}
The trash icon deletes a schedule, and **Resend** sends the last report to the hotel again at once. Both take effect immediately.
{% endhint %}

**Handling tab**

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2F2bNk7X9RpuHNITPe4UWY%2Fimage.png?alt=media&#x26;token=9c6588fa-012e-4f8a-8781-b28c5b3f276e" alt="The Handling Options sub-tab with the required Creditor drop-down, the Account Debit field, and the Add Own Schedule checkbox"><figcaption><p>Handling Options.</p></figcaption></figure>

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2FlqgPpdMYXlkXAPXOQDSv%2Fimage.png?alt=media&#x26;token=31b573b3-d20f-4713-9f37-b8b5ff72ed24" alt="The Prices sub-tab with one handling price row showing arrival dates, booking dates, a price, and a start and end age"><figcaption><p>Handling prices.</p></figcaption></figure>

<figure><img src="https://1539646852-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FZCqO8EQ5P5Mioq1zbQAc%2Fuploads%2Fl9QJ8VIyoZq760C6pC0t%2Fimage.png?alt=media&#x26;token=f4d18e6a-ccb0-4d50-abce-3ef4c3e52618" alt="The Hotels sub-tab with a checklist of hotels, three of them selected for handling"><figcaption><p>Hotels the handling fee applies to.</p></figcaption></figure>

#### Related pages

* [Suppliers](./)
* [Extra supplier](extra-suplier.md)
* [Users](../users/users/)
* [Hotels](../hotel/hotels/)
* [How to create a creditor](../autobilling/how-to-create-a-creditor.md)
