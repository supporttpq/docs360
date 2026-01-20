# Hotel reporting

### Overview

**Hotel Reporting** lets you email booking lists to suppliers automatically. The list content matches the lists in [Export → Lists](../../../export-1/lists.md).

### Purpose

Use Hotel Reporting to keep suppliers updated without manual exports. You can send either:

* new bookings made in the last _X_ days, or
* arrivals happening within the next _X_ days.

### Field Explanations

* **Interval** – How often the report is sent (daily, weekly, monthly, annually).
* **Bookings Made** – Includes bookings created within the last _X_ days.
* **Days After** – Includes bookings arriving within the next _X_ days.
* **Hour** – The time the email is sent.
* **Email** – The recipient email address.
* **Schedulers** – Shows all schedules and the send history.
* **Reporting** – The report type to generate.
* **Empty List** – Sends the report even when there are no results.

{% hint style="warning" %}
**Bookings Made** and **Days After** are mutually exclusive.\
Select only one of them.
{% endhint %}

### Instructions for Use

1. Go to the **Hotel Reporting** tab.
2. Click **Create** to add a schedule.
3. Select the **Interval**.
4. Select one option:
   * **Bookings Made** for bookings created in the last _X_ days.
   * **Days After** for bookings arriving in the next _X_ days.
5. Set the **Hour**.
6. Enter the supplier **Email** address.
7. Optional: enable **Empty List** to send empty reports.
8. Save the schedule.
9. Use **Schedulers** to review and manage schedules.

### Notes

* Create one schedule per supplier email address.
* Use **Schedulers** to confirm what was sent and when.

### FAQ

#### Can I use **Bookings Made** and **Days After** together?

No. Pick the one that matches your use case.

#### Why did I receive a report with no bookings?

**Empty List** was enabled. Disable it if you only want reports with results.

#### Can I send the same report to multiple recipients?

Create multiple schedules. Use one recipient email per schedule.

#### Where do I see previously sent reports?

Open **Schedulers**. It shows existing schedules and send history.

#### My supplier says they did not receive the email. What should I check?

Check the **Email** address for typos. Ask them to check spam or quarantine. Then verify the schedule exists and is saved.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Hotel Reporting scheduler setup screen"><figcaption><p>Hotel Reporting scheduler setup.</p></figcaption></figure>
