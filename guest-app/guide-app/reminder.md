---
description: The Reminder section on the Guide App Home screen.
---

# Reminder

**Applies to:** Guide App, Tourpaq Office · **Last reviewed:** 12-10-2026

Guides at a destination handle many small, time-bound tasks: a guest pick-up, a meeting with a colleague, a call to make. The **Reminder** section lets a guide record such a task with a date and time, and pass it to another guide.

#### Overview

**Reminder** is one of the ten sections on the Guide App Home screen. It opens the **Reminders** screen, where a guide can:

* Create a reminder with a title, description, date, time, alarm and alarm sound.
* Send a reminder to another guide.
* Accept or decline a reminder that another guide sent.
* Review reminders in three lists: **Accepted and local reminders**, **Not answered reminders** and **Sent reminders**.

Reminders that guides send to each other are also listed in Tourpaq Office on the Guide Reminders page.

#### Purpose

Use Reminder to:

* Keep track of a task that must happen at a set date and time.
* Hand a task to another guide and see whether that guide accepted or declined it.
* Set an alarm ahead of the due time, from five minutes to one week before.

#### Preconditions

* You have a Tourpaq user and can sign in to the Guide App — see Guide App and Users Management.
* To send a reminder, the receiving guide exists in Tourpaq — see Guide teams.

{% hint style="danger" %}
**TO VERIFY** — Which user rights or user type does a guide need to see and use the Reminder section? Guide Reminders says only Guide Masters, Guide Teams and Sales Ledger users open the Tourpaq Office menu, and that only a guide team can add reminders. Does the same restriction apply to the Guide App?
{% endhint %}

{% hint style="danger" %}
**TO VERIFY** — Which guides appear in **Send to other guide**? All guides of the brand, only guides in your guide team, or another rule?
{% endhint %}

#### How-to

{% stepper %}
{% step %}
**Open the Reminders screen**

On the Guide App Home screen, tap **Reminder**. The **Reminders** screen opens. Tap the list name at the top to switch between **Accepted and local reminders**, **Not answered reminders** and **Sent reminders**.

<figure><img src="../../.gitbook/assets/image (18).jpg" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Create a reminder**

Tap **+** at the top right of the **Reminders** screen. Enter a **Title**, for example `Airport pick-up – group of 12`. Enter a **Description**, for example `Meet the group at arrivals, hall B`. Select the **Date** and **Time**, for example `14 Oct 2026` and `07:30`. Tap **Set alarm** and select when the alarm fires, for example **1 hour before**. Optional: select an **Alarm sound**. Tap **Save**.

<figure><img src="../../.gitbook/assets/image (17).jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (16).jpg" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Send a reminder to another guide**

Fill in the form as in the previous task. In **Send to other guide**, select the guide who must receive the reminder. The top-right action changes from **Save** to **Send**. Tap **Send**, then tap **YES** on the question **Do you want to send this reminder?**

<figure><img src="../../.gitbook/assets/image (15).jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (14).jpg" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Answer a reminder you received**

Open the **Not answered reminders** list and tap the reminder. Read the title, description, date, time, alarm, alarm sound and the guide it came from. Tap **ACCEPT** to accept it, or **Decline** at the top right to decline it. Tap **YES** on the confirmation question, for example **Do you want to accept this reminder?**

<figure><img src="../../.gitbook/assets/image (13).jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (12).jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (11).jpg" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Check the answer to a reminder you sent**

Open the **Sent reminders** list. Each entry shows the receiving guide and the answer: **Accepted** or **Declined**.


{% endstep %}

{% step %}
**Review your active reminders**

Open the **Accepted and local reminders** list. Use the **Active** and **Completed** tabs to switch between open and finished reminders. Entries are grouped by day, for example **TODAY**.

<figure><img src="../../.gitbook/assets/image (19).jpg" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

An accepted reminder appears in **Accepted and local reminders**, and the sender sees the answer in **Sent reminders**. In Tourpaq Office, open Guide Reminders to see sender, recipient, alarm date and status.

{% hint style="warning" %}
Sending a reminder delivers it to another guide, who can accept or decline it. The app asks you to confirm before it sends.
{% endhint %}

{% hint style="danger" %}
**TO VERIFY** — After a reminder is saved or sent, can the guide edit it, recall it or delete it?
{% endhint %}

#### Field Reference

**New reminder form**

| Field                   | Description                                                                                                                                                                                                                                      | Required  | Notes                                                                                                                                           |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Title**               | Short name of the task. It is the main line of the reminder in every list.                                                                                                                                                                       | TO VERIFY | Also shown as **Title** in Tourpaq Office Guide Reminders.                                                                                      |
| **Description**         | Details of the task. It appears under the title in the lists.                                                                                                                                                                                    | TO VERIFY |                                                                                                                                                 |
| **Date**                | Day on which the reminder is due. Shown as `12 Oct 2026`.                                                                                                                                                                                        | TO VERIFY |                                                                                                                                                 |
| **Time**                | Time of day at which the reminder is due. Shown as `13:35`.                                                                                                                                                                                      | TO VERIFY |                                                                                                                                                 |
| **Set alarm**           | When the alarm fires relative to the due time. Options: **At time of event**, **5 minutes before**, **15 minutes before**, **30 minutes before**, **1 hour before**, **2 hours before**, **1 day before**, **2 days before**, **1 week before**. | TO VERIFY |                                                                                                                                                 |
| **Alarm sound**         | The sound used for the alarm.                                                                                                                                                                                                                    | TO VERIFY | A received reminder shows **Not set** when the sender chose no sound.                                                                           |
| **Send to other guide** | The guide who receives the reminder.                                                                                                                                                                                                             | No        | When a guide is selected, the top-right action reads **Send**. With no guide, it reads **Save**. A cross next to the name clears the selection. |

{% hint style="danger" %}
**TO VERIFY** — Which fields are mandatory? What happens when the date and time are in the past? What does the alarm do when it fires (notification, sound, with the app closed), and which sounds can be chosen?
{% endhint %}

**Reminder lists**

| List                             | Description                                                                                                                                                                                     |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Accepted and local reminders** | Reminders you accepted and reminders you created for yourself. Has **Active** and **Completed** tabs. Entries are grouped by day and show title, description and the sending guide (**From:**). |
| **Not answered reminders**       | Reminders sent to you that you have not accepted or declined. Tap one to open it.                                                                                                               |
| **Sent reminders**               | Reminders you sent. Each entry shows the receiving guide (**To:**) and **Accepted** or **Declined**.                                                                                            |

{% hint style="danger" %}
**TO VERIFY** — (1) Does **Save** with no receiving guide create the _local_ reminder? (2) How does a reminder move from **Active** to **Completed**, and what happens when a reminder is overdue? (3) What does **Sent reminders** show before the receiving guide answers? (4) Does the receiving guide get a push notification when a reminder arrives?
{% endhint %}

**Tourpaq Office**

| Item                | Description                                                                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Guide Reminders** | Tourpaq Office page that lists reminders with sender (**From**), recipient (**To**), **Title**, **Submission Date**, **Alarm Date** and status. See Guide Reminders. |

{% hint style="info" %}
The notifications described on Guide App in the session expiry section relate to payments on extra orders. They are not the Reminder section.
{% endhint %}

{% hint style="danger" %}
**TO VERIFY** — The Guide App shows **Declined**, and Tourpaq Office filters by **Rejected**. Are they the same status? Do reminders created only for yourself appear in Tourpaq Office? Do alarms stop when the session expires?
{% endhint %}

#### Related pages

* Guide App
* Guide Reminders
* Guide teams
* Users Management
