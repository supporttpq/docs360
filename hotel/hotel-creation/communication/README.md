# Communication

### Overview

The **Communication** tab lets you schedule booking-list emails for a hotel.\
The system generates the list automatically and sends it to your recipients.

### Purpose

This keeps hotels and agencies updated without manual exports.\
It helps partners plan arrivals and manage availability.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
This tab uses the same scheduler logic as [Hotel reporting](hotel-reporting.md).
{% endhint %}

### Field Explanations

* **Interval** – How often the report is sent:
  * **Daily** – The report is generated and sent every day.
  * **Weekly** – Sent every week on the selected weekday.
  * **Monthly** – Sent every month on the selected day.
  * **Annually** – Sent every year on the selected date.
* **Bookings Made** – Bookings created in the last **X** days.
* **Days After** – Bookings arriving in the next **X** days.
* **Hour** – The time the email is sent.
* **E-mail** – One or more recipient email addresses.
* **Schedulers** – Overview of all schedulers and their status.
* **Reporting** – The report format/type to generate.
* **Empty List** – Send the email even when the list is empty.

Examples:

* **Bookings Made = 7** sends bookings created in the last 7 days.
* **Days After = 7** sends arrivals in the next 7 days.

{% hint style="warning" %}
**Bookings Made** and **Days After** are mutually exclusive.\
Set one of them, not both.
{% endhint %}

### How to use

{% stepper %}
{% step %}
### 1. Create a scheduler

1. Open the hotel and go to **Communication**.
2. Click **Create**.
{% endstep %}

{% step %}
### 2. Configure what to send

1. Select an **Interval**.
2. Set either **Bookings Made** or **Days After**.
3. Select the **Reporting** type.
{% endstep %}

{% step %}
### 3. Set recipients and timing

1. Choose the **Hour**.
2. Add one or more **E-mail** recipients.
3. Optional: enable **Empty List**.
{% endstep %}

{% step %}
### 4. Save and monitor

1. Save the scheduler.
2. Use **Schedulers** to review status and history.
{% endstep %}
{% endstepper %}

### FAQ

#### Can I send the report to more than one email address?

Yes. Add multiple addresses in **E-mail**.

#### What’s the difference between **Bookings Made** and **Days After**?

* **Bookings Made** targets recently created bookings.
* **Days After** targets upcoming arrivals.

#### Can I use **Bookings Made** and **Days After** together?

No. Choose one. They filter different report types.

#### Why did I receive an empty report?

You likely enabled **Empty List**.\
Disable it to skip empty sends.

#### Where can I see what was sent earlier?

Open **Schedulers** and review the scheduler history and status.

#### How do I stop the emails from being sent?

Disable or delete the scheduler in **Schedulers**.

#### The report is not sent. What should I check?

Check **Schedulers** for errors and last run time.\
Also verify the recipient email addresses are correct.
