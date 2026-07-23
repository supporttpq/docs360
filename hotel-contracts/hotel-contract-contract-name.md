# Hotel contract - Contract Name

### Overview

The **Contract Name** page is where you create and maintain a hotel contract. You define contract terms, validity periods, pricing rules, and any extra costs.

### What you configure here

Use this page to define:

* General hotel and contract information
* Room definitions (via the **Rooms** tab)
* Contract periods and seasonal pricing (via the **Periods** tab)
* Supplements and discounts
* Additional costs and services

### Preconditions

Before you create or edit a contract:

* The hotel and supplier already exist, or you create them during this flow.
* The user must have editing rights.
* You have key contract details ready (creditor, contract type, and validity dates).

### Screenshot

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Tabs available

* **General**: Hotel and contract information (default tab).
* **Rooms** and **Periods**: Define room types and contract periods.
* Other tabs (for example `Board Supplements`, `Extra Beds`, `Early Booking`, `Stay & Pay`) let you configure rules in detail.

***

### General tab

The General tab is split into a left panel (**Hotel**) and a right panel (**Contract**).

#### Hotel section (left panel)

* **Hotel**: Select an existing hotel, or choose _Create new_.
* **Name**: Internal hotel name.
* **Address**, **Phone**, **Email**: Hotel contact details.
* **Release Email**: Email address used for release-related communication.
* **Resort**: Resort/destination for the hotel.
* **Rating**: Hotel rating.
* **Supplier**: Supplier account linked to the hotel.
* **Code**: Internal hotel code.
* **Web**: Optional website link.

#### Contract section (right panel)

* **Name**: Contract name (often matches the hotel name).
* **Creditor**: Financial creditor for invoicing and settlement.
* **Date Start / End**: Contract validity period.
* **Contract Type**: Contract type (for example allotment or guarantee).
* **Child Price Age**: Age range used for child pricing.
* **Child Ages for Extra Beds**: Age range eligible for extra bed pricing/discounts.
* **Auto Billing**: Enable if automatic invoicing should apply.
* **Combine E.B. with S\&P**: Enable if Early Booking and Stay & Pay should be evaluated together.

{% hint style="info" %}
Unsure about **Contract Type** or **Creditor**? Check with finance first. These fields affect reporting and invoicing flows.
{% endhint %}

### Next steps

* Configure room types in [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md).
* Configure periods, allotments, and costs in [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md).
