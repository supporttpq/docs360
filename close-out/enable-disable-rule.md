# Enable / Disable rule

### Overview

Close Out rules control **Free Hotel Allotment (FHA)** in price lists. When a matching rule is enabled, the system sets FHA to `0`. When the rule is disabled, the system restores FHA from the **current hotel configuration**.

Use this when you need to stop sales fast. Typical cases are capacity limits and operational stop sales.

{% hint style="info" %}
Changes are applied asynchronously. Allow up to \~2 minutes for price lists to update.
{% endhint %}

### Enable a rule

When you select **Enabled** and click **Save**:

* The rule becomes active.
* Backend services update affected Price List Tables (PLTAs).
* FHA is set to `0` for all matched hotel/room combinations.

#### Examples

1. **Rule set on transport + resort**
   * All PLTAs in the rule period, created with that transport and resort hotels, get FHA = `0`.
2. **Rule set only on a resort (no transport)**
   * All PLTAs in the rule period, created with that resort’s hotels and **all transports**, get FHA = `0`.

### Disable a rule

When you clear **Enabled** and click **Save**:

* The rule becomes inactive.
* The Stop Sale Resort service recalculates FHA on affected PLTAs.
* FHA is restored to the free allotment defined in the hotel setup.

#### Examples

1. **Rule set on transport + resort**
   * All PLTAs in the rule period, created with that transport and resort hotels, get FHA restored from the hotel/room setup.
2. **Rule set only on a resort (no transport)**
   * All PLTAs in the rule period, created with that resort’s hotels and **all transports**, get FHA restored from the hotel/room setup.

### Key notes

* Disabling a rule does **not** restore “what it was before”. It restores whatever is configured now in the hotel setup.
* Use a narrow scope when possible. Wide rules can block sales across many price lists.

### Related tasks

* [Close Out](./)
* [Create / Edit rule](create-edit-rule.md)
