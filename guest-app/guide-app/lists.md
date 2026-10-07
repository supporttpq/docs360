---
description: >-
  Passenger lists that a guide exports from the Guide App, and the matching
  Tourpaq Office pages.
---

# Lists

**Applies to:** Tourpaq Office · **Last reviewed:** 02-10-2026

{% hint style="danger" %}
**TO VERIFY** — The **Lists** section of the Guide App has not been inspected for TQA-4298. The statements below are carried from the previous Guide App page and from Tourpaq Office documentation.
{% endhint %}

#### Overview

**Lists** is the section of the Guide App where a guide generates export files with the guests booked on excursions and other lists. Passenger lists can be exported in multiple formats. The same lists are available in Tourpaq Office on the Destination Lists page.

Excursions sold in the apps, and Extra Orders made before departure in WebBooking (OneHome), appear in these lists. A product booked through OneHome is also included in the Guide App export.

#### Purpose

* Give the guide the guest lists needed to run excursions.
* Check which guests have booked an excursion.
* Check the excursions sold and the amount paid per booking, in the sales ledger.

#### Preconditions

* The user signs in as a **guide** or **guide master**. Other users cannot generate the export files.
* Excursions are sold as described on Extras.

{% hint style="danger" %}
**TO VERIFY** — Which list types does the **Lists** section offer, in which formats, and what filters does the guide set?
{% endhint %}

#### How-to

{% stepper %}
{% step %}
**Generate a list in the app**

Sign in as a guide or guide master, tap **Lists** and generate the export file.
{% endstep %}

{% step %}
**Generate the same list in Tourpaq Office**

Open the Destination Lists page in Tourpaq Office. The previous page gives the path as **Extras → Destination Lists**.
{% endstep %}
{% endstepper %}

{% hint style="danger" %}
**TO VERIFY** — Confirm the **Extras → Destination Lists** path on staging, and list the steps and buttons on the **Lists** screen in the app.
{% endhint %}

#### Field Reference

{% hint style="danger" %}
**TO VERIFY** — Filters and options on the **Lists** screen, and the settings in Tourpaq Office that decide which bookings appear on each list.
{% endhint %}

**Sales ledger**

The sales ledger shows the excursions sold and the amount paid for each order, per booking. When you filter by allotment date, it also shows the other excursions of a booking, even if they fall outside the search interval.

{% hint style="danger" %}
**TO VERIFY** — Is the sales ledger reached from **Lists** in the app, or only in Tourpaq Office? Staging has a **Finance** page at the path `/finance/destination-sales`. Confirm its menu label and whether it is the same ledger. See Guide Sales Ledger.
{% endhint %}

#### Related pages

* Guide App
* Extras
* Lists (Export)
* Extras List
* Guide Sales Ledger
