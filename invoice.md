---
description: Invoice listing
---

# Invoice

### Invoice dashboard (Invoice list)

Use the **Invoice** page to find invoices, check where they are in the process (pending/approved/rejected), and download or take actions like **archive** or **pay**.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### What you can do here

* **Search and filter** invoices by date range, invoice number, creditor, status, and more.
* **Open an invoice** from the list.
* **Download** invoice files (PDF / XML) and related **accounting** exports.
* **Archive** invoices to remove them from your day-to-day view.
* **Pay** invoices (if your user role has access).

{% hint style="info" %}
What you can see and do may depend on your permissions. If you don’t see **Pay** or download options, ask your admin to confirm your role.
{% endhint %}

### Step-by-step: find an invoice

{% stepper %}
{% step %}
### 1) Choose a date range

Set **From date** and **To date** to control which invoices appear in the list.

* If you can’t find an invoice, widen the date range first.
{% endstep %}

{% step %}
### 2) Add optional filters (if needed)

Use one or more of these filters to narrow the results:

* **Invoice Number**: search for a specific invoice ID/number.
* **Creditor**: filter by supplier/service provider.
* **Status**: show only **Pending**, **Approved**, or **Rejected** invoices.
* **Archive Status**: show **Archived** or **Not archived** invoices.
* **Internal Comment**: search by internal notes/tags.
{% endstep %}

{% step %}
### 3) Display results

Select **Display** to apply your filters.

* Select **Clear** to reset all filters and start over.
{% endstep %}

{% step %}
### 4) Open the invoice

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

### FAQs

* **I can’t find an invoice I know exists. What should I do?**\
  Start by widening the **From date** / **To date** range. Then try searching by **Invoice Number** or **Creditor**.
* **What’s the difference between “Due date” and “App. due date”?**\
  **Due date** is when payment is due. **App. due date** is when the invoice was approved/registered in the system.
* **Why is an invoice “Rejected”?**\
  Rejected invoices usually have missing/incorrect details or need clarification. Open the invoice and check **Comments** for the reason and next steps.
* **Where do I download the invoice PDF or XML?**\
  Use **Download Invoice PDF** or **Download Invoice XML** in the invoice tools or directly in the invoice row (depending on your view and permissions).
* **What does “Archived” mean?**\
  Archived invoices are hidden from the default working list but are still available. Use **Archive Status** to show them again.
* **Can I archive or pay multiple invoices at once?**\
  You can select multiple invoices using the **checkboxes** and then run the available bulk action (for example **Archive**). Bulk **Pay** depends on your setup and permissions.
* **I don’t see the Pay/Download options. Is something wrong?**\
  Not necessarily—those actions can be permission-based. Ask your admin to confirm your role and access rights.
