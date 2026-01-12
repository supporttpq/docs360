# Hotel release - Reporting

### Overview

The **Hotel Release Reporting Scheduler** runs hotel release reporting on a schedule.

It is executed by a Windows service.

It sends release lists based on the configured rules in Tourpaq Office.

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

### Field reference

| Field                   | What it controls                                                                                                                                                     |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Interval**            | How often the scheduler runs. Daily can also use a “not before” start date. Weekly requires a weekday. Monthly requires a day of month. Annually runs once per year. |
| **Days After**          | How many days are included in the exported interval after the run date. Example: Run date **10.01.2014** + `7` means the interval **10.01.2014 → 17.01.2014**.       |
| **Hour**                | When the list is sent. This field is mandatory.                                                                                                                      |
| **Email**               | Who receives the list.                                                                                                                                               |
| **Room**                | Optional filter for a specific room type. Leave blank to include all room types.                                                                                     |
| **Start Period**        | Do not include allotments before this date.                                                                                                                          |
| **End Period**          | Do not include allotments after this date.                                                                                                                           |
| **Cut Down Allotments** | If enabled, the system sets **Available rooms = Booked rooms** and **Free rooms = 0** for the affected period. If disabled, availability is not modified.            |

### Scheduler Types

{% tabs %}
{% tab title="Daily" %}
<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs every day.
* You can set a “not before” date next to the interval.

Example:

* Service runs on **24.03.2025**.
* Interval from **Days After** is **24.03.2025 → 31.03.2025**.
* Rule period is **27.03.2025 → 31.03.2025**.
* Result: only **27.03.2025 → 31.03.2025** is included.
{% endtab %}

{% tab title="Weekly" %}
<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs once per week.
* You must choose the weekday.
{% endtab %}

{% tab title="Monthly" %}
<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs once per month.
* You must choose the day of month.
{% endtab %}

{% tab title="Annually" %}
<figure><img src="../../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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
