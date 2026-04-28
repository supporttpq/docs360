---
description: >-
  Configure supplier invoice schedules and manage creditor invoice statuses in
  Tourpaq Office Finance. Regenerate invoices and archive invoices when needed.
---

# Creditor invoices

## Overview

Creditor invoices automate and track **supplier invoicing** across service types like **hotels**, **extras**, **supplements**, and **handling fees**.

Use this feature to manage invoice schedules, track invoice statuses, and regenerate or archive invoices when needed.

Before you add schedules, make sure the supplier is configured in [How to create a creditor](how-to-create-a-creditor.md) and the overall flow is enabled in [Autobilling](./).

### Related pages

Use these pages together with creditor invoices:

* [Autobilling](./) for the full invoice automation flow
* [How to create a creditor](how-to-create-a-creditor.md) to set up the supplier record
* [How to set autobilling for hotels](how-to-set-autobilling-for-hotels.md) to configure hotel invoice schedules
* [How to set autobilling for extras](how-to-set-autobilling-for-extras.md) to configure extra invoice schedules
* [How to set autobilling for discounts/supplements](how-to-set-autobilling-for-discounts-supplements.md) to configure discount and supplement invoices
* [How to set autobilling for handling](how-to-set-autobilling-for-handling.md) to configure handling invoices
* [Invoice](../invoice.md) to review, archive, and pay generated invoices

***

## Purpose

This feature ensures that all creditor-related billing is performed on time and in alignment with contractual and operational requirements. By defining invoice schedules and managing invoice statuses, administrators can:

* Automate recurring invoicing tasks
* Maintain consistent accounting processes
* Simplify creditor reconciliation and reporting

📋 _Creditor invoice schedules overview — Finance → Autobilling_

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Configure invoice schedules for hotels, extras, supplements, and handling.</p></figcaption></figure>

***

## Setting invoice schedules

Invoice schedules define when and how invoices are automatically generated for specific entities such as hotels, extras, supplements, or handling services.

Schedule setup depends on the entity. Use the matching setup page for [hotels](how-to-set-autobilling-for-hotels.md), [extras](how-to-set-autobilling-for-extras.md), [discounts/supplements](how-to-set-autobilling-for-discounts-supplements.md), or [handling](how-to-set-autobilling-for-handling.md).

### Supported schedule types

You can create invoice schedules for:

* **Hotels**
* **Hotels (Before Arrival)**
* **Extras**
* **Supplements**
* **Handling**

### Configuration steps

{% stepper %}
{% step %}
#### Add New Schedule

Click **Add New Schedule** to start creating a new schedule.
{% endstep %}

{% step %}
#### Select interval type

Choose one of: **Daily** (every day), **Weekly** (select weekday), **Monthly** (select day of month), or **Days After** (number of days after an event, e.g. after departure).
{% endstep %}

{% step %}
#### Select entity

Choose the applicable hotel, extra, supplement, or handling entry.
{% endstep %}

{% step %}
#### Save configuration

Click **Save** to apply the new schedule.
{% endstep %}

{% step %}
#### Add additional schedules

_Optional._ Repeat the process to configure multiple schedules as needed.
{% endstep %}
{% endstepper %}

***

## Invoice statuses

Each invoice generated in the system follows a defined status flow that reflects its current position in the billing process.

| Status                                                 | Description                                                           |
| ------------------------------------------------------ | --------------------------------------------------------------------- |
| <mark style="background-color:yellow;">Pending</mark>  | Automatically assigned when an invoice is first generated.            |
| <mark style="background-color:green;">Approved</mark>  | Indicates that the creditor has reviewed and approved the invoice.    |
| <mark style="background-color:green;">Paid</mark>      | Assigned when an approved invoice has been marked as paid.            |
| Regenerated                                            | Set when the invoice has been recreated after updates or corrections. |
| Archived                                               | The invoice has been archived and stored for record-keeping.          |
| <mark style="background-color:purple;">Rejected</mark> | Indicates that the creditor has declined the invoice.                 |
| Deleted                                                | The invoice has been permanently removed from the system.             |

***

## Status flow examples

| Example flow                            | Description                                                                             |
| --------------------------------------- | --------------------------------------------------------------------------------------- |
| Pending → Approved → Paid → Regenerated | Typical flow where an invoice is processed, paid, and later regenerated for correction. |
| Pending → Approved → Regenerated        | The invoice is approved and then regenerated without payment.                           |
| Pending → Rejected → Regenerated        | The invoice is rejected by the creditor and later corrected.                            |
| Pending → Deleted                       | The invoice is removed before processing.                                               |
| Pending → Regenerated                   | The invoice is recreated before approval.                                               |

***

## Regenerating an invoice

Regeneration allows you to recreate an invoice in case of data corrections, supplier changes, or updated booking values.

{% hint style="warning" %}
**Before you regenerate** Ensure all underlying data (costs, booking values, supplier setup) has been corrected _before_ triggering regeneration. The old invoice will be marked Regenerated and a new Pending invoice will appear in its place.
{% endhint %}

### Steps to regenerate an invoice

{% stepper %}
{% step %}
#### Open invoice list

Navigate to **Finance → Invoice**.
{% endstep %}

{% step %}
#### Select invoice

Locate and select the invoice that needs to be regenerated.
{% endstep %}

{% step %}
#### Click Regenerate

Press the **Regenerate** button in the invoice action toolbar.
{% endstep %}

{% step %}
#### Confirm action

Click **OK** in the confirmation dialog to proceed.
{% endstep %}

{% step %}
#### Verify new invoice

The regenerated invoice will appear in the list with updated data and a Pending status.
{% endstep %}
{% endstepper %}

🔄 _Regenerate invoice action — Finance → Invoice list_

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Regenerate an invoice from Finance → Invoice when costs or booking values changed.</p></figcaption></figure>

***

## Result

{% hint style="success" %}
With invoice scheduling and lifecycle management, the **Creditor Invoice** feature provides a complete automation flow for supplier invoicing — from generation to payment — ensuring timely processing and accurate financial reporting across all creditor-related entities in Tourpaq.
{% endhint %}

Next, use [Invoice](../invoice.md) to work with generated invoices, or return to [Autobilling](./) to review the full process.

***

## FAQ

<details>

<summary>Where do I see all generated invoices?</summary>

In **Finance → Invoice**. See [Invoice](../invoice.md) for a full breakdown of filters and columns.

</details>

<details>

<summary>What's the difference between schedules and invoices?</summary>

A _schedule_ defines when invoices are generated. An _invoice_ is the generated record with a status (Pending / Approved / Paid / etc.).

</details>

<details>

<summary>When are scheduled invoices generated?</summary>

Based on the schedule (daily / weekly / monthly / days after). The exact runtime depends on your scheduled job setup — often overnight.

</details>

<details>

<summary>When should I regenerate an invoice?</summary>

Regenerate after changes to costs, booking values, supplier/creditor setup, or invoice details.

</details>

<details>

<summary>Can I archive invoices?</summary>

Yes. Archiving keeps invoices for record-keeping while removing them from the default working list (depending on your active filters).

</details>
