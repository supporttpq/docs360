---
description: >-
  This page allows users to monitor and manage SMS sent to customers. Here, they
  can check details about the messages sent, the sending period, their status,
  and other relevant information.
---

# Ticket texts

### **Overview**

On this page, administrators can configure **ticket texts** – reusable pieces of text that are automatically printed on customer tickets when the booking meets certain conditions.

Use ticket texts for things like legal information, special conditions, extra fees, or important instructions that must always appear on specific types of tickets.

### **Purpose**

Ticket texts help you:

* Provide customers with **clear written information** directly on their tickets (e.g. terms, conditions, extra charges).
* Allow agencies to **customize printed tickets** based on defined booking conditions (such as booking period, product, or room type).
* Maintain **consistent and accurate communication** across all tickets, without having to rewrite the same messages each time.

### **Administrator capabilities**

From this page, administrators can:

* **Use an existing text template** – Apply a predefined ticket text to the relevant bookings.
* **Edit an existing text** – Update the content, valid dates, or conditions for an existing ticket text.
* **Insert a new text** – Create and configure a new ticket text to be included on tickets.
* **Delete a text** – Remove texts that are no longer needed or valid.

### **Ticket text attributes**

Each ticket text entry contains the following fields:

* **Text type** – The category or purpose of the text (for example: information, terms & conditions, cancellation rules, special fees).
* **Identification code** – An internal code used to identify or reference this text. This helps distinguish it from other texts with similar content.
* **Date interval** – The start and end dates that define when this text is active. The text will only be printed on tickets for bookings within this date range.
* **Text content** – The actual message that will appear on the printed ticket.

### **Usage example**

* A hotel agency wants to add a note about **seasonal resort fees** that only applies during the summer.
* The administrator creates a new ticket text, sets the **date interval** to cover the summer season, links it to the relevant **room type** or product, and writes a short explanatory message.
* For any booking that matches those conditions (date range and room type), the system automatically includes this message on the printed ticket.

### **Best practices for ticket texts**

{% hint style="info" %}
When creating ticket texts, keep the following recommendations in mind:

* **Be concise and clear** – Use simple language and keep the text as short as possible while still being precise.
* **Avoid duplication** – Reuse existing ticket texts where you can, instead of creating very similar new ones.
* **Use meaningful identification codes** – Choose codes that make it easy to understand the purpose of the text (for example: `SUMMER_FEE_2025`).
* **Review dates regularly** – Periodically check date intervals so that outdated texts are either updated or deleted.
* **Test before going live** – Always test with a sample booking to ensure the text appears on the right tickets and under the correct conditions.
{% endhint %}
