---
description: Recent Tourpaq releases, fixes, improvements, and documentation updates.
hidden: true
noIndex: true
icon: burst-new
---

# What's new

{% columns %}
{% column %}
## Tourpaq Release May 2026

New features, performance improvments and automation enhancements to help you work faster

<a href="./#recent-release-history" class="button primary" data-icon="book-open">See What's New -></a>
{% endcolumn %}

{% column %}
<figure><img src="../.gitbook/assets/screencapture-staging-bookingx-tourpaq.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}



### Release symbols

* 🟢 **New** — New feature or page added.
* 🔵 **Improved** — Enhancement / Update to an existing feature.
* 📄 **Docs** — Documentation added or updated with no product change.

{% updates format="full" %}
{% update date="2026-06-09" %}
## 2026-06 (Tourpaq v15.2)

* 🔵 Extra Category - Display in Hotel List filter
* 🔵 Extra Category - One product must be selected
{% endupdate %}

{% update date="2026-04-27" %}
## 2026-04 (Tourpaq v15.1)

* 📄 **What's new** was added to track recent Tourpaq releases and documentation updates. See [What's new](./).
* 📄 **Price List** was updated with clearer search behavior, display logic, and bulk pricing guidance. See [Price List](../price-list/pricelist.md).
* 📄 **Allotments** was updated with manual allotments, linked-to-transport allotments, and generic allotment guidance for Extras. See [Allotments](../extras-setup/extras-general-page/allotments.md).
* 📄 **Print Tickets** was updated with clearer single-booking and bulk reprint workflows. See [Print Tickets](../tickets/print-tickets.md).
* 📄 **Autobilling** was updated with prerequisites, invoice generation flow, lifecycle states, and troubleshooting. See [Autobilling](../autobilling/).
* 🟢 Editable board hotel allotment. See [Hotel Allotment](../hotel/hotel-creation/hotel-allotments/editable-board.md).
* 🟢 Log for Gouda & Europeiske insurance. See [Internal Logs](internal-logs/insurance-payload-log-gouda-and-europaeiske.md).
* 🟢 Land days to Real Transports. [See Real Transport - Departures](../real-transports/departures/add-land-days-to-real-transports-offset-handling.md).
* 🟢 Releases/Stop Sales Log. See [Releases/Stop Sales Log](../releases-stop-sales-log.md).
* 🟢 Support user role. See [Users - Support User Role](../users/users/support-user-role-gdpr-compliance.md)
* 🟢 Payment file import/File import format. See [File import format](../finance/payment-file-import/skjernbank-file-import-format.md).
* 🔵 Hotel Release reporting. See [Hotel release - Reporting](../hotel/hotel-creation/releases/hotel-release-reporting.md).
* 🔵 Remove GMT Offset. See [Arrival Gateway](arrival-gateways/) & [Departure Gateway](departure-gateways/).
* 🔵 Improvement to the new price list. See [Price List](../price-list/pricelist.md#price-list-search).
* 🔵 Add code/name where missing in fields/tables. See [Special Offers](../special-offers.md) & [Flight change](../flight-change/).
* 🔵 Rounding on Extras & Discount/Supplements. See the [Extras Category](../extras-category/) & [Discounts/Supplements Categories](../disc-suppl-categories.md).
* 🔵 Add a new Room Types filter in All bookings. See [All Bookings](../booking/all-bookings/).
* 🔵 Display Bookings and Total Pax for guide/guidemaster users in All Bookings. See [All Bookings](../booking/all-bookings/).
* 🔵 Payment registration new filtering. See [Payment registration](../finance/payment-registration.md).
{% endupdate %}

{% update date="2026-03-17" tags="tourpaq-v15.0" %}
## 2026-03 (Tourpaq v15.0)

* 🟢 **Transport Rules** added automatic extension support for transport rules. See [Edit Transport Rule](../transport-rules/edit-transport-rule.md).
* 🔵 **Hotel release automation** now flags unused allotments as **Suitable for release** and emails suppliers automatically. See [Hotel release - automation](../hotel/hotel-creation/releases/hotel-release-automation.md).
* 🔵 **Transport Rule Weekdays Support** adds weekday-based generation for transport rules that use two external providers. See [Transport Rule Weekdays Support](../transport-rules/transport-rule-weekdays-support.md).
* 🔵 **Hotel release rules** were expanded with clearer day-level release logic, release-status recalculation, and editable past-date handling. See [Releases](../hotel/hotel-creation/releases/).
* 📄 **Onboard a new employee (Tourpaq Office access)** was added to support user creation, role assignment, brand scope, and security setup. See [Onboard a new employee (Tourpaq Office access)](../users/users/onboard-a-new-employee-tourpaq-office-access.md).
* 📄 A known transport-search edge case is now documented: departures can appear without a valid return date in specific rule-extension scenarios. See [Transport Search Displays Departure Without Return Date (Known Limitation)](../booking/new-booking/new-booking/transport-search-displays-departure-without-return-date-known-limitation.md).
{% endupdate %}

{% update date="2026-02-03" %}
## 2026-02 (Tourpaq v14.9)

* 🟢 **Automatic ticket issue** was added for Amadeus GDS bookings, including deadline-based daily ticketing for eligible paid reservations. See [Automatic ticket issue](../gds-queue-place/submit-a-gds-booking/automatic-ticket-issue.md).
* 🟢 **Individual payments** was added, allowing separate payment links per passenger on the same booking. See [Individual payments](../booking/new-booking/individual-payments.md).
* 🟢 **QR code for vouchers** was added for faster voucher lookup and on-site validation. See [QR code for vouchers](../booking/new-booking/qr-code-for-vouchers.md).
* 🔵 **Keep automatic discount prices** improves booking-edit handling by making price lock vs reprice behavior explicit for discounts, extras, and travel insurance. See [Keep automatic discount prices](../booking/new-booking/keep-automatic-discounts-prices.md).
* 🔵 **No-show handling** was clarified for both transport reporting and export lists, improving operational consistency for outbound and homebound removals. See [Remove pax on outbound or homebound only, Transport Reporting Impact](../booking/new-booking/remove-pax-on-outbound-or-homebound-only/remove-pax-on-outbound-or-homebound-only-transport-reporting-impact.md) and [Remove pax on outbound or homebound only, Export lists impact](../booking/new-booking/remove-pax-on-outbound-or-homebound-only/remove-pax-on-outbound-or-homebound-only-export-lists-impact.md).
* 🔵 **Customer details on customer card** improves in-booking customer maintenance by saving reusable customer details directly from the booking flow. See [Customer info / Details on customer card](../booking/new-booking/customer-info-details-on-customer-card.md).
* 📄 Ticket errata placement across ticket versions is now documented. See [Customer Information displayed on the Ticket](../customer-information-errata/customer-information-displayed-on-the-ticket.md).
{% endupdate %}
{% endupdates %}

### Example

A release entry marked **🟢 New** means a new feature or workflow became available in that month.

A release entry marked **📄 Docs** means the manual changed, but the product behavior did not.

### Related pages

* [Welcome to the Tourpaq Manual](../)
* [Getting Started with Tourpaq](<../README (1).md>)
* [Onboard a new employee (Tourpaq Office access)](../users/users/onboard-a-new-employee-tourpaq-office-access.md)





## What's new

Stay up to date with the latest features, improvements, and fixes across the Tourpaq platform. Updated continuously by the product team.

{% hint style="info" %}
🚀 **Tourpaq 5.2 is here** — This release brings major improvements to the Finance module, a redesigned Bookings grid, and full PBS clearing file support. Read the full release notes →
{% endhint %}

\| 📦 24 Updates | ✨ 9 New features | 🔧 11 Improvements | 🐛 4 Bug fixes |

&#x20;\|:-:|:-:|:-:|:-:|&#x20;

\| This quarter | `NEW` | `IMP` | `FIX` |

***

### Filters

### See all updates below.Filter view: NEWFilter view: IMPFilter view: FIXFilter view: INT---### 📅 May 202&#x36;**`NEW` — PBS clearing file — full field mapping** · _May 5, 2026_

The Finance module now exports a fully validated PBS clearing file using fixed-width ASCII layout. Includes all 17 field definitions, integrity checks, and a downloadable format reference.

🏦 `Finance`

{% hint style="success" %}
**`IMP` — Bookings grid — column resizing and sticky header** · _May 2, 2026_

Columns in the Bookings list are now resizable and the header row stays visible while scrolling through large datasets.

📋 `Bookings`
{% endhint %}

{% hint style="warning" %}
**`INT` — Stripe payment gateway integration** · _May 1, 2026_

Tourpaq now connects directly with Stripe for card-on-file and subscription payments. Configurable per creditor from the Integration settings panel.

💳 `Integrations`
{% endhint %}

\---

#### 📅 April 202&#x36;**`NEW` — Price list — season rule inheritance** · _Apr 18, 2026_

Price rules can now inherit from a parent season, reducing duplication for overlapping date ranges. A visual diff tool shows changes between child and parent.

🏷️ `Price list`

{% hint style="danger" %}
**`FIX` — Transport manifest — duplicate passenger entries** · _Apr 11, 2026_

Fixed a bug where passengers with multiple booking references appeared twice on the transport manifest PDF export.

🚌 `Transport`
{% endhint %}

\---

#### 📅 March 202&#x36;**`IMP` — Hotel allotment — overbooking threshold control** · _Mar 24, 2026_

Admins can now set a per-hotel overbooking buffer (0–20%) from the Hotel settings screen. Previously required a support ticket to adjust.

🏨 `Hotels`

{% hint style="danger" %}
**`FIX` — Creditor invoices — wrong VAT rate on grouped lines** · _Mar 10, 2026_

VAT was calculated incorrectly when multiple invoice lines with different rates were grouped into a single creditor invoice. Now resolved.

🧾 `Finance`
{% endhint %}

← Load older updates

\#### Categories

|                 |        |
| --------------- | ------ |
| 📄 All updates  | **24** |
| ✨ New features  | **9**  |
| 🔧 Improvements | **11** |
| 💳 Integrations | **4**  |
| 🐛 Bug fixes    | **4**  |

***

**Popular modules**

|                |       |
| -------------- | ----- |
| 🏨 Hotels      | **6** |
| 📋 Bookings    | **5** |
| 🚌 Transport   | **4** |
| 🏦 Finance     | **5** |
| 🏷️ Price list | **4** |

***

**Legend**

| Badge | Meaning     |
| ----- | ----------- |
| `NEW` | New feature |
| `IMP` | Improvement |
| `FIX` | Bug fix     |
| `INT` | Integration |

\---

{% hint style="info" %}
🎧 **Need help?**

Can't find a feature or spotted a bug?

[Contact support →](mailto:support@tourpaq.com)
{% endhint %}
