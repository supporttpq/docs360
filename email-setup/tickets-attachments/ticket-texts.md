---
description: Add and manage reusable text blocks that are printed on customer tickets.
---

# Ticket texts

### Overview

Ticket texts are reusable text blocks that can be printed on customer tickets. They appear only when a booking matches the rules you set.

Use ticket texts for terms and conditions, fees, or short instructions. They help you keep tickets consistent.

### Access

* Path: **E-mail Setup → Ticket Attachments → Ticket texts**

### What ticket texts do

Ticket texts help you:

* Give customers clear information on the ticket.
* Show different texts for different bookings.
* Avoid rewriting the same message over and over.

### What you can do on this page

From this page you can:

* Create a new ticket text.
* Edit an existing ticket text.
* Delete ticket texts you no longer use.

### Ticket text fields

Each ticket text entry contains the following fields:

* **Text type** – What the text is for (for example, information or terms).
* **Identification code** – A short code that helps you find the text later.
* **Date interval** – Start and end dates for when the text can be used.
* **Text content** – The message that will be printed on the ticket.

### Typical setup (step-by-step)

{% stepper %}
{% step %}
#### 1. Create a new ticket text

Choose to add a new ticket text on the page.
{% endstep %}

{% step %}
#### 2. Fill in the basic fields

Set the text type, an identification code, and the date interval. Write the text content in plain language.
{% endstep %}

{% step %}
#### 3. Choose when it should appear

Select the rules that decide when the text is printed. Typical rules are booking dates, product, or room type.
{% endstep %}

{% step %}
#### 4. Save and test

Create a sample booking that should match the rules. Generate the ticket and confirm the text is printed.
{% endstep %}
{% endstepper %}

### Example

* You want to add a note about a seasonal resort fee.
* Create a ticket text for the summer dates.
* Link it to the right product or room type.
* The ticket will show the note only for matching bookings.

### Best practices

{% hint style="info" %}
When you create ticket texts:

* **Keep it short**. Use plain language.
* **Reuse existing texts** where possible.
* **Use clear codes** that explain the purpose (for example, `SUMMER_FEE_2026`).
* **Review dates** so outdated texts do not stay active.
* **Test with a sample booking** before you rely on it.
* **Avoid editing older texts** if you need a new version. Create a new text with a new date interval instead.
{% endhint %}

### FAQ

<details>

<summary>Where will the ticket text appear?</summary>

It appears on the customer ticket. It is printed only when the booking matches your rules.

</details>

<details>

<summary>Why is my ticket text not showing up?</summary>

Check the date interval first. Then check that the booking matches the conditions you selected. Finally, generate the ticket again to test.

</details>

<details>

<summary>Can I use more than one ticket text on the same ticket?</summary>

Yes, if the booking matches more than one set of rules. Test with a sample booking to confirm the result.

</details>

<details>

<summary>Do changes affect tickets that were already sent?</summary>

No. Already sent tickets do not change. Re-send the ticket to include your updated text.

</details>

<details>

<summary>Should I delete old ticket texts?</summary>

Delete them if you are sure they are no longer needed. If you might need them later, shorten the date interval instead.

</details>
