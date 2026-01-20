# Rules - Hotel Contract Configuration

### Overview

Use the **Rules** tab to attach contractual conditions to a hotel contract.

Rules typically cover booking constraints, supplier policies, and other terms that do not belong in pricing or availability.

{% hint style="info" %}
Use **Rules** for reusable contract terms. Use **Remarks** for one-off text printed in the Contract PDF.
{% endhint %}

***

### Screenshot

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

* The hotel contract exists and is open for editing.
* The rule definitions are available in **Hotel → Hotel Contract Rules**.

***

### Structure

The tab has two areas:

* **Overview**: Shows the rules already attached to the contract.
  * **No**: Line number.
  * **Type**: Rule category (for example _General Condition_ or _Remarks_).
  * **Rule Text**: The full text of the rule.
* **Edit**: Add, remove, or update rules for this contract.

***

### How to add rules

{% stepper %}
{% step %}
### Maintain the rule definitions

Go to **Hotel → Hotel Contract Rules**.

Create a new rule or update an existing one.
{% endstep %}

{% step %}
### Attach the rule to the contract

Open the hotel contract.

Go to **Rules**.

Add the rule and save the contract.
{% endstep %}
{% endstepper %}

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Tips

* Keep rule text short and specific.
* Use consistent **Type** values. It helps sorting and review.
* Review rules before you export or share contract documents.

***

### Related workflows

* [Remarks - Hotel Contract Configuration](remarks-hotel-contract-configuration.md): Add printable text to the Contract PDF.
* [Hotel contract - General](hotel-contract-general.md): Create and manage the contract header.

***

### FAQ

**What’s the difference between Rules and Remarks?**\
Use **Rules** for contract terms you want to maintain as rules.\
Use **Remarks** for optional free text that prints in the Contract PDF.

**Can I add more than one rule to a contract?**\
Yes. Add as many rules as needed.

**Where do I create and edit rule texts?**\
Use **Hotel → Hotel Contract Rules** to maintain the rule definitions.

**If I update a rule definition, does it change existing contracts?**\
It can. If the same rule is reused, updates may show everywhere it’s used.\
If you need contract-specific wording, create a separate rule.
