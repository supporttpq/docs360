# Hotel release - Reporting

### Overview

The **Hotel Release Reporting Scheduler** is a set of configurable rules that are executed periodically by a Windows service.&#x20;

The **Hotel Release** functionality controls when rooms from allotment and secured inventory are withdrawn from sale.

{% hint style="info" %}
A release determines when reserved inventory (allotment or secured rooms) is no longer available for booking.
{% endhint %}

#### Core Rule

* When a **release is activated**, all rooms from:
  * allotment rooms (AR)
  * secured rooms (SR)\
    must be removed from sale.
* The system prevent any further sales of these rooms after the release is triggered.

The scheduler automates the release of hotel rooms according to the rules defined in Tourpaq Office, ensuring timely notifications to suppliers and proper management of allotments.

### Core Behavior

{% hint style="danger" %}
A release overrides availability.
{% endhint %}

* When a **release is activated**:
  * all **allotment rooms (AR)** and **secured rooms (SR)** are removed from sale
* These rooms:
  * remain in inventory
  * but are **no longer bookable**

### Purpose

Use the scheduler to:

* send release lists daily, weekly, monthly, or annually
* ensure release rules run consistently
* reduce manual work

#### Related pages

* [Releases](./)
* [Hotel release - automation](hotel-release-automation.md)

### Create or edit a scheduler rule

To configure a rule for a hotel:

1. Go to **Dashboard → Hotel → Releases → Scheduler**.
2. Click **Add Record**.
3. Fill in the scheduler fields.
4. Click **Insert**.
5. Edit existing rows inline and click **Update**.

{% hint style="info" %}
Dates in the screenshots use the format **DD.MM.YYYY**.
{% endhint %}

### Booking Cancellation Handling

#### Behavior

* When a booking is cancelled:
  * if it used **AR or SR**, the rooms are marked as **released**
  * if a release is already active:
    * the room **does not return to sale**

{% hint style="warning" %}
Cancelled rooms are not automatically reintroduced into availability if a release applies.
{% endhint %}

#### Inventory Adjustment Rules

* On cancellation:
  * **increase AR/SR counts**
  * **do not increase free rooms**

{% hint style="info" %}
The inventory is restored at contract level (AR/SR), but not at sellable level.
{% endhint %}

### Screenshot

<figure><img src="../../../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure>

### Release Tab – UI Enhancements and Filtering

#### 1. “Show all” Filter

* &#x20;**“Show all”  -** checkbox

**Behavior**

* Unchecked (default): show only **active dates**
* Checked: show all records

***

#### 2. Period Filter

* Name: **Period**
* Behavior: period selector
  * includes standard future presets (e.g. next week, next month)

**Logic**

* When a period is selected: display only releases that **impact the selected period**

### Release Configuration

#### Dynamic Interval Column

![](<../../../.gitbook/assets/image (746).png>)

The second column changes depending on the selected **INTERVAL**:

| Interval | Column Name  | Description                                              |
| -------- | ------------ | -------------------------------------------------------- |
| DAILY    | DATE         | Release triggers once on a specific date                 |
| WEEKLY   | WEEKDAY      | Release triggers on a specific weekday across the period |
| MONTHLY  | DAY-OF-MONTH | Release triggers on a specific day each month            |
| ANNUALLY | DATE         | Release triggers once per year on a specific date        |

### Field definitions

| Field                   | What it controls                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Interval**            | <p>How often the scheduler runs. </p><ul><li>If <strong>Daily</strong> is chosen the scheduler will run every day. Next to interval drop down is a date field and if chosen it will run the scheduler not before that date.</li><li>If <strong>Weekly</strong> the scheduler will run every week at a mandatory day specified right next to the interval drop down.</li><li>If <strong>Monthly</strong> is chosen the scheduler will run every month on a day specified right next to interval drop down.</li><li>If <strong>Annually</strong> is chosen the scheduler will run every year on a day specified right next to interval drop down.</li></ul> |
| **Days**                | <p><strong>For DAILY:</strong></p><ul><li>Tooltip: Number of days before the release is activated.<br>After creation, the value can be adjusted in “Allotment per Day”.</li></ul><p><strong>For NON-DAILY:</strong></p><ul><li>Tooltip: Number of days before the release is activated.</li></ul>                                                                                                                                                                                                                                                                                                                                                         |
| **Hour**                | <p>Time of day when the release is activated.<br>If an email is configured, it is sent at this time.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Email**               | <p>If an email address is defined, a “Hotel Release” email is sent listing affected rooms and dates.<br>Requires a configured “Hotel Release” template in Email Center for the first agency.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Room Type**           | The room type(s) affected by the release.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **From Date**           | The first date when the release can be activated.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **To Date**             | The last date when the release can be activated.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Cut Down Allotments** | <p>If enabled, rooms are removed from sale after the release.<br>Email sending is independent of this setting.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Clone**               | Enables a Clone button to duplicate existing release lines.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

### Scheduler Types

{% tabs %}
{% tab title="Daily" %}
<figure><img src="../../../.gitbook/assets/image (747).png" alt=""><figcaption></figcaption></figure>

* Runs every day starting from the first execution date.

Example:

* Service runs on **24.03.2025**.
* Interval from **Days After** is **24.03.2025 → 31.03.2025**.
* Rule period is **27.03.2025 → 31.03.2025**.
* Result: only **27.03.2025 → 31.03.2025** is included.
{% endtab %}

{% tab title="Weekly" %}
<figure><img src="../../../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure>

* Runs once per week.
* You must choose the weekday.
* Useful for hotels that want to release rooms on a consistent weekly schedule.
{% endtab %}

{% tab title="Monthly" %}
<figure><img src="../../../.gitbook/assets/image (749).png" alt=""><figcaption></figcaption></figure>

* Runs once per month.
* You must choose the day of month.
* Ideal for monthly batch updates of hotel room availability.
{% endtab %}

{% tab title="Annually" %}
<figure><img src="../../../.gitbook/assets/image (750).png" alt=""><figcaption></figcaption></figure>

* Runs once per year.
* It covers the configured **Start Period** and **End Period**.

{% hint style="info" %}
In annual mode, **Days After** is ignored.
{% endhint %}
{% endtab %}
{% endtabs %}

### Notes and limitations

* Each scheduler row belongs to one hotel.
* The scheduler only runs if the Windows service is running.
* Use the release logs to audit what was sent and when.

### FAQ

#### Does this scheduler release rooms, or only send a report?

It sends a scheduled release list.

If **Cut Down Allotments** is enabled, it also updates availability.

#### Can one scheduler rule cover multiple hotels?

No. Each row is linked to one hotel.

#### Which email address receives the release list?

The address entered in the **Email** field for that scheduler row.

#### What time does the list get sent?

The **Hour** value in the scheduler row.

#### Why are some dates missing from the exported interval?

The exported interval is limited by:

* **Start Period** and **End Period**
* any period constraints on the underlying release rules

#### What’s the difference between this and “Hotel release - automation”?

Automation identifies rooms to release and marks allotments as **Suitable for release**.

This scheduler controls when release lists are sent and over which date interval.
