---
description: >-
  Manage supplier invoices in Tourpaq Office Finance. Search and filter the
  invoice list, download invoice PDF/XML and accounting files, archive invoices,
  and pay invoices (permissions required).
---

# Invoice

### Invoice dashboard (invoice list)

Use the **Invoice** page to find supplier invoices, check status (**Pending**, **Approved**, **Rejected**), and take actions like **download**, **archive**, or **pay**.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (6).png" alt="Invoice list with filters and status columns"><figcaption><p>Invoice list: filter by date range, invoice number, creditor, and status. Then download, archive, or pay invoices.</p></figcaption></figure>

### What you can do here

* **Search and filter** invoices by date range, invoice number, creditor, status, and more.
* **Open an invoice** from the list.
* **Download** invoice files (PDF/XML) and related **accounting** exports.
* **Archive** invoices to remove them from your day-to-day view.
* **Pay** invoices (if your user role has access).

{% hint style="info" %}
What you can see and do may depend on your permissions. If you don’t see **Pay** or download options, ask your admin to confirm your role.
{% endhint %}

### Step-by-step: find an invoice

{% stepper %}
{% step %}
**1) Choose a date range**

Set **From date** and **To date** to control which invoices appear in the list.

* If you can’t find an invoice, widen the date range first.
{% endstep %}

{% step %}
**2) Add optional filters (if needed)**

Use one or more of these filters to narrow the results:

* **Invoice Number**: search for a specific invoice ID/number.
* **Creditor**: filter by supplier/service provider.
* **Status**: show only **Pending**, **Approved**, or **Rejected** invoices.
* **Archive Status**: show **Archived** or **Not archived** invoices.
* **Internal Comment**: search by internal notes/tags.
{% endstep %}

{% step %}
**3) Display results**

Select **Display** to apply your filters.

* Select **Clear** to reset all filters and start over.
{% endstep %}

{% step %}
**4) Open the invoice**

In the results table, select the invoice number in **INV.NO** to open it.
{% endstep %}
{% endstepper %}

### Understanding the invoice list

Each row is one invoice. Common fields you’ll use:

* **INV.NO**: The invoice number (usually a link).
* **TYPE**: What kind of invoice it is (for example: hotel invoice, handling invoice, extra invoice).
* **NAME**: Short description (often includes supplier + date).
* **CREDITOR**: Who the invoice is from.
* **INT.COMM**: Internal comment/tag (your team’s internal reference).
* **AMOUNT**: Invoice total.
* **DUE DATE**: When payment is due.
* **APP. DUE DATE**: The date the invoice was approved/registered in the system.
* **STATUS**:
  * **Pending**: not approved yet
  * **Approved**: approved and ready for the next step
  * **Rejected**: rejected (usually needs correction or follow-up)
* **COMMENTS**: View notes and discussion related to the invoice.
* **ARCHIVED**: Shows whether the invoice is archived.

### Download files (PDF, XML, accounting)

Depending on the invoice and your permissions, you may see download options in the row or in the invoice tools.

* **Download Invoice PDF**: downloads a printable PDF copy.
* **Download Invoice XML**: downloads the invoice in XML format.
* **Download Accounting**: downloads the accounting export/record linked to the invoice.

{% hint style="warning" %}
If a download is missing or empty, confirm the invoice has the expected attachments and that you are allowed to access them.
{% endhint %}

### Archive invoices

Archiving helps keep your day-to-day invoice list clean.

* To archive a single invoice, use **Archive** on that invoice.
* To archive multiple invoices, use the **checkboxes** to select several rows (bulk actions), then choose **Archive**.

{% hint style="info" %}
To view archived invoices later, change **Archive Status** to show archived items.
{% endhint %}

### Pay invoices

If your role allows it, you can select **Pay** for an invoice.

* Use this when you are ready to send the invoice to your payment process.
* If **Pay** is not available, the invoice may need approval first (check **Status**) or you may not have permission.
