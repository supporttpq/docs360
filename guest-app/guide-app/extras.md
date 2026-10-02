---
description: >-
  Excursions that a guide sells in the Guide App, and the Tourpaq Office
  settings that make an Extra appear there.
---

# Extras

{% hint style="danger" %}


**Applies to:** Tourpaq Office · **Last reviewed:** 02-10-2026

{% hint style="danger" %}
**TO VERIFY** — The Guide App screens on this page have not been inspected for TQA-4298. The configuration is carried from the previous Guide App documentation and has not been re-checked on a Guide App screen. Each open question is marked where it applies.
{% endhint %}

#### Overview

**Extras** lists the excursions that a guide can order on behalf of a guest, and shows the orders already made on the **Booked** tab of **Booked extras**.

An excursion sold in the app is an **Extra Order**: an Extra that is ordered and paid separately from the booking. An Extra becomes an Extra Order when both of these are true:

* At least one brand assignment on the Extra includes **Guide sale**.
* The Extra uses allotment type **Manual** or **Generic**.

The same Extra can be ordered in these places:

| Where                                                 | Who orders                                                                    |
| ----------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Guide App**                                         | A guide, on behalf of the guest.                                              |
| **Guest App**                                         | The guest.                                                                    |
| **Extra Orders** tab of the booking in Tourpaq Office | An Administrator or Guide user.                                               |
| WebBooking (OneHome)                                  | The customer, before departure. The order is created through the Booking API. |

Extras with **Manual** and **Generic** allotment are sold in the same way. The allotment type decides how availability is managed, not whether the excursion can be sold.

#### Purpose

* Sell excursions to guests at the destination.
* Take payment with a guide payment type.
* Cancel an order and refund it from the **Booked** tab.
* Show the guide which excursions a guest has already ordered.

#### Preconditions

* The Extra is in an Extras Category of type **Tours**. Only Extras in a Tours category are shown in the apps — see Extras Category.
* At least one brand assignment on the Extra includes **Guide sale** — see Extras.
* The Extra uses allotment type **Manual** or **Generic**, and allotments are generated — see Allotments.
* A resort is assigned on the Extra — see Resources. The apps use only the resort.
* Prices exist for the Extra — see Prices.
* One debit and one credit guide payment type exist — see Payment Method.
* The guide has those payment types assigned.
* The user signs in as a guide. Only guides can add products and make them available in the app.

#### How-to

{% stepper %}
{% step %}
**Configure the Extra**

1. Go to **Extras Setup → Extras** and open the Extra, or click **Create**.
2. Select an **Extras Category** of type **Tours**.
3. Select **Manual** or **Generic** in **Allotment Type** on the **Basic setup** tab.
4. Under **Brands** on the **Overview** tab, select an option that includes **Guide sale** for each brand that sells the excursion, then click **Save**.
5. Assign the resort on the **Resources** tab: click **New filter type**, select the resort, then click **Save filter type**.
6. Click **Generate New Allotments** on the **Allotments** tab (Manual) or the **Generic Allotment** tab (Generic), and choose **Daily** or **Weekly**.
7. Create one price line per age group and period on the **Prices** tab.
8. Add pictures on the **Photos** tab and a text in **Description in customer center**.
{% endstep %}

{% step %}
**Create the pick-up points (route)**

1. Go to **Extras → Routes** and click insert. A route is generated.
2. Add the pick-up points and fill in the fields listed under Field Reference.
3. On the **Brands** tab of the route, assign the agency and mark the route as for sale.
{% endstep %}

{% step %}
**Create the guide payment types**

Go to **Finance → Method of payment** as an Administrator and click **New**. Tick **Guide payment** and **Active**. Create one **Debit** type for sales (cash in) and one **Credit** type for refunds (cash out).
{% endstep %}

{% step %}
**Assign the payment types to the guide**

Open the guide on the Edit Guide page and assign the payment types. To use the DIBS settings of a specific agency for all payments by this guide, select the agency in **Override agency DIBS**. Leave it at the default to use the agency selected in the app.
{% endstep %}

{% step %}
**Sell an excursion in the app**

1. Sign in and tap **Extras**. A list of the available excursions is shown.
2. Select an excursion and view its details.
3. Check the booking details and the number of adults and children, then tap **ADD TO CART**.
4. On **Cart Checkout**, check the excursion, date, passengers (**Pax**), price and the observation fields.
5. Select the payment type under **Paid by**: cash, agent machine or card.
6. Complete the order.
{% endstep %}

