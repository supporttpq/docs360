---
description: >-
  Learn how Tourpaq Office recalculates free room count (FHA) in price lists
  using queue processing, instant booking updates, and manual recalculation.
---

# Free room count behavior

## Overview

This feature controls **free room count** recalculation in Tourpaq Office.

It updates the **Free Hotel Allotment (FHA)** value on **price list entries**.

Recalculation runs after hotel allotment changes, bookings, cancellations, or manual triggers.

## Why it matters

The recalculation is necessary to:

* Keep availability accurate across Office, Web Booking, and agency sites.
* Prevent booking errors caused by stale allotment values.
* Ensure price lists reflect the latest hotel allotment per day.

## Prerequisites

* The price list entry must have a **selling price** set (for example `P1`, `P2`, or `D1`).

If the selling price is `0` (or missing):

* The offer can still appear on the **agency presentation site**.
* The offer cannot be booked in **Web Booking** or **Tourpaq Office**.

## How recalculation works

### Automatic recalculation (queue)

Tourpaq Office uses a **queue** for bulk recalculation.

This is the typical flow after you update hotel allotments:

* Affected price list entries are added to the queue.
* The system processes entries one by one.
* FHA (free room count) is recalculated and saved.

Processing time depends on volume (rules, agencies, transports).

Typical time is **2–15 minutes**.

{% hint style="warning" %}
If recalculation takes **more than 15 minutes**, treat it as suspicious.

Check for large batch updates, service issues, or stuck queue processing.
{% endhint %}

### Instant recalculation (booking events)

Some actions recalculate FHA instantly.

When a booking is placed, cancelled, or modified (for example room replacement):

* Hotel allotment is updated immediately in **Hotel Allotment per Day**.
* The related price list entry is recalculated **instantly** (no queue).

This allows the same package to be booked again within seconds.

{% hint style="info" %}
Instant recalculation applies to the specific price list entry being booked.

Other price list entries selling the same hotel room on other transports may still wait for the queue.
{% endhint %}

### Manual recalculation

You can force a recalculation for a specific price list entry.

Click the **Magic Wand** icon on the price list entry.

The recalculation runs instantly.

<figure><img src=".gitbook/assets/image (64) (1).png" alt="Magic Wand icon for manual free room count (FHA) recalculation on a price list entry"><figcaption><p>Use the Magic Wand to manually recalculate the free room count (FHA).</p></figcaption></figure>

## FAQ

#### What is “free room count” in Tourpaq Office?

It is the **Free Hotel Allotment (FHA)** shown on a price list entry.

It represents how many rooms are currently available for that departure.

#### What triggers the queue-based recalculation?

Hotel allotment updates typically trigger it.

This includes creating, extending, or changing allotment per day.

#### Why was my booking updated instantly, but other transports still show old FHA?

Instant recalculation only applies to the booked price list entry.

Other price list entries for the same room type on other transports follow the queue.

#### How long should recalculation take?

Typically **2–15 minutes**.

It depends on how many rules and price list entries are queued.

#### What should I do if recalculation takes longer than 15 minutes?

Treat it as suspicious.

Check for:

* Large batch updates.
* Service interruptions.
* A stuck queue or failed processing.

#### Why can an offer be visible but not bookable?

A price list entry can be displayed even when its selling price is `0`.

In that case, it cannot be booked in Web Booking or Office.

#### How do I force an immediate recalculation?

Use the **Magic Wand** icon on the relevant price list entry.

#### Does this affect transport availability (FTA) too?

This page describes hotel free room count (**FHA**).

Transport free seat count (**FTA**) follows its own recalculation logic.
