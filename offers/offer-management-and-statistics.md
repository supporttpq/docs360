# Offer management and statistics

### Overview

After you **send** an offer, Tourpaq automatically tracks two key dates:

* **Expiration date**: how long the offer stays valid for the customer
* **Follow-up date**: when the agent should follow up

These dates make it easier to manage your sales pipeline and ensure no offers are forgotten.

<figure><img src="../.gitbook/assets/image (267).png" alt="Offer follow-up and expiration dates"><figcaption><p>Offers include follow-up and expiration dates after they are sent.</p></figcaption></figure>

***

### Purpose

Use offer management to:

* Keep control of offers that are **about to expire** or need **follow-up**
* Convert accepted offers into **bookings**
* Close offers with a **close reason** when they will not be converted
* Export offers for reporting and review
* Review **statistics** per sales agent (sent offers + success rate)

***

### Before you start

* You need access to the **Offers** module.
* Offers must be **sent** before expiration/follow-up timing becomes relevant.

Related pages:

* [Offers](./)
* [Create new offer](create-new-offer.md)

***

### Key concepts

#### Offer expiration (availability)

An offer is typically available for a limited number of days after it is sent. When the offer reaches the end of that period, it can become **expired**.

#### Offer follow-up

The follow-up date is the internal “reminder” date for the agent/team to contact the customer.

{% hint style="info" %}
Expiration is for the **customer** (how long the offer is valid). Follow-up is for the **sales process** (when you should contact them).
{% endhint %}

***

### Configure default follow-up and expiration timing

Your company setup can define default values used when offers are sent:

* **Default offer availability days**
* **Default offer follow-up days**

<figure><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Default offer availability days and follow-up days"><figcaption><p>Default offer availability and follow-up settings in company setup.</p></figcaption></figure>

{% hint style="warning" %}
If you don’t have permission to change these defaults, ask your system administrator.
{% endhint %}

***

### What happens after an offer is sent

When you send an offer:

* Tourpaq sets the **expiration date** and **follow-up date** automatically.
* You can usually **adjust** these dates manually on the offer if needed.
* Offers near their **follow-up** or **expiration** date can appear on the **Tourpaq dashboard**, making them easier to act on.

The typical end result of an offer is one of the following:

* **Converted to a booking** (success)
* **Closed** with a close reason (no sale)

***

### Convert an offer into a booking

There are typically two ways an offer becomes a booking:

1. **Customer self-booking**: the customer uses the booking link/button in the offer email (if enabled in your setup).
2. **Agent-created booking**: the sales agent creates the booking in Tourpaq Office.

<figure><img src="../.gitbook/assets/image (268).png" alt="Offer converted to booking"><figcaption><p>When converted, the booking is created with customer, transport, and hotel details prefilled.</p></figcaption></figure>

When the offer is converted:

* The booking is created with transport/hotel and customer information prefilled.
* The offer no longer needs follow-up and typically disappears from dashboard reminders.

***

### Manage offers (filters and export)

On the Offers management page, you can filter offers by common criteria such as:

* Customer name or email
* Customer type (customer vs offeree)
* Offer status (available, expired, sold, closed, etc.)
* Close reason (for closed offers)
* Follow-up period
* Create period

For detailed filter explanations, see [Offers](./).

#### Export offers

Exporting offers is useful for reporting and analysis outside Tourpaq (for example in Excel).

<figure><img src="../.gitbook/assets/image (269).png" alt="Export offers menu"><figcaption><p>Export is available from the menu on the Offers page.</p></figcaption></figure>

{% stepper %}
{% step %}
### 1) Open the Offers page

Go to the Offers module and make sure you see the offers list.
{% endstep %}

{% step %}
### 2) Apply filters (optional)

If you only want to export a subset (for example a specific period or a specific agent), apply filters first.
{% endstep %}

{% step %}
### 3) Export

Open the menu (three dots) and select **Export**.
{% endstep %}

{% step %}
### 4) Save the file

The system generates a file based on your current filter results.
{% endstep %}
{% endstepper %}

<figure><img src="../.gitbook/assets/image (6) (1) (1) (3) (1) (1).png" alt="Example exported offers list"><figcaption><p>Example of exported offer data.</p></figcaption></figure>

{% hint style="info" %}
If no filters are applied, the export typically includes **all** offers that are visible to you.
{% endhint %}

***

### Offer statistics

Use the Statistics view to track performance per sales agent.

To open it:

1. Go to [Offers](./)
2. Switch from **Offers** to **Statistics**

You will typically see:

* **Sent offers** (not drafts/unsent)
* **Success rate** (conversion performance)

<figure><img src="../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Offer statistics"><figcaption><p>Statistics view showing sent offers and success rate per sales agent.</p></figcaption></figure>
