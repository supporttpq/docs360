# Notes

### Overview

The **Notes** tab is an internal log for a single **Real Transport** route.\
Use it to capture decisions, exceptions, and short-lived operational context.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Purpose

* Keep a lightweight audit trail for day-to-day operations.
* Share context between colleagues working the same route.

{% hint style="info" %}
Notes are internal. They are not shown to customers or external agents.
{% endhint %}

### Fields

* **Internal notes**: Free-text area for rapid documentation.\
  Treat the default placeholder text as a prompt to add real content.
* Use Notes to explain _why_ something changed for the transport.

### Working standards

When writing notes for a Real Transport route, follow these standards:

1. **Check before acting**\
   Before changing departures, rules, or passenger requirements, scan the latest notes first.
2. **Document operational events**\
   Use short, scannable bullets. Include details that help someone act fast.
   * Airport or handling issues (delays, local constraints, ground handling changes).
   * Supplier changes (times, flight numbers, seat allocation, cost inputs).
   * Rule interactions (what changed, and which rule(s) it affects).
   * Testing notes (what was tested and the outcome).
3. **Use a consistent format**\
   Start each entry with a date and initials. Add a one-line summary.

{% code title="Recommended note format" %}
```
2026-01-26 - AB - Supplier confirmed new departure time +15 min.
- Applied to departures from 2026-02-01.
- Flight change queued and sent.
```
{% endcode %}

### FAQ

#### Who can see Notes?

Notes are intended for internal users working in Tourpaq Office.\
They are route-specific and live with the Real Transport record.

#### Do Notes affect pricing, availability, or booking logic?

No. Notes do not change system behavior by themselves.\
They document the reason behind changes made elsewhere.

#### Are Notes shown to passengers or printed on tickets?

No. Use **Passenger Information** for messages that passengers must see.\
Use Notes for internal context only.

#### What should I write when I make a departure change?

Write the **what**, **why**, and **scope**:

* What changed (time, flight number, seats, supplier, costs).
* Why it changed (supplier request, GDS mismatch, operational issue).
* Scope (date range, affected brands, whether flight change was queued/sent).

#### Should I delete old notes?

Usually no. Old notes are valuable as an audit trail.\
If the list gets noisy, add a closing line like “Resolved” with a date.