{% step %}
**Cancel an order**

On **Extras**, open the **Booked** tab and tap the order. Choose whether to refund the money to the guest. A refund needs a credit payment type assigned to the guide.
{% endstep %}
{% endstepper %}

The order is listed on the **Booked** tab of **Booked extras**, under **Unpaid orders** or **Paid orders**. Expand an order to see the excursion, date, time, number of passengers and price. The order is also listed on the **Extra Orders** tab of the booking in Tourpaq Office.

{% hint style="danger" %}
**TO VERIFY** — (1) The previous page says guide payment types are assigned under **Users → Guides**. Tourpaq Office now shows **Guide Teams**, **Guide Names** and **Guide Profiles** under **Users**. Which one holds the payment types and **Override agency DIBS**? (2) The previous page calls the tab for the resort **Resurser**. Confirm the current label. (3) Is a route required for every excursion, and where does the app show the pick-up points? (4) The previous page gives the route path as **Extras → Routes**. Confirm it on staging.
{% endhint %}

#### Field Reference

**Extra**

| Field                              | Description                                                                                                                                   | Required | Notes                                                                                                                                              |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Extras Category**                | Decides whether the Extra is shown in the apps. Only Extras in a **Tours** category are shown.                                                | Yes      |                                                                                                                                                    |
| **Allotment Type**                 | Decides how availability is managed. **Manual** gives one capacity per day, on set days. **Generic** gives a capacity per date and time slot. | Yes      | **None** and **LinkedToTransport** do not support Extra Orders.                                                                                    |
| **Brands**                         | Makes the Extra orderable for a brand. An option that includes **Guide sale** makes it an Extra Order in the Guide App and Guest App.         | Yes      | **Guide sale + Internet Sale + For Sale** also makes it orderable in WebBooking (OneHome) and on the **Extra Orders** tab of the booking.          |
| **Resources** (resort)             | Assigns the Extra to a resort.                                                                                                                | Yes      | Other resource types, such as transports and hotels, are ignored by the apps.                                                                      |
| **Description in customer center** | The first information shown for the excursion.                                                                                                | No       | Can be set per brand to give different descriptions.                                                                                               |
| **Photos**                         | Pictures shown with the excursion.                                                                                                            | No       | Add one or more representative pictures.                                                                                                           |
| **Prices**                         | One line per age group and period. Shown as **Adult Price** and **Child Price**.                                                              | Yes      | Prices for Extra Orders are defined on this tab only. The Generic Product Price Rules page is no longer used.                                      |
| **START TIME** / **END TIME**      | Gives the same date different prices during the day, for example a morning and an afternoon departure.                                        | No       | Defaults are `00:00` and `23:59`, which is one price for the whole day. The **S** button splits a price line into two time periods.                |
| **Keep showing in app**            | Keeps the excursion listed when allotment is 0 or sold out. No buy button is shown.                                                           | No       | Documented for the Guest App.                                                                                                                      |
| **Automatic billing** (creditor)   | Sets the currency of the sold Extra.                                                                                                          | No       | Without a creditor, the agency currency applies, then the company currency. Create a creditor with the wanted currency and assign it to the Extra. |

A guest is offered the excursion only on allotment dates within the stay, and only while allotment is left.

{% hint style="danger" %}
**TO VERIFY** — Is **Keep showing in app** present on the current **Basic setup** tab, and does it apply to the Guide App as well as the Guest App?
{% endhint %}

**Route pick-up point**

| Field              | Description                                               | Required | Notes        |
| ------------------ | --------------------------------------------------------- | -------- | ------------ |
| **Code**           | Code of the pick-up point.                                | Yes      |              |
| **Description**    | Short description of the pick-up point.                   | Yes      |              |
| **List name**      | Name of the pick-up point as printed on the export files. | Yes      |              |
| **Price**          | Not used for this type of route.                          | No       | Leave empty. |
| **Cost**           | Not used for this type of route.                          | No       | Leave empty. |
| **Price tag**      | Not used for this type of route.                          | No       | Leave empty. |
| **Meeting hour**   | The hour when the guests start to gather.                 | Yes      |              |
| **Departure hour** | The hour when the guests move on with the excursion.      | Yes      |              |
| **Return hour**    | The hour when the guests finish the excursion.            | Yes      |              |

