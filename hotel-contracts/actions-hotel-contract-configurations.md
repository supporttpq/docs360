# Actions - Hotel Contract Configurations

### Overview

The **Actions** tab lets you run **contract-level bulk actions**. You can reimport specific contract sections, export the contract, or send it to suppliers. It improves workflow efficiency by reducing the need to update each tab manually.

***

<figure><img src="../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### What you can do here

* Reimport selected contract sections without rebuilding the whole contract.
* Export the contract to PDF.
* Send the contract by email to the supplier for acceptance or rejection.

### Preconditions

* A contract must be saved and assigned to a supplier.
* The contract must be eligible for import.
* The user must have access rights to hotel contract administration and importing.

***

### Import tab

Use this tab to reimport selected sections. Only the selected sections are updated.

#### Sections available for reimport

| Section                      | Description                                                   |
| ---------------------------- | ------------------------------------------------------------- |
| **Hotel Allotment**          | Reimports allotments for each period and room type.           |
| **Room Cost**                | Updates room cost per period.                                 |
| **Stay & Pay**               | Reimports stay/pay deals (for example “Stay 7, Pay 6”).       |
| **Early Booking**            | Reimports early booking discount rules.                       |
| **Cut Down Hotel Allotment** | Applies reductions to predefined allotments.                  |
| **Extra Bed Cost**           | Syncs prices for additional beds.                             |
| **Extra Cost Rule**          | Reimports extra cost rules.                                   |
| **Release**                  | Updates release rules (for example lead time before booking). |
| **Board Supplements**        | Imports supplements like Half Board or Full Board.            |
| **Gala Dinner**              | Reimports gala dinner rules.                                  |
| **Deposits**                 | Imports deposit payment structure.                            |
| **Facilities**               | Imports facilities (e.g., Wi-Fi, Pool, Parking).              |

#### Run a reimport

{% stepper %}
{% step %}
### Select sections

Tick the sections you want to refresh.
{% endstep %}

{% step %}
### Start the reimport

Click **Reimport Hotel Contract**.
{% endstep %}

{% step %}
### Verify the result

Check the relevant tabs after the reimport. Focus on **Rooms**, **Periods**, and **Costs**.
{% endstep %}
{% endstepper %}

***

### Related Workflows

* **Initial Import:** When a new hotel contract is added and the import from an external file (XML, XLSX, or API) is performed.
* **Data Correction:** When the source data changes and you want to sync updates without deleting the contract.
* **Partial Update:** After a new season is added, only room costs or allotments may be updated using this screen.

***

#### Notes

* This does **not** delete data you do not select.
* Selected sections are updated/replaced.
* Always verify results after reimport, especially in the **Rooms**, **Periods**, and **Costs** tabs.
* A confirmation will appear if unsaved changes exist on the contract.

<figure><img src="../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Share tab

Use this tab to share the contract with external recipients.

* **Export hotel contract (PDF)**: Exports the contract as a PDF file.
* **Send email**: Sends the contract to the supplier. You can add multiple email addresses. The supplier can accept or reject the contract.

<figure><img src="../.gitbook/assets/image (11) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
To use **Send email**, you must create an email template for **Hotel Contract**. Otherwise, the system shows a warning.
{% endhint %}

### Save a hotel contract without product details

During hotel contract negotiations, certain information may not yet be available (e.g., board codes, product names, or supplements). The system lets you save a hotel contract without providing these details immediately. However, the data must be complete at import time to ensure accuracy and consistency.

#### Why this exists

Contract creation stays flexible. Validation happens in two stages.

1. **Save-level validation** → Allows saving contracts even when some fields are unknown.
2. **Import-level validation** → Ensures all mandatory fields are present before the contract is imported and made operational.

This approach enables contract staff to store draft agreements without blocking their workflow while maintaining strict data quality at import.

#### Functional Requirements

1. **Validation Levels**
   * Save-level: Minimal validation, allowing optional fields to remain empty.
   * Import-level: Strict validation applied before importing the contract.
2. **Fields validated at import only (Board tab):**
   * **Extra Category** → Mandatory only for import.
   * **Product** → Mandatory only for import.
   * **Name** → Mandatory only for import.
   * **Code** → Mandatory only for import.
3. **PDF Export**
   * When generating the PDF, the system will use the _List Name_ from the Board Types for board references.
   * This ensures independence from individual naming conventions.
4. **Contract Staff Actions**
   * **Send email** and **Export to PDF** remain available even if optional data is missing.

### Next steps

* Verify rooms in [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md).
* Verify periods and seasonal setup in [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md).
* Review general contract settings in [Hotel contract - General](hotel-contract-general.md).

### FAQ

**Does reimport delete existing data?**\
No. Data you do not select stays unchanged.\
Selected sections are updated/replaced.

**Can I reimport if I have unsaved changes?**\
You’ll get a confirmation prompt.\
Save first when possible.

**Why can’t I use “Send email” in the Share tab?**\
You are missing the **Hotel Contract** email template, or you lack permissions.\
Create the template, then try again.

**What does the supplier receive by email?**\
A contract email with an accept/reject option.\
It does not give the supplier edit access in Tourpaq.

**When should I save without product details?**\
During negotiation, when board codes/products are not final.\
Complete the data before import.
