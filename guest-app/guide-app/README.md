---
description: >-
  What the Guide App is, how guides sign in, and which Tourpaq Office settings
  feed each Home section.
hidden: true
noIndex: true
---

# Guide App

**Applies to:** Tourpaq Office · **Last reviewed:** 02-10-2026

{% hint style="danger" %}
**TO VERIFY** — Only the **Home** screen of the Guide App has been inspected for TQA-4298. Statements about other screens are carried from the previous Guide App documentation and have not yet been checked on a Guide App screen. Each one is marked on the page where it appears.
{% endhint %}

#### Overview

The **Guide App** is the mobile application that guides use at the destination. It tracks the activity of guides, helps guides coordinate with each other, supports guests directly through chat, and exports passenger lists in multiple formats. Guides also use it to sell excursions on behalf of guests.

A guide signs in with the username and password of a Tourpaq user. After sign-in, the **Home** screen shows ten sections: **Extras**, **Services**, **Lists**, **Tickets**, **Documents**, **Guides**, **Reminder**, **Reports**, **Sms** and **Conversations**. The top bar shows the title **Home** and a **Logout** link. Each section has its own page below this one.

The Guide App is not the Guest App. Guests sign in to the Guest App with a booking number. Content in Tourpaq Office under **Guest App** (Vocabulary, Insider Tips, Maps, Weekly Activities, Good to Know, Settings) is shown in the Guest App. An excursion can be ordered in both apps, as described on Extras.

#### Purpose

* Find which Tourpaq Office page feeds each Guide App section.
* Check what must be configured before a section shows data to a guide.
* Check which user rights a section needs.
* Tell the Guide App apart from the Guest App.

#### Preconditions

* A Tourpaq user for the guide — see Users Management and Guide teams.
* The Guide App is installed on the guide's device.
* For **Lists**: the user is a **guide** or **guide master**. Other users cannot generate the export files.
* For excursion sales in **Extras**: the setup described on Extras. Only guides can sell products in the app.

{% hint style="danger" %}
**TO VERIFY** — Which Guide App version and distribution channel (store or internal) do guides use on staging and production? Which user rights does each of the other Home sections need?
{% endhint %}

#### How-to

{% stepper %}
{% step %}
**Sign in**

1. Open the Guide App.
2. Enter the username and password of your Tourpaq user.
3. Confirm the sign-in.

The list of available menus is shown right after the sign-in succeeds.
{% endstep %}

{% step %}
**Open a section**

Tap the section on the **Home** screen. You can also open a section from the side menu, using the burger icon at the top left.
{% endstep %}

{% step %}
**Sign out**

On the **Home** screen, tap **Logout** in the top bar.
{% endstep %}

{% step %}
**Change how long a session lasts**

Go to **Users → Brands**, open the brand, and change **Destination API Token** on the **General** tab. Enter the number of minutes.
{% endstep %}
{% endstepper %}

After sign-in, the **Home** screen shows the sections listed under Field Reference. A session that is idle for longer than the configured time expires, and the guide signs in again.

{% hint style="danger" %}
**TO VERIFY** — What is the exact label of the sign-in button, and what does the guide see after a failed sign-in? Is the burger icon at the top left shown on screens other than **Home**? It is not on the **Home** screen.
{% endhint %}

#### Field Reference

**Home sections**

| Section           | Description                                                                                                        |
| ----------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Extras**        | Excursions that the guide can sell and the orders already made. Fed by Extras that are set up with **Guide sale**. |
| **Services**      | Not yet documented.                                                                                                |
| **Lists**         | Passenger lists that the guide can export. Guide or guide master login required.                                   |
| **Tickets**       | Not yet documented.                                                                                                |
| **Documents**     | Not yet documented.                                                                                                |
| **Guides**        | Not yet documented.                                                                                                |
| **Reminder**      | Not yet documented.                                                                                                |
| **Reports**       | Not yet documented.                                                                                                |
| **Sms**           | Not yet documented.                                                                                                |
| **Conversations** | Chat with guests. Not yet documented in detail.                                                                    |

**Session**

| Field                     | Description                                                                                                                                                        | Required | Notes                                                                                                                                                                         |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Destination API Token** | Number of minutes of inactivity after which the guide's session expires and notifications stop. Set in the **General** tab of Edit Brand under **Users → Brands**. | No       | The default is 30 minutes, counted from the last user action. A service stops the notifications, so a short delay can occur. The label still contains the word _Destination_. |

{% hint style="danger" %}
**TO VERIFY** — Confirm the field label, the default of 30 minutes and the menu path on the current **Users → Brands** screen.
{% endhint %}

**Known limitations**

* Only guides can add products and make them available in the app.
* Stop sales hours do not affect the guide's list of excursions. A guide sees all available excursions.
* An excursion with allotment type **None** or **LinkedToTransport** cannot be ordered in the apps.
* The status of an order in the app is cleared when the guest travels home.

#### Related pages

* Extras
* Lists
* Guest App
* Guide App (previous page)
* Guide teams
* Brands
