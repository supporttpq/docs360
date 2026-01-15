# Remarks - Hotel Contract Configuration

### Overview

Use **Remarks** to add optional text to the exported **Contract PDF**.

Remarks are typically used for:

* Supplier-facing notes.
* Practical stay information (check-in rules, meal notes, etc.).
* Contract-specific clarifications that should print on the PDF.

{% hint style="info" %}
Keep Remarks short. Long blocks make the PDF harder to scan.
{% endhint %}

***

### Screenshot (where you edit Remarks)

<figure><img src="../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure>

***

### Screenshot (how it looks in the Contract PDF)

<figure><img src="../.gitbook/assets/image (390).png" alt=""><figcaption></figcaption></figure>

***

### How it works

{% stepper %}
{% step %}
### Add your text

Go to **Hotel Contract → Remarks**.

Enter your text in **Remarks**.
{% endstep %}

{% step %}
### Save the contract

Save the hotel contract to persist the Remarks text.
{% endstep %}

{% step %}
### Export the Contract PDF

Generate the Contract PDF.

The Remarks text prints in the **Remarks** section.
{% endstep %}
{% endstepper %}

### Notes (for internal use)

Use **Notes** for internal comments that should stay inside Tourpaq Office.

Notes are **not printed** in the Contract PDF.

If Notes exist, the Contract PDF shows a small indicator under **Remarks**:

* `[x] Internal notes`

This tells the reader to open the contract in Tourpaq to view the Notes.

<figure><img src="../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure>

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md): Where you create and maintain the full contract.
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md): Also contains internal-only Notes (but period-specific).

***

### FAQ

**Are Remarks required?**\
No. Remarks are optional.

**Who can see Remarks?**\
Anyone who reads the exported Contract PDF can see them.

**What’s the difference between Remarks and Notes?**\
Use **Remarks** for text that should print in the Contract PDF.\
Use **Notes** for internal-only comments in Tourpaq Office.

**Do Notes ever appear in the PDF?**\
Not the text itself. The PDF only shows the `[x] Internal notes` indicator.

**Why do I see `[x] Internal notes` in the PDF?**\
Someone added internal Notes on the contract. Open the contract to read them.

**Can I use Remarks for pricing or legal clauses?**\
Avoid it. Use contract rules and structured fields for anything enforceable.\
Use Remarks for short, human-readable context only.
