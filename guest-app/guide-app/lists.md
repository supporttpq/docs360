---
description: >-
  Passenger lists that a guide exports from the Guide App, and the matching
  Tourpaq Office pages.
---

# Lists

**Applies to:** Tourpaq Office · **Last reviewed:** 02-10-2026

{% hint style="danger" %}
**TO VERIFY** — The **Lists** section of the Guide App has not been inspected for TQA-4298. The statements below are carried from the existing Guide App page and Tourpaq Office documentation.
{% endhint %}

#### Overview

**Lists** is the section of the Guide App where a guide generates export files with the guests booked on excursions and other lists. The same lists are available in Tourpaq Office.

#### Purpose

* Give the guide the guest lists needed to run excursions.
* Check which guests have booked an excursion.

#### Preconditions

* The guide signs in as a **guide** or **guide master**. Other users cannot generate the export files.
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

Open the Destination Lists page in Tourpaq Office.
{% endstep %}
{% endstepper %}

{% hint style="danger" %}
**TO VERIFY** — The existing page gives the Office path as **Extras → Destination Lists**. Confirm that path on staging, and list the steps and buttons in the app.
{% endhint %}

#### Field Reference

{% hint style="danger" %}
**TO VERIFY** — Filters and options on the **Lists** screen, and the settings in Tourpaq Office that decide which bookings appear on each list.
{% endhint %}

**Sales ledger**

The sales ledger shows the excursions sold and the amount paid for each order, per booking. When you filter by allotment date, it also shows the other excursions of a booking, even if they fall outside the search interval.

{% hint style="danger" %}
**TO VERIFY** — Is the sales ledger reached from **Lists** in the app, or only in Tourpaq Office? Staging shows a **Finance** page at the path `/finance/destination-sales`. Confirm its menu label and whether it is the same ledger. See also Guide Sales Ledger.
{% endhint %}

#### Related pages

* Guide App
* Extras
* Lists (Export)
* Extras List
* Guide Sales Ledger
