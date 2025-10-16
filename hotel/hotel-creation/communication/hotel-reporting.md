# Hotel reporting

### Overview

The **Hotel Reporting** feature allows automated sending of booking lists directly to suppliers from the hotel module. These lists are identical to those found in the **Export Lists** section, but can be scheduled to run and send automatically.

### Purpose

This feature helps hotels maintain efficient communication with suppliers by ensuring they receive timely updates on bookings. Reports can be tailored to show either recent bookings or upcoming arrivals, reducing manual work and ensuring suppliers always have the latest information.

### Field Explanations

* **Interval** – Defines how often the report is sent (daily, weekly, monthly, annually).
* **Bookings Made** – Generates a report of all bookings created within the last _X_ days.
  * ⚠️ Mutually exclusive with **Days After** (only one can be selected).
* **Days After** – Generates a report of all bookings arriving within the next _X_ days.
* **Hour** – The exact time the email is sent.
* **E-mail** – The recipient email address that will receive the report.
* **Schedulers** – Displays all scheduled reports and allows reviewing of previously sent lists.
* **Reporting** – Defines the type of list/report to be generated.
* **Empty List** – If checked, a report will be sent even when no bookings exist for the selected interval.

### Instructions of Use

1. Go to the **Hotel Reporting** tab.
2. Click **Create** to set up a new scheduled report.
3. Select the **Interval** (daily, weekly, monthly, annually).
4. Choose one of the following:
   * **Bookings Made** – to include reservations created in the past _X_ days, OR
   * **Days After** – to include bookings arriving in the next _X_ days.
5. Set the **Hour** for when the report should be sent.
6. Enter the **Email** address of the supplier.
7. (Optional) Check the **Empty List** if you want reports to be sent even when there are no bookings.
8. Save the scheduler.
9. Use the **Schedulers** section to view and manage all scheduled reports.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
