---
description: >-
  Excursions that a guide sells in the Guide App, and the Tourpaq Office
  settings that make an Extra appear there.
---

# Extras

{% hint style="danger" %}
**TO VERIFY** — The Guide App screens in this page have not been inspected for TQA-4298. The configuration below is carried from the existing Guide App page and has not been re-checked on a Guide App screen.
{% endhint %}

#### Overview

**Extras** lists the excursions that a guide can order on behalf of a guest, and shows the orders already made on the **Booked** tab of **Booked extras**.

An excursion sold in the Guide App is an **Extra Order**: an Extra that is ordered and paid separately from the booking. The Extra is configured in Tourpaq Office. The Guide App shows it.

#### Purpose

* Sell excursions to guests at the destination.
* Take payment with a guide payment type.
* Cancel an order and refund it from the **Booked** tab.

#### Preconditions

* The Extra is in an Extras Category of type **Tours** — see Extras Category.
* At least one brand assignment on the Extra includes **Guide sale** — see Extras.
* The Extra uses allotment type **Manual** or **Generic**, and allotments are generated — see Allotments.
* A resort is assigned on the Extra — see Resources.
* Prices exist for the Extra — see Prices.
* One debit and one credit guide payment type exist — see Payment Method.
* The guide has those payment types assigned.

#### How-to

{% stepper %}
{% step %}
**Configure the Extra**

1. Go to **Extras Setup → Extras** and open the Extra, or click **Create**.
2. Select an **Extras Category** of type **Tours**.
3. Select **Manual** or **Generic** in **Allotment Type**.
4. In **Brands**, select an option that includes **Guide sale**, then click **Save**.
5. Add the resort on the **Resources** tab.
6. Generate allotments on the **Allotments** tab (Manual) or **Generic Allotment** tab (Generic).
7. Create the price lines on the **Prices** tab.
{% endstep %}

{% step %}
**Create the guide payment types**

Go to **Finance → Method of payment** and click **New**. Tick **Guide payment** and set **Active**. Create one **Debit** type for sales and one **Credit** type for refunds.
{% endstep %}

{% step %}
**Assign the payment types to the guide**

Assign the payment types on the guide record.
{% endstep %}

{% step %}
**Sell an excursion in the app**

1. Sign in and tap **Extras**.
2. Select the excursion and check the booking, adults and children.
3. Tap **ADD TO CART**.
4. On **Cart Checkout**, check the excursion, date, passengers (**Pax**) and price.
5. Select the payment type under **Paid by** and complete the order.
{% endstep %}

{% step %}
**Cancel an order**

On **Extras**, open the **Booked** tab, tap the order and cancel it. To refund, the guide needs a credit payment type.
{% endstep %}
{% endstepper %}

The order is listed on the **Booked** tab under **Unpaid orders** or **Paid orders**, and on the **Extra Orders** tab of the booking in Tourpaq Office.

{% hint style="danger" %}
**TO VERIFY** — The existing page says guide payment types are assigned under **Users → Guides**. Tourpaq Office now shows **Guide Teams**, **Guide Names** and **Guide Profiles** under **Users**. Which one holds the payment types and the **Override agency DIBS** setting?
{% endhint %}

#### Field Reference

**Extra**

| Field                              | Description                                                                                                                           | Notes                                                                                                                                     |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Extras Category**                | Decides whether the Extra is shown in the apps. Only Extras in a **Tours** category are shown.                                        |                                                                                                                                           |
| **Allotment Type**                 | Decides how availability is managed. **Manual** gives one capacity per day. **Generic** gives a capacity per date and time slot.      | **None** and **LinkedToTransport** do not support Extra Orders.                                                                           |
| **Brands**                         | Makes the Extra orderable for a brand. An option that includes **Guide sale** makes it an Extra Order in the Guide App and Guest App. | **Guide sale + Internet Sale + For Sale** also makes it orderable in WebBooking (OneHome) and on the **Extra Orders** tab of the booking. |
| **Resources** (resort)             | Assigns the Extra to a resort. The apps use only the resort.                                                                          | Other resource types, such as transports and hotels, are ignored by the apps.                                                             |
| **Description in customer center** | The first information shown for the excursion.                                                                                        | Can be set per brand.                                                                                                                     |
| **Photos**                         | Pictures shown with the excursion.                                                                                                    |                                                                                                                                           |
| **Prices**                         | One line per age group and period. Shown as **Adult Price** and **Child Price**.                                                      | Prices for Extra Orders are defined on this tab only.                                                                                     |
| **START TIME** / **END TIME**      | Gives the same date different prices during the day.                                                                                  | Defaults are `00:00` and `23:59`, which is one price for the whole day.                                                                   |
| **Keep showing in app**            | Keeps the excursion listed when allotment is 0 or sold out. No buy button is shown.                                                   | Documented for the Guest App.                                                                                                             |
| **Automatic billing** (creditor)   | Sets the currency of the sold Extra. Without a creditor, the agency currency applies, then the company currency.                      |                                                                                                                                           |

{% hint style="danger" %}
**TO VERIFY** — Is **Keep showing in app** present on the current **Basic setup** tab, and does it apply to the Guide App as well as the Guest App?
{% endhint %}

**Guide payment type**

| Field                       | Description                                                                                  | Notes                                                                        |
| --------------------------- | -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Code**                    | Code of the payment type.                                                                    |                                                                              |
| **Plaintext**               | Short description of the payment type.                                                       |                                                                              |
| **Debit/Credit**            | **Debit** is used to buy the excursion (cash in). **Credit** is used for refunds (cash out). |                                                                              |
| **Guide payment**           | Makes the type available to guides.                                                          | Must be ticked. The **Agencies** section is active only when it is ticked.   |
| **Active Y/N**              | Sets the type active or inactive.                                                            |                                                                              |
| **Cash payment**            | Limits the type to cash.                                                                     | If a guide selects Cash and no cash type exists, the order is not completed. |
| **Agent Machine Payment**   | Like cash, but the guide enters a transaction code from the payment machine.                 |                                                                              |
| **'Pay from home' Payment** | Like cash, but shows as **Paid from home** on the excursion list.                            |                                                                              |
| **Is Dankort**              | Limits the type to Dankort cards.                                                            |                                                                              |

{% hint style="info" %}
The guide's list is not affected by stop sales hours. A guide sees all available excursions.
{% endhint %}

{% hint style="warning" %}
An order made in the app takes allotment first and stays pending. If payment is approved, the order becomes OK. If payment is rejected, the allotment is restored and the order is cancelled. If payment is not finalised, the allotment is restored after 10 minutes.
{% endhint %}

#### Related pages

* Guide App
* Extras
* Allotments
* Prices
* Extra Orders
* Payment Method
