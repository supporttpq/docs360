---
description: Add internal notes to a transport rule for context and traceability.
---

# Notes

### Overview

Use the **Notes** tab to document why a transport rule was changed.

Keep notes short and searchable.

{% hint style="info" %}
Notes are internal. They are not shown to customers or external agents.
{% endhint %}

### Field: Internal notes

<figure><img src="../.gitbook/assets/image (584).png" alt=""><figcaption></figcaption></figure>

This is a free-text field for your team.

#### What to write

* **Change log:** what changed and why.
  * Example: `2026-01-26 CP: Increased quota by 10% for the summer peak.`
* **Decisions:** why you picked a specific setup or naming.
* **Operational context:** known issues, workarounds, or handover notes.

#### What not to write

* Customer-facing messages.
* Personal data that is not required for operations.

### Best practices

1. **Date and sign** notes (ISO date + initials).
2. **Keep it scannable.** Use bullets. Avoid long paragraphs.
3. **Keep it current.** Remove outdated context.

### FAQ

<details>

<summary>Are Notes visible to customers?</summary>

No. Notes are internal and only visible to users with access to transport rules.

</details>

<details>

<summary>Who can read Notes?</summary>

Anyone who can access the transport rule can read its Notes.

</details>

<details>

<summary>Should I use Notes as an audit log?</summary>

Use Notes for quick context. Do not rely on them as a full audit trail.

</details>

<details>

<summary>What’s a good Notes format?</summary>

Start with a date and initials, then add one sentence.

Example: `2026-01-26 CP: Renamed rule to match the naming standard.`

</details>

### Related pages

* [Create Transport Rule](create-transport-rule.md)
* [Edit Transport Rule](edit-transport-rule.md)