Of the other tabs on a route, only **Brands** is used for this type of Extra.

{% hint style="danger" %}
**TO VERIFY** — Which route fields are mandatory? The previous page does not say.
{% endhint %}

**Guide payment type**

| Field                       | Description                                                                                  | Required | Notes                                                                                                                                         |
| --------------------------- | -------------------------------------------------------------------------------------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Code**                    | Code of the payment type.                                                                    | Yes      |                                                                                                                                               |
| **Plaintext**               | Short description of the payment type.                                                       | Yes      |                                                                                                                                               |
| **Debit/Credit**            | **Debit** is used to buy the excursion (cash in). **Credit** is used for refunds (cash out). | Yes      |                                                                                                                                               |
| **Guide payment**           | Makes the type available to guides.                                                          | Yes      | Must be ticked, because all excursions are sold through guides. The **Agencies** section is active only when it is ticked.                    |
| **Active Y/N**              | Sets the type active or inactive.                                                            | Yes      |                                                                                                                                               |
| **Cash payment**            | Limits the type to cash.                                                                     | No       | If a guide selects Cash and no cash type exists, the system finds no matching payment type and does not complete the order.                   |
| **Agent Machine Payment**   | Like cash, but the guide enters a transaction code from the payment machine.                 | No       |                                                                                                                                               |
| **'Pay from home' Payment** | Like cash, but shows as **Paid from home** on the excursion list.                            | No       |                                                                                                                                               |
| **Is Dankort**              | Limits the type to Dankort cards.                                                            | No       |                                                                                                                                               |
| **Agencies**                | Assigns brands to the payment type.                                                          | No       | With two payment types on different brands, the system takes the one for the selected agency. With two on the same brand, it takes the first. |
| **Override agency DIBS**    | On the guide: use the DIBS settings of a chosen agency for all payments by this guide.       | No       | Applies only in the mobile apps. Default uses the agency selected in the app.                                                                 |

**Recommended setup:** two cash types (one in, one out), two regular credit card types (one in, one out) and two Dankort types (one in, one out).

**Payment fees:** most credit card types carry a fee of 25 kr (3.33 EUR) per order. Cash carries the same fee when the order currency is DKK.

**Payment and cancellation**

How an Extra Order is paid depends on when it is ordered.

| Ordered                                          | Payment                                                                                            | Where the order is visible                                                |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| In the Guide App or Guest App at the destination | Paid with the Extra Order, using a guide payment type.                                             | **Extra Orders** tab, Destination lists, **Booked** tab in the Guide App. |
| Before departure, in WebBooking (OneHome)        | Added to the booking total and paid with the booking. No payment is registered on the Extra Order. | **Extra Orders** tab, Destination lists.                                  |

How an order is cancelled depends on the payment flow:

| Order type                                    | How it is cancelled                                                                                                                                                                                                                   |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Extra Order** (ordered and paid in the app) | From the **Booked** tab. Refunded as described under Sell and Cancel above.                                                                                                                                                           |
| **Pre-booked Extra** (booking payment flow)   | Removed from the booking. The difference is shown as a negative balance in Balance Administration.                                                                                                                                    |
| Booked through OneHome (WebBooking)           | The Booking API inserts the product as an Extra Order. The product is in the Guide App export, and a guide can cancel it from the Guide App. The amount is shown as a negative balance for the booking, not as an Extra Order refund. |

See **Cancelling an Extra** on Extra Orders.

{% hint style="warning" %}
An order made in the app takes allotment first and stays pending. These orders do not appear in Tourpaq Office yet. If payment is approved, the order becomes OK. If payment is rejected, the allotment is restored and the order is cancelled. If payment is not finalised for any reason, the allotment is restored after 10 minutes. If payment is pending, a pending payment is sent to the customer. When the result arrives, an approval email is sent, or a rejection email is sent and the order is cancelled and the allotment restored.
{% endhint %}

{% hint style="info" %}
In the **CXL/Error** menu in Tourpaq Office, you see bookings where the service cancelled an Extra Order but the payment was still confirmed. Use it to find and resolve these differences. The status of an order in the app is cleared when the guest travels home.
{% endhint %}

{% hint style="info" %}
The guide's list is not affected by stop sales hours. A guide sees all available excursions.
{% endhint %}

#### Related pages

* Guide App
* Lists
* Extras
* Allotments
* Prices
* Extra Orders
* Payment Method
{% endhint %}
