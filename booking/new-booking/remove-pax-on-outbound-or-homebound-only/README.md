---
description: >-
  Use No-show in Travel plan to remove a passenger (pax) from outbound or
  homebound only. Learn what it affects, when it resets after transport changes,
  and export/reporting impacts.
---

# Remove pax on outbound or homebound only

### Overview

Use **No-show** in **Travel plan** to remove a passenger (**pax**) from **outbound** or **homebound** only.

It works per flight line. It does not delete the passenger from the booking.

### What this does (and does not do)

**No-show does:**

In Tourpaq Office, you set this on the booking’s **Travel plan** per passenger and per flight line.

Example: the passenger travels outbound, but not homebound.

Use **No-show** when a passenger should be removed from **one direction only**.

* Mark a passenger as not travelling on a specific flight line.
* Let you mark outbound and homebound independently.

**No-show does not:**

* Remove the passenger from the booking entirely.
* Automatically carry over if you change the passenger’s transport.

{% hint style="info" %}
Terminology:

* **Pax** = passenger.
* **Outbound** = travelling out.
* **Homebound** = travelling back home.
{% endhint %}

***

### Before you start

* You can open and edit bookings in Tourpaq Office.
* You have permission to edit the booking’s **Travel plan**.

***

### Mark a passenger as No-show for outbound or homebound

{% stepper %}
{% step %}
### 1. Open the booking

Open an existing booking (or create one).

Make sure the booking is in **edit** mode.

<figure><img src="../../../.gitbook/assets/image (264).png" alt="Booking in edit mode before setting No-show in Travel plan"><figcaption><p>Open the booking in edit mode.</p></figcaption></figure>
{% endstep %}

{% step %}
### 2. Go to the Travel plan

In **Details**, open the **Travel plan** tab.

You will see a **No-show** column with a checkbox per travel line.

Each line is tied to a **passenger + flight segment**.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (2) (1).png" alt="Travel plan tab showing No-show checkbox per passenger and flight segment"><figcaption><p>Travel plan: No-show is set per passenger per travel line.</p></figcaption></figure>
{% endstep %}

{% step %}
### 3. Set No-show on the specific line

Tick **No-show** for the passenger on the outbound or homebound line you need.

The change is saved immediately.

You do not need to open the passenger screen first.

<figure><img src="../../../.gitbook/assets/image (2) (1) (3).png" alt="No-show checkbox selected for one passenger on the outbound or homebound line"><figcaption><p>Tick No-show on the outbound or homebound line you want to remove.</p></figcaption></figure>
{% endstep %}

{% step %}
### 4. Verify it stays set when you only edit other booking data

Edit the booking, but keep the passenger’s transport unchanged.

The No-show checkbox stays set.

<figure><img src="../../../.gitbook/assets/image (4) (3).png" alt="No-show remains set after editing other booking data without changing transport"><figcaption><p>No-show remains set if the transport line stays unchanged.</p></figcaption></figure>
{% endstep %}

{% step %}
### 5. Know when No-show is reset

If you change the passenger’s transport data, No-show is cleared.

Common changes:

* Changing flight date or interval
* Switching transport/flight

This happens because the system treats the updated transport as **new travel data**.

<figure><img src="../../../.gitbook/assets/image (6) (3).png" alt="No-show reset after changing passenger transport details"><figcaption><p>Changing the transport line clears No-show.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

### Notes

* No-show is set **per line**. One passenger can be No-show outbound only.
* No-show stays set until the transport line changes.
* If you change transport, re-check No-show afterwards if still needed.

### FAQ

<details>

<summary><strong>What’s the difference between No-show and removing a passenger?</strong></summary>

**No-show** removes the passenger from a specific **travel line** (outbound or homebound).

It does not remove the passenger from the booking.

</details>

<details>

<summary><strong>Where do I set No-show?</strong></summary>

Set it on the booking in **Details → Travel plan**.

It is a checkbox per passenger per flight segment.

</details>

<details>

<summary><strong>Why did my No-show checkbox disappear or reset?</strong></summary>

No-show is cleared when the passenger’s **transport line changes**.

Example: you change flight date/interval or switch the transport.

</details>

<details>

<summary><strong>Does No-show stay set if I edit other booking data?</strong></summary>

Yes.

If you edit other data and keep the transport unchanged, No-show stays set.

</details>

<details>

<summary><strong>How does No-show affect exports, lists, and reporting?</strong></summary>

It can impact which passengers are included on outputs that are based on travel lines.

See the detailed behavior here:

* [Remove pax on outbound or homebound only, Export lists impact](remove-pax-on-outbound-or-homebound-only-export-lists-impact.md)
* [Remove pax on outbound or homebound only, Transport Reporting Impact](remove-pax-on-outbound-or-homebound-only-transport-reporting-impact.md)

</details>
