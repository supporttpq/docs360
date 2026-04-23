---
description: >-
  How No-show affects Export → Lists outputs in Tourpaq Office. Learn which list
  types exclude outbound vs homebound no-show passengers and how to validate
  exports.
hidden: true
---

# Remove pax on outbound or homebound only, Export lists impact

### Overview

The booking **No-show** checkbox (set per travel line) affects which passengers appear in **Export → Lists** outputs.

This page shows the expected behavior for the most common export list types.

For how to set No-show on a booking, see [Remove pax on outbound or homebound only](./).

### Where this applies

This affects lists generated from [Export → Lists](../../../export-1/lists.md), where the output is based on travel lines.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (16).png" alt="Export → Lists filters and Report type selection in Tourpaq Office"><figcaption><p>Export → Lists: choose report type and filters before exporting.</p></figcaption></figure>

### Expected behavior by report type

When you export lists that include passengers, the output should exclude passengers flagged as No-show for the relevant direction.

* **Passenger list**
  * Excludes passengers flagged as **No-show outbound**.
* **Departure homebound**
  * Excludes passengers flagged as **No-show homebound**.
* **Transfer list**
  * Excludes passengers flagged as **No-show outbound**.
* **Transfer list homebound**
  * Excludes passengers flagged as **No-show homebound**.

### How to validate quickly

{% stepper %}
{% step %}
### 1) Create a test case

Pick a booking with at least one passenger.

Set No-show outbound or homebound for that passenger.
{% endstep %}

{% step %}
### 2) Export the relevant list

Go to **Export → Lists**.

Pick the report type you want to validate (Passenger list, Transfer list, etc.).
{% endstep %}

{% step %}
### 3) Verify the output

Confirm that the passenger is excluded only on the direction where No-show is set.
{% endstep %}
{% endstepper %}

### FAQ

#### The passenger disappeared from all lists. Why?

Check whether No-show was set on **both** the outbound and homebound lines.

Also verify you exported the intended report type (outbound vs homebound variants).

#### Why is No-show affecting exports at all?

Many lists are generated from travel lines.

No-show removes a passenger from a specific direction’s travel line. The export should mirror that.
