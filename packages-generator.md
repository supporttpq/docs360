---
description: >-
  Create A la Carte package suggestions in Tourpaq Office by combining one-way
  transports, hotels, rooms, and stay nights into generated departure-date
  packages for Select Offer.
---

# Packages Generator

## Overview

**Packages Generator** creates **A la Carte package suggestions** in Tourpaq Office.

A package combines **one-way transport legs** with **hotel + room stays** and a number of nights.

The generator then expands your rule into **generated packages** per departure date and check-in date.

## What it’s used for

* To create multi-step trips that combine several transports and hotel stays.
* To build **preset trips** and **circuit offers** (multi-destination).
* To simplify sales by offering pre-built packages in **Select Offer**.
* To market complex trips as one product for agencies and customers.

## Prerequisites

* Access to the **Price List** module.
* Transports must support **one-way seats** (outbound, between segments, and homebound).
* Hotels must have a valid **Price List per Day** for the travel period.

<figure><img src=".gitbook/assets/image (59) (1).png" alt="Packages Generator screen in Tourpaq Office"><figcaption><p>Create package rules and generate date-based package suggestions.</p></figcaption></figure>

## Create a package rule and generate packages

{% stepper %}
{% step %}
**Create a package**

1. Go to **Price List → Packages Generator**.
2. Click **Create**.
3. Fill in the package details:
   * **Package Name**
   * **Agency**
   * **Booking Period** (start and end date).
   * **Travel Interval** (the travel date range to generate packages for).
   * **Discount** (optional).
{% endstep %}

{% step %}
**Add the first travel segment**

1. **Add Transport** → Select a transport (must have one-way seats).
2. **Select Hotel** → Choose a hotel with an existing price list.
3. **Select Room** → Choose a room.
4. Set the **number of nights** for the stay.
{% endstep %}

{% step %}
**Add the next segment(s)**

1. Add another **Transport** for the next destination.
2. Add the next **Hotel** and **Room**, then set nights.
3. Use **Ignore Filter by Arrival** if the hotel list is too narrow.
4. Remove duplicate lines if you added the same hotel twice by mistake.
{% endstep %}

{% step %}
**Add the homebound leg**

1. Add the return transport.
2. If the expected route does not exist, search again and pick an available homebound.
3. Adjust nights if you need the return to align with the travel plan.
4. Mark the last leg as **One-way Home**.
{% endstep %}

{% step %}
**Generate packages**

1. Click **Save**.
2. Click **Generate**.
{% endstep %}
{% endstepper %}

<figure><img src=".gitbook/assets/image (61) (1).png" alt="Generated packages list with departures and hotel check-in dates"><figcaption><p>Generated packages are the date-based suggestions created from your rule.</p></figcaption></figure>

## Result and usage

* **View Content** → Displays all entities used in the package (transports, hotels, rooms).
* **Generated Packages** → Shows each generated departure date and hotel check-in date.
* Book packages via **Select Offer**.

{% hint style="info" %}
Packages Generator builds package **suggestions** and date-based combinations.

Pricing still depends on your underlying price lists and rules.
{% endhint %}

## Related pages

* [A la Carte](booking/new-booking/a-la-carte/)
* [Packages](booking/new-booking/a-la-carte/packages.md)
* [Pricelist](price-list/pricelist.md)
