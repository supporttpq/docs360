---
description: >-
  Auto-generate supplier invoices in Tourpaq Office from cost data and billing
  schedules. Suppliers approve by email. Track invoices in Finance → Invoice.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Autobilling

### Overview

**Autobilling** automatically generates **supplier invoices** in Tourpaq Office.

It uses your configured **billing schedules** and the **cost data** stored on bookings, hotels, extras, and supplements. This reduces manual invoicing and supports consistent finance workflows.

### Automated invoice generation

Tourpaq generates invoices for the following components:

* **Hotel Deposit Invoice**
* **Hotel Early Booking Invoice**
* **Hotel Invoice**
* **Extra Invoice**
* **Extra Early Booking Invoice**
* **Transfer Invoice**
* **Discount/Supplement Invoice**
* **Handling Invoice**

These invoices are generated based on configured billing schedules and use the cost values stored in the system for each relevant item (e.g., hotels, extras, supplements).

***

### Invoice approval workflow

Once an invoice is generated:

1. The **creditor/supplier** receives an **email** with a link to review the proposed invoice.
2. By accessing the link, the creditor can **approve or reject** the invoice directly.
3. This creates a clear audit trail for invoice approval and changes.

***

### Viewing generated invoices

All generated invoices are available in **Finance → Invoice**.

See [Invoice](../invoice.md).

For each invoice, the following information is displayed:

* **Invoice Number**
* **Invoice Type**
* **Invoice Name**
* **Creditor Name**
* **Internal Comment**
* **Amount**
* **Approved Due Date**
* **Download Option** (PDF format)

{% hint style="info" %}
Autobilling uses supplier/creditor configuration. If a creditor is missing, create it first (see the Autobilling subpages).
{% endhint %}
