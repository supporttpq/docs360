# Departure stat weeks

### Overview

Use **Departure stat weeks** to define how Tourpaq groups departures into weeks for statistics and reporting.

Go to **Setup → Departure stat weeks**.

You can define the week setup per **brand**. You can also set a **default interval** as a fallback.

This affects weekly reporting for metrics like sales, departures, and occupancy.

### How it works

1. Select the brand in the agency selector (top-right).
2. Create a year definition for the selected brand.
3. Optionally mark it as the default interval.
4. Optionally set a start and end period.

Tourpaq then calculates **departure stat weeks** for that year.

Weeks start on the system’s week start day (often Monday).

### Fields

* **Agency selection**
  * Chooses which brand the definition applies to.
* **Year value**
  * The reporting year (for example, `2026`).
* **Set as default interval** (optional)
  * Used as a fallback for brands without their own definition.
* **Start / end period** (optional)
  * Use this when your “business year” is not the calendar year.
  * Controls the range Tourpaq uses to build weekly statistics.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt="Departure stat weeks configuration showing the agency selector and year interval fields"><figcaption></figcaption></figure></div>

### Common tasks

{% stepper %}
{% step %}
**Create a brand-specific year definition**

1. Select the brand in the agency selector.
2. Set **Year value**.
3. (Optional) Set **Start / end period**.
4. Save.
{% endstep %}

{% step %}
**Set a default interval**

1. Select the brand you want to use as the default baseline.
2. Enable **Set as default interval**.
3. Save.
{% endstep %}
{% endstepper %}

### Examples

#### Default year setup

Brand A has no year defined. A default interval is set from **01-01-2026** to **27-12-2026**.

* First departure stat week: **05-01-2026 → 11-01-2026**
* Last departure stat week: **starts 27-12-2026**

#### Custom year definition

Brand B defines its own interval for 2026: **15-12-2025** to **13-12-2026**.

This aligns reporting with an operational year instead of the calendar year.

* First departure stat week: **15-12-2025 → 21-12-2025**
* Last departure stat week: **starts 13-12-2026**
