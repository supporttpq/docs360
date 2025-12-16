# Customer Offer SMS template

### Overview

A **Customer Offer SMS template** is a reusable message format you can use when sending an SMS from an offer.

Instead of writing the full SMS every time, you create a template once (per Brand) and then only write the _custom_ part of the message when you send it.

<figure><img src="../.gitbook/assets/image (273).png" alt="Customer Offer SMS template settings"><figcaption></figcaption></figure>

***

### Where to find it

In most setups, SMS templates for offers are configured per Brand:

* **Brands → (select a Brand) → Select Offer → SMS configuration**

{% hint style="info" %}
If you have multiple brands, make sure you update the correct **Brand**, otherwise the wrong template may be used when sending offers.
{% endhint %}

***

### How it works

The template can include placeholders (variables) that Tourpaq fills in automatically.

The most important one is:

* `[Message]` — this is the text you type when you send the SMS from the offer.

When the SMS is sent:

1. Tourpaq takes your SMS template.
2. It replaces placeholders like `[CustomerFirstName]` and `[BrandName]`.
3. It replaces `[Message]` with the text you wrote for this specific customer.

<figure><img src="../.gitbook/assets/image (274).png" alt="SMS configuration and variables"><figcaption></figcaption></figure>

{% hint style="success" %}
If your template does **not** include `[Message]`, the custom text you type when sending may not appear in the outgoing SMS.
{% endhint %}

***

### Create or update an SMS template

{% stepper %}
{% step %}
### 1) Open the Brand’s Select Offer settings

Go to:

* **Brands → (select a Brand) → Select Offer**
{% endstep %}

{% step %}
### 2) Find the SMS template field

Locate the SMS template area in the Select Offer settings.

Depending on your setup, you may be able to:

* write/edit the SMS template directly
* or select a predefined template
{% endstep %}

{% step %}
### 3) Add placeholders

Add the placeholders you want to use.

At minimum, include:

* `[Message]`

Optionally include placeholders such as:

* `[CustomerFirstName]`
* `[BrandName]`
{% endstep %}

{% step %}
### 4) Save and test

Send a test SMS to an internal phone number to confirm:

* the greeting text looks correct
* placeholder values are inserted
* the custom text you typed shows where `[Message]` is placed
{% endstep %}
{% endstepper %}

***

### Example

Template example:

```
Dear [CustomerFirstName],
[Message]
Thank you for choosing [BrandName].
```

When you send the SMS from an offer, whatever you type in the offer’s message field replaces `[Message]`.

<figure><img src="../.gitbook/assets/image (275).png" alt="Example of SMS template result"><figcaption></figcaption></figure>

***

### Tips for writing good offer SMS messages

* Keep the SMS short and action-oriented.
* Make the next step clear (for example: “Please check your email for the offer link”).
* Avoid internal terms that customers won’t understand.
* If you include links, verify they work on mobile.

***

### Related pages

* [Select text for Offers](select-text-for-offers.md)
* [Customer offers automatic flow](customer-offer-automatic-flow.md)
