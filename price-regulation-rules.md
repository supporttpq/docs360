---
description: >-
  Configure Tourpaq Office price regulation rules for automatic repricing.
  Adjust prices up/down by hours and offer count. Set lowest price limits and
  audit in price list history.
---

# Price regulation rules

## Overview

A **Price Regulation Rule** controls **automatic repricing** in Tourpaq Office.

It can increase or decrease prices based on:

* Time passed (**hours**)
* Demand (**number of offers**)
* Guard rails (**lowest price** limits)

Use this to keep pricing competitive without dropping below your minimum price.

## Purpose

The purpose of this rule is to:

* Automate price increases or decreases for offers.
* Control how often and by how much a price can change.
* Ensure prices never go below defined minimum thresholds.
* Reduce manual intervention when managing multiple offers.

## Preconditions

* The user must have permissions to create or edit price regulation rules.
* A valid **Name** and **Code** must be provided.
* Agree on pricing rules (amounts, hours, offer thresholds, and minimum prices) before setup.

<figure><img src=".gitbook/assets/image (52) (1).png" alt=""><figcaption></figcaption></figure>

## Create or edit a rule

1. Navigate to **Price Regulation Rules** in the system and select **Create/Edit Rule**.
2. Fill in the fields below.

### Fields

All `*` fields are required.

* **Name \***: Clear rule name. Example: `Weekend Repricing`.
* **Code \***: Unique code for the rule.
* **Amount \***: Amount to add when prices go **up**.
* **Amount (down)**: Amount to subtract when prices go **down**.
* **Hours number**: Hours between “go up” adjustments.
* **Hours number (down)**: Hours between “go down” adjustments.
* **Offers number**: Offer count required before applying the “go up” amount.
* **Offers number (down)**: Offer count required before applying the “go down” amount.
* **Lowest price / Lowest price2 / Lowest price3 / Lowest price4**:
  * Minimum price limits. The system will not price below these values.
  * Typically used to protect different intervals (P1–P4) or scenarios.

3. After filling in the details:
   * Review all minimum price values carefully to prevent underpricing.
   * Save the rule.
4. The rule will now automatically regulate prices based on the defined triggers (time, offers, and limits).

### Best practices

* Always set realistic **Lowest price** values to avoid unprofitable sales.
* Use **Hours number** carefully—too small values may cause frequent price changes.
* Use consistent naming in **Name** so rules are searchable.
* Double-check both **Amount** and **Amount (down)** to ensure they follow company pricing policies.

{% hint style="warning" %}
When a price regulation rule is active, **price list history** is updated automatically.

You can see that a service ran each time prices were adjusted according to the configured rule.

The feature that enables **price list go up / go down limits** must be configured in [System Setup](setup/system-setup/).

<img src=".gitbook/assets/image (349).png" alt="" data-size="original">
{% endhint %}

### Apply the rule in a price list

After you enable the feature and the service is running:

1. Open **Price List**.
2. Select the **transport**, **hotel**, and **room type**.
3. Click **Display**.
4. In the grid, set the rule in the **PL. REG. RULE.** column.
5. Click **Save**.

<figure><img src=".gitbook/assets/image (53) (1).png" alt=""><figcaption></figcaption></figure>

### **FAQ**

1. **What is a price regulation rule?**\
   A price regulation rule is a set of conditions that tells Tourpaq Office when to automatically raise or lower prices based on time and offer count, while protecting minimum price limits.
2. **Why do I need a code and a name for each rule?**\
   The name makes the rule easy to find. The code uniquely identifies it.
3. **What does “Hours number” mean?**\
   It is the number of hours between price adjustments.
4. **How do minimum price fields work?**\
   They define the lowest prices the system can set. Prices will not go below these limits.
5. **How often does a rule run?**\
   The service checks your conditions continuously. When the conditions are met, prices are adjusted.
6. **Can I prevent rules from lowering prices too much?**\
   Yes. Set **Lowest price** limits to protect against underpricing.
7. **Where do I see the price changes?**\
   In **price list history**, where automatic adjustments are logged with timestamps.
