# Payment Plan - Hotel Contract Configuration

### Overview

The **Payment Plan** tab lets you define payment milestones for a hotel contract.

Each row is one planned payment (for example: deposit, installment, or payback).

This helps financial tracking and forecasting. It also supports more accurate settlement with the hotel.

***

### Screenshot

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Purpose

Use Payment Plan to:

* Document when payments are due.
* Track expected paybacks (if any).
* Keep payment schedules consistent for reporting and exports.

***

### Preconditions

Before you set up a payment plan:

* The hotel contract already exists.
* You know the payment dates and amounts agreed with the supplier.

***

### Fields

| Field            | Description                                                                                                        |
| ---------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Deposit Date** | Date when the payment is made. Use format `DD-MM-YYYY`.                                                            |
| **Payback Date** | Optional date for when the payment is returned or reconciled.                                                      |
| **Tot Amount**   | Amount for this payment milestone, in the contract currency. This is input manually or pulled from contract terms. |
| **Currency**     | Currency used for the payment. This is typically fixed per contract.                                               |
| **Year**         | Year used to group payment plans in the **Hotel Contract export**.                                                 |

***

### How it works

{% stepper %}
{% step %}
### Add a payment milestone

Add a new row for each planned payment.

Use one row per due date.
{% endstep %}

{% step %}
### Fill in dates and amount

Set **Deposit Date** and **Tot Amount**.

Set **Payback Date** only when you expect a payback.
{% endstep %}

{% step %}
### Set the grouping year

Pick **Year** to control how plans are grouped in the Hotel Contract export.

Keep this consistent across similar contracts.
{% endstep %}
{% endstepper %}

***

### Tips

{% hint style="info" %}
If you change payment plans on an active contract, align with finance first. It can affect follow-up, exports, and reconciliation workflows.
{% endhint %}

* Keep milestone amounts easy to reconcile (avoid unnecessary split lines).
* Leave **Payback Date** empty unless you have a defined payback event.

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md)

***

### FAQ

**Can I add multiple payment milestones?**\
Yes. Add one row per payment date.

**What date format should I use?**\
Use `DD-MM-YYYY`.

**When should I use “Payback Date”?**\
Use it when a payment is expected to be returned or reconciled later.\
If not relevant, leave it empty.

**Does “Tot Amount” have to match the contract total?**\
Not necessarily. It depends on your process and what you want to track.\
Finance typically expects the plan to reconcile against supplier settlement.

**Why can’t I change the currency here?**\
Currency is usually fixed per contract to avoid mixed-currency settlement.\
If you need a different currency, update the contract setup.

**What does the “Year” field control?**\
It controls grouping in the Hotel Contract export.\
Use it to keep payment plans organized across reporting periods.
