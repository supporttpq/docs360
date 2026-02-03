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

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Common tasks

{% stepper %}
{% step %}
### Create a brand-specific year definition

1. Select the brand in the agency selector.
2. Set **Year value**.
3. (Optional) Set **Start / end period**.
4. Save.
{% endstep %}

{% step %}
### Set a default interval

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

### FAQ

<details>

<summary><strong>What happens if a brand has no year definition?</strong></summary>

Tourpaq uses the **default interval**, if one is defined.

If no default exists, weekly statistics may be incomplete or misaligned.

</details>

<details>

<summary><strong>When should I use Start / end period?</strong></summary>

Use it when your reporting year does not match the calendar year.

This is common for seasonal operations.

</details>

<details>

<summary><strong>Why does the first stat week not start on 01-01?</strong></summary>

Weeks follow the system’s week start day.

If 01-01 is mid-week, the first full week starts later.

</details>

<details>

<summary><strong>Can I define different intervals per brand?</strong></summary>

Yes. The agency selector scopes the definition to a single brand.

Brands without a definition can still inherit the default interval.

</details>
