# Select text for Offers

### Overview

**Select text for Offers** is where you manage the **standard texts, images, and communication templates** used when sending offers to customers.

This is typically configured **per Brand**, so each brand can have its own logo, email header/footer, insurance texts, and reminder messages.

<figure><img src="../.gitbook/assets/image (272).png" alt="Select text for Offers / Select Offer settings"><figcaption></figcaption></figure>

***

### Where to find it

In most setups, you will find these settings under:

* **Brands → (select a Brand) → Select Offer**

{% hint style="info" %}
If you work with multiple brands, make sure you are editing the **correct Brand** before updating texts and images.
{% endhint %}

***

### What this setup affects

The content you configure here is reused in customer communication such as:

* **Offer emails** (including header/footer and general information text)
* **Offer reminder emails/SMS** (automatic follow-ups)
* Customer-facing sections in the offer like:
  * **Travel insurance / cancellation insurance information**
  * **Trip safety text**
  * **More experiences / optional add-ons text**

For an explanation of how offer layouts work, see [Offer template](offer-template.md).

***

### What you can configure

#### 1) Brand texts (standard content)

These texts help ensure your team writes consistent, professional messages across all offers.

Common fields include:

* **Mail subject** (default subject when sending an offer)
* **Mail header** (your greeting/introduction)
* **Mail footer** (signature, contact details, disclaimers)
* **General available product text** (general information shown with the offer)
* **Unavailability custom message** (shown if an option becomes unavailable)

{% hint style="info" %}
Keep the header/footer fairly stable. Consultants can still add a personal message when creating an offer.
{% endhint %}

#### 2) Placeholders (personalization)

Many text fields support placeholders (dynamic fields) so messages can be personalized automatically.

Examples you may see:

* `[CustomerFirstName]`
* `[DepartureDate]`
* `[OfferLink]`

{% hint style="warning" %}
Only supported placeholders will work. If a placeholder is written incorrectly (or not supported), it may appear as plain text in the email.
{% endhint %}

#### 3) Template images

Upload the images that are shown in your offer layout, for example:

* **Logo** (brand identity)
* **Trip safety image**
* **More experiences image**
* **Web banner / included image** (depends on your template)

{% hint style="warning" %}
Image support depends on your offer template. Some templates do not display all image types. If an image looks stretched or cropped, check the recommended sizes in the field tooltip and upload a correctly sized image.
{% endhint %}

#### 4) Close reasons (why an offer was closed)

Close reasons are used when an offer is closed manually or automatically.

Set these up so consultants can select a clear explanation, such as:

* Customer booked elsewhere
* No availability
* Price too high
* Customer did not respond

Add a short description per reason so reports and internal follow-up remain consistent.

#### 5) Insurance and informational texts

If your offer template shows insurance and information sections, you can maintain standard texts for:

* **Travel insurance**
* **Cancellation insurance**
* **Trip safety text**
* **More experiences text**

Use these fields for the content you want to be the same for all customers (policy notes, links, and legal/compliance wording).

#### 6) Reminder emails and SMS (automatic follow-up)

You can automate reminders so customers receive follow-ups without manual work.

Typical settings include:

* **Email reminder schedule days**
  * Enter multiple values separated by commas (example: `3,7,14,21`)
  * Each number is the day offset your system uses to send reminders (based on your configuration)
* **Enable auto schedule** (turns on automatic sending)
* **Enable auto schedule close** (closes the offer after the last scheduled reminder)
* **Mail reminder subject/body**
* **SMS reminder body**

To learn how the scheduler behaves after an offer is booked (for example, canceling remaining reminders), see [Customer offers automatic flow](customer-offer-automatic-flow.md).

#### 7) Display extra description (optional)

If enabled, Tourpaq can show a **custom description** for included price extras in the customer offer.

{% hint style="info" %}
This requires an offer template that supports extra descriptions. If nothing changes in the customer email, the template may not include that section.
{% endhint %}

***

### Recommended setup flow (for new installations)

{% stepper %}
{% step %}
### 1) Pick the Brand you are configuring

Confirm you are editing the correct brand before you change texts or upload images.
{% endstep %}

{% step %}
### 2) Upload images first

Upload your logo and any images used by your offer template, then preview the result to ensure nothing is cropped or stretched.
{% endstep %}

{% step %}
### 3) Add the standard offer texts

Fill in:

* Mail subject
* Mail header
* Mail footer
* General available product text

Use placeholders where relevant.
{% endstep %}

{% step %}
### 4) Configure close reasons

Add a small set of reasons your team will actually use. Avoid having too many similar reasons.
{% endstep %}

{% step %}
### 5) Configure reminders (optional)

If you want automated follow-ups:

1. Enter schedule days (for example `3,7,14`)
2. Enable auto schedule
3. Write reminder email/SMS texts
4. Decide whether offers should auto-close after the last reminder
{% endstep %}

{% step %}
### 6) Test by sending an offer to yourself

Create a test offer and send it to an internal email address to verify:

* branding and layout
* placeholder values
* images
* insurance texts (if shown)
* reminder text formatting

See [Create new offer](create-new-offer.md) if you need help creating a test offer.
{% endstep %}
{% endstepper %}

***

### Tips for clear customer communication

* Write in short paragraphs and use bullet lists when possible.
* Avoid internal terms (for example, “offeree”) in customer-facing texts.
* Keep the next step obvious (for example: “Click the link in this email to view your offer”).
* Review and update standard texts when you change branding or contact details.
