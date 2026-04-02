---
description: Recent Tourpaq releases, fixes, improvements, and documentation updates.
noIndex: true
icon: burst-new
---

# What's new

This page tracks recent Tourpaq releases and documentation updates.

It complements [Welcome to the Tourpaq Manual](<README (2).md>) and [Getting Started with Tourpaq](<README (1).md>) by showing what changed most recently.

### Overview

Recent changes are grouped by monthly version.

Each entry shows whether the update is new, changed, improved, fixed, breaking, or documentation-only.

### Purpose

This page gives new employees and existing teams one place to review recent Tourpaq changes.

It also links each release item to the relevant manual page for full details.

### Navigation

This page is placed at the top of the manual sidebar.

The newest month appears first.

### Interface overview

Each monthly release section includes:

* a monthly version label
* a release symbol
* a short summary
* a link to the relevant page

### How versioning works

Tourpaq releases follow a date-based versioning model (`YYYY-MM`).

There are no major or minor version numbers.

Updates are deployed continuously and documented here as they go live.

### Release symbols

* 🟡 **Changed** — Behaviour of an existing feature has changed.
* 🟢 **New** — New feature or page added.
* 🔵 **Improved** — Enhancement / Update to an existing feature.
* ⚪ **Fixed** — Bug fix or correction.
* 📄 **Docs** — Documentation added or updated with no product change.

### Recent release history

{% updates format="full" %}
{% update date="2026-04-02" %}
## 2026-04 (Documentation updates)

* 📄 **What's new** was added to track recent Tourpaq releases and documentation updates. See [What's new](./).
* 📄 **Price List** was updated with clearer search behavior, display logic, and bulk pricing guidance. See [Price List](price-list/pricelist.md).
* 📄 **Allotments** was updated with manual allotments, linked-to-transport allotments, and generic allotment guidance for Extras. See [Allotments](extras-setup/extras/allotments.md).
* 📄 **Print Tickets** was updated with clearer single-booking and bulk reprint workflows. See [Print Tickets](tickets/print-tickets.md).
* 📄 **Autobilling** was updated with prerequisites, invoice generation flow, lifecycle states, and troubleshooting. See [Autobilling](autobilling/).
{% endupdate %}

{% update date="2026-03-17" tags="tourpaq-v15.0" %}
## 2026-03 (Tourpaq v15.0)

* 🟢 **Transport Rules** added automatic extension support for transport rules. See [Edit Transport Rule](transport-rules/edit-transport-rule.md).
* 🔵 **Hotel release automation** now flags unused allotments as **Suitable for release** and emails suppliers automatically. See [Hotel release - automation](hotel/hotel-creation/releases/hotel-release-automation.md).
* 🔵 **Transport Rule Weekdays Support** adds weekday-based generation for transport rules that use two external providers. See [Transport Rule Weekdays Support](transport-rules/transport-rule-weekdays-support.md).
* 🔵 **Hotel release rules** were expanded with clearer day-level release logic, release-status recalculation, and editable past-date handling. See [Releases](hotel/hotel-creation/releases/).
* 📄 **Onboard a new employee (Tourpaq Office access)** was added to support user creation, role assignment, brand scope, and security setup. See [Onboard a new employee (Tourpaq Office access)](users/users/onboard-a-new-employee-tourpaq-office-access.md).
* 📄 A known transport-search edge case is now documented: departures can appear without a valid return date in specific rule-extension scenarios. See [Transport Search Displays Departure Without Return Date (Known Limitation)](booking/new-booking/new-booking/transport-search-displays-departure-without-return-date-known-limitation.md).
{% endupdate %}

{% update date="2026-02-03" %}
## 2026-02 (Tourpaq v14.9)

* 🟢 **Automatic ticket issue** was added for Amadeus GDS bookings, including deadline-based daily ticketing for eligible paid reservations. See [Automatic ticket issue](gds-queue-place/submit-a-gds-booking/automatic-ticket-issue.md).
* 🟢 **Individual payments** was added, allowing separate payment links per passenger on the same booking. See [Individual payments](booking/new-booking/individual-payments.md).
* 🟢 **QR code for vouchers** was added for faster voucher lookup and on-site validation. See [QR code for vouchers](booking/new-booking/qr-code-for-vouchers.md).
* 🔵 **Keep automatic discount prices** improves booking-edit handling by making price lock vs reprice behavior explicit for discounts, extras, and travel insurance. See [Keep automatic discount prices](booking/new-booking/keep-automatic-discounts-prices.md).
* 🔵 **No-show handling** was clarified for both transport reporting and export lists, improving operational consistency for outbound and homebound removals. See [Remove pax on outbound or homebound only, Transport Reporting Impact](booking/new-booking/remove-pax-on-outbound-or-homebound-only/remove-pax-on-outbound-or-homebound-only-transport-reporting-impact.md) and [Remove pax on outbound or homebound only, Export lists impact](booking/new-booking/remove-pax-on-outbound-or-homebound-only/remove-pax-on-outbound-or-homebound-only-export-lists-impact.md).
* 🔵 **Customer details on customer card** improves in-booking customer maintenance by saving reusable customer details directly from the booking flow. See [Customer info / Details on customer card](booking/new-booking/customer-info-details-on-customer-card.md).
* 📄 Ticket errata placement across ticket versions is now documented. See [Customer Information displayed on the Ticket](customer-information-errata/customer-information-displayed-on-the-ticket.md).
{% endupdate %}
{% endupdates %}

### Example

A release entry marked **🟢 New** means a new feature or workflow became available in that month.

A release entry marked **📄 Docs** means the manual changed, but the product behavior did not.

### Related pages

* [Welcome to the Tourpaq Manual](<README (2).md>)
* [Getting Started with Tourpaq](<README (1).md>)
* [Onboard a new employee (Tourpaq Office access)](users/users/onboard-a-new-employee-tourpaq-office-access.md)
