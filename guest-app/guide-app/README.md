---
description: >-
  What the Guide App is, how guides sign in, and which Tourpaq Office settings
  feed each Home section.
hidden: true
noIndex: true
---

# Guide App

#### Overview

The **Guide App** is the mobile application that guides use at the destination. A guide signs in with the username and password of a Tourpaq user.

After sign-in, the **Home** screen shows ten sections: **Extras**, **Services**, **Lists**, **Tickets**, **Documents**, **Guides**, **Reminder**, **Reports**, **Sms** and **Conversations**. The top bar shows the title **Home** and a **Logout** link. Each section has its own page below this one.

#### Purpose

* Find which Tourpaq Office page feeds each Guide App section.
* Check what must be configured before a section shows data to a guide.
* Tell the Guide App apart from the Guest App.

#### Preconditions

* A Tourpaq user for the guide — see Users Management and Guide teams.
* The Guide App is installed on the guide's device.

{% hint style="danger" %}
**TO VERIFY** — Which Guide App version and distribution channel (store or internal) guides use on staging and production?
{% endhint %}

#### How-to

{% stepper %}
{% step %}
**Sign in**

1. Open the Guide App.
2. Enter the username and password of your Tourpaq user.
3. Confirm the sign-in.
{% endstep %}

{% step %}
**Sign out**

On the **Home** screen, tap **Logout** in the top bar.
{% endstep %}
{% endstepper %}

After sign-in, the **Home** screen shows the sections listed under Field Reference.

{% hint style="danger" %}
**TO VERIFY** — What is the exact label of the sign-in button, and what does the guide see after a failed sign-in?
{% endhint %}

#### Field Reference

**Home sections**

| Section           | Description                                                     |
| ----------------- | --------------------------------------------------------------- |
| **Extras**        | Excursions that the guide can sell and the orders already made. |
| **Services**      | Not yet documented.                                             |
| **Lists**         | Passenger lists that the guide can export.                      |
| **Tickets**       | Not yet documented.                                             |
| **Documents**     | Not yet documented.                                             |
| **Guides**        | Not yet documented.                                             |
| **Reminder**      | Not yet documented.                                             |
| **Reports**       | Not yet documented.                                             |
| **Sms**           | Not yet documented.                                             |
| **Conversations** | Not yet documented.                                             |

**Session**

| Field                     | Description                                                                                                                                                        | Required | Notes                                                                                                                                               |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Destination API Token** | Number of minutes of inactivity after which the guide's session expires and notifications stop. Set in the **General** tab of Edit Brand under **Users → Brands**. | No       | The default is 30 minutes. A service stops notifications, so a short delay can occur. The field label still uses the obsolete name Destination App. |

{% hint style="danger" %}
**TO VERIFY** — Confirm the field label, the default of 30 minutes and the menu path on the current **Users → Brands** screen.
{% endhint %}

#### Related pages

* Guide App (existing page)
* Guest App
* Guide teams
* Brands
