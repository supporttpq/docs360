# Notes

### Overview

The **Notes** tab is an internal field for storing operational context and team communication for an **Extra** product.

You’ll typically find it as the last tab in the Extra’s configuration.

{% hint style="info" %}
Notes are **internal only**. They do not populate the website, offers, tickets, or other customer-facing documents.
{% endhint %}

### When to use Notes

Use Notes to add context that helps colleagues understand **what was changed** and **why**.

Common use cases:

* **Internal clarifications**: Provider rules, operational constraints, or exceptions.
* **Change log**: Why a price, resource, or allotment was changed.
* **Team instructions**: What to do during cancellations, re-bookings, or manual handling.

### Field guide

<figure><img src="../../.gitbook/assets/image (585).png" alt=""><figcaption></figcaption></figure>

Use the UI elements above the text area to confirm you are writing in the right place.

**A. Product Identification (Header)**

* Product Name: `20kg Bagage inkl max 5kg håndbagage`
* System Code: `XBAG_JTD_S_20KG`

**B. Brands Context**

Above the notes field, you will see various brand divisions (e.g., _Tourpaq DK_, _Tourpaq SE_, _Tourpaq Live_).

* Status Indicators: For example, "For sale+Int" on _Tourpaq DK_ means the product is active for that specific Brand.
* Instruction: Notes are usually shared across brands. If your note only applies to one Brand, start the note with the brand name (for example: `Tourpaq SE:`).

**C. The "Enter notes..." Text Area**

* Input Type: Free-form text.
* Usage Instructions:
  1. **Be concise**: Write clear, actionable information.
  2. **Timestamp entries**: Start with date + initials.
  3. **Keep it product-level**: Avoid customer-specific information.
  4. **Save your changes**: Use **Save**/**Update** after editing. The field may not auto-save.

#### Recommended note format

Use a consistent format so others can scan and trust the history:

```
[YYYY-MM-DD - Initials]
Change:
Reason:
Impact (optional):
```

### FAQ

<details>

<summary>Are Notes visible to customers (web, offer, ticket, emails)?</summary>

No. Notes are meant for internal use only.

</details>

<details>

<summary>Should I write one long note, or multiple dated entries?</summary>

Use multiple dated entries. It keeps a clean audit trail and avoids overwriting context.

</details>

<details>

<summary>My note is only relevant for one brand. What should I do?</summary>

Start the note with the brand name (for example `Tourpaq SE:`) so it’s clear.

</details>

<details>

<summary>What kind of content should not be written in Notes?</summary>

Avoid:

* Passenger PII (names, passports, phone numbers, emails)
* Payment details
* Anything that belongs in a booking-specific service case

</details>

<details>

<summary>I updated the note but it didn’t “stick”. Why?</summary>

Most often, the page wasn’t saved.

After editing the Notes text area, click **Save** or **Update** on the page.

</details>

### Related pages

* [Extras](./)
* [Extras – Communication](communication.md)
* [Service Cases](../../service-cases/)
