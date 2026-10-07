---
description: >-
  Excursions that a guide sells in the Guide App, and the Tourpaq Office
  settings that make an Extra appear there.
---

# Extras

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
2.  Select an **Extras Category** of type **Tours**.

    ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-dce28b7a9e3e4b0568273aaa4aee5b94ac2efb9e%2Fimage%20\(279\).png?alt=media)
3. Select **Manual** or **Generic** in **Allotment Type** on the **Basic setup** tab.
4. Under **Brands** on the **Overview** tab, select an option that includes **Guide sale** for each brand that sells the excursion, then click **Save**.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-f4a1ec7cfd51a78b5a1acdc2cf2370433853c643%2Fimage%20\(283\).png?alt=media)
5. Assign the resort on the **Resources** tab: click **New filter type**, select the resort, then click **Save filter type**.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-a94439bab8957dbd0929554f0cbd75e54cbf18f6%2Fimage%20\(282\).png?alt=media)
6. Click **Generate New Allotments** on the **Allotments** tab (Manual) or the **Generic Allotment** tab (Generic), and choose **Daily** or **Weekly**.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-1397b7254ee97754ad5c234a1613ea61d524598b%2Fimage%20\(66\).png?alt=media)\
   **Daily** - the tool will generate allotments each day or from n to n days (e.g. from 2 to 2 days) in a given date interval (**Duration**). In here we also have the possibility to make new allotments each n minutes (**Daily Frequency**) between a time interval (this is applying for each day) or to set up the **Specific time** of the allotments (see the picture below),\
   **Weekly** - the tool will generate allotments for one or more days of the week. We will also be able to specify the allotments frequency (each week or from n to n weeks). We will also have to define the desired time or set the allotment to be available every n minutes, exactly like in the **Daily** basis option. From this point, the steps are similar.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-6e50f6e3fbb85fc89093a51fb0b97e22c0c67911%2Fimage%20\(67\).png?alt=media)
7. Create one price line per age group and period on the **Prices** tab.
8. Add pictures on the **Photos** tab and a text in **Description in customer center**.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-7f8ee839d8dfd840f2ec3c39ea9118ba6faaf186%2Fimage%20\(280\).png?alt=media)
{% endstep %}

{% step %}
**Create the pick-up points (route)**

1. Go to **Extras → Routes** and click insert. A route is generated.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-412610f3a993ea20e9614a5334dfd7dbdc7b75f2%2Fimage%20\(2\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20\(1\)%20%20%20\(2\).png?alt=media)
2. Add the pick-up points and fill in the fields listed under Field Reference.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-2acec4ae18694a734b0133eb64a15a2c07c2fa76%2Fimage%20\(72\).png?alt=media)
3. On the **Brands** tab of the route, assign the agency and mark the route as for sale.
{% endstep %}

{% step %}
**Create the guide payment types**

Go to **Finance → Method of payment** as an Administrator and click **New**. Tick **Guide payment** and **Active**. Create one **Debit** type for sales (cash in) and one **Credit** type for refunds (cash out).\
![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-f08deaf552adfb4bcdf6bf65eb97d549faff356f%2Fimage%20\(73\).png?alt=media)\
![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-474ee969c1c856335bfa1d624c0fce427eed2f66%2Fimage%20\(74\).png?alt=media)
{% endstep %}

{% step %}
**Assign the payment types to the guide**

Open the guide on the Edit Guide page and assign the payment types. To use the DIBS settings of a specific agency for all payments by this guide, select the agency in **Override agency DIBS**. Leave it at the default to use the agency selected in the app.\
![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-81c590c478f5f572b2f662064f65399a8a1dcad1%2Fimage%20\(75\).png?alt=media)
{% endstep %}

{% step %}
**Sell an excursion in the app**

1. Sign in and tap **Extras**. A list of the available excursions is shown.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-c546f57881a6c738cb14b377766bde4726e1b07f%2Fimage%20\(190\).png?alt=media)
2. Select an excursion and view its details.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-d90839cd76a579eaffa6447f91c1b220e7b862a6%2F11-525720509f53db66d4be8db089be1662.png?alt=media)
3. Check the booking details and the number of adults and children, then tap **ADD TO CART**.\
   ![](https://docs.tourpaq.com/assets/images/22-681f42ba0ae483955f992620f44cdda0.png)
4. On **Cart Checkout**, check the excursion, date, passengers (**Pax**), price and the observation fields.
5. Select the payment type under **Paid by**: cash, agent machine or card.\
   ![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-578c44e1a2c0b32ca1f6f8be20f58acd98abbac0%2Fimage%20\(191\).png?alt=media)
6. Complete the order.
{% endstep %}

{% step %}
**Cancel an order**

On **Extras**, open the **Booked** tab and tap the order. Choose whether to refund the money to the guest. A refund needs a credit payment type assigned to the guide.\
![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-3899bb7b981daf66ed4f62a7cfc465275c20b701%2Fimage%20\(192\).png?alt=media)\
![](https://docs.tourpaq.com/assets/images/55-f4fe0b97ccc6779a3e8784668d4048d4.png)
{% endstep %}
{% endstepper %}

The order is listed on the **Booked** tab of **Booked extras**, under **Unpaid orders** or **Paid orders**. Expand an order to see the excursion, date, time, number of passengers and price. The order is also listed on the **Extra Orders** tab of the booking in Tourpaq Office.

#### Field Reference

**Extra**

<table data-search="false"><thead><tr><th>Field</th><th>Description</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Extras Category</strong></td><td>Decides whether the Extra is shown in the apps. Only Extras in a <strong>Tours</strong> category are shown.</td><td></td></tr><tr><td><strong>Allotment Type</strong></td><td>Decides how availability is managed. <strong>Manual</strong> gives one capacity per day, on set days. <strong>Generic</strong> gives a capacity per date and time slot.</td><td><strong>None</strong> and <strong>LinkedToTransport</strong> do not support Extra Orders.</td></tr><tr><td><strong>Brands</strong></td><td>Makes the Extra orderable for a brand. An option that includes <strong>Guide sale</strong> makes it an Extra Order in the Guide App and Guest App.</td><td><strong>Guide sale + Internet Sale + For Sale</strong> also makes it orderable in WebBooking (OneHome) and on the <strong>Extra Orders</strong> tab of the booking.</td></tr><tr><td><strong>Resources</strong> (resort)</td><td>Assigns the Extra to a resort.</td><td>Other resource types, such as transports and hotels, are ignored by the apps.</td></tr><tr><td><strong>Description in customer center</strong></td><td>The first information shown for the excursion.</td><td>Can be set per brand to give different descriptions.</td></tr><tr><td><strong>Photos</strong></td><td>Pictures shown with the excursion.</td><td>Add one or more representative pictures.</td></tr><tr><td><strong>Prices</strong></td><td>One line per age group and period. Shown as <strong>Adult Price</strong> and <strong>Child Price</strong>.</td><td>Prices for Extra Orders are defined on this tab only. The Generic Product Price Rules page is no longer used.</td></tr><tr><td><strong>START TIME</strong> / <strong>END TIME</strong></td><td>Gives the same date different prices during the day, for example a morning and an afternoon departure.</td><td>Defaults are <code>00:00</code> and <code>23:59</code>, which is one price for the whole day. The <strong>S</strong> button splits a price line into two time periods.</td></tr><tr><td><strong>Keep showing in app</strong></td><td>Keeps the excursion listed when allotment is 0 or sold out. No buy button is shown.</td><td>Documented for the Guest App.<br><img src="https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-6ffc67467a0d8187f436565c6fff8781bb4e8c04%2Fimage%20(284).png?alt=media" alt=""></td></tr><tr><td><strong>Automatic billing</strong> (creditor)</td><td>Sets the currency of the sold Extra.</td><td>Without a creditor, the agency currency applies, then the company currency. Create a creditor with the wanted currency and assign it to the Extra.<br><img src="https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-5e2202d873991fe83e1a68fc837862b4d9939c60%2Fimage%20(281).png?alt=media" alt=""></td></tr></tbody></table>

A guest is offered the excursion only on allotment dates within the stay, and only while allotment is left.

**Route pick-up point**

<table data-search="false"><thead><tr><th>Field</th><th>Description</th></tr></thead><tbody><tr><td><strong>Code</strong></td><td>Code of the pick-up point.</td></tr><tr><td><strong>Description</strong></td><td>Short description of the pick-up point.</td></tr><tr><td><strong>List name</strong></td><td>Name of the pick-up point as printed on the export files.</td></tr><tr><td><strong>Price</strong></td><td>Not used for this type of route.</td></tr><tr><td><strong>Cost</strong></td><td>Not used for this type of route.</td></tr><tr><td><strong>Price tag</strong></td><td>Not used for this type of route.</td></tr><tr><td><strong>Meeting hour</strong></td><td>The hour when the guests start to gather.</td></tr><tr><td><strong>Departure hour</strong></td><td>The hour when the guests move on with the excursion.</td></tr><tr><td><strong>Return hour</strong></td><td>The hour when the guests finish the excursion.</td></tr></tbody></table>

Of the other tabs on a route, only **Brands** is used for this type of Extra.

**Guide payment type**

<table data-search="false"><thead><tr><th>Field</th><th>Description</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Code</strong></td><td>Code of the payment type.</td><td></td></tr><tr><td><strong>Plaintext</strong></td><td>Short description of the payment type.</td><td></td></tr><tr><td><strong>Debit/Credit</strong></td><td><strong>Debit</strong> is used to buy the excursion (cash in). <strong>Credit</strong> is used for refunds (cash out).</td><td></td></tr><tr><td><strong>Guide payment</strong></td><td>Makes the type available to guides.</td><td>Must be ticked, because all excursions are sold through guides. The <strong>Agencies</strong> section is active only when it is ticked.</td></tr><tr><td><strong>Active Y/N</strong></td><td>Sets the type active or inactive.</td><td></td></tr><tr><td><strong>Cash payment</strong></td><td>Limits the type to cash.</td><td>If a guide selects Cash and no cash type exists, the system finds no matching payment type and does not complete the order.</td></tr><tr><td><strong>Agent Machine Payment</strong></td><td>Like cash, but the guide enters a transaction code from the payment machine.</td><td></td></tr><tr><td><strong>'Pay from home' Payment</strong></td><td>Like cash, but shows as <strong>Paid from home</strong> on the excursion list.</td><td></td></tr><tr><td><strong>Is Dankort</strong></td><td>Limits the type to Dankort cards.</td><td></td></tr><tr><td><strong>Agencies</strong></td><td>Assigns brands to the payment type.</td><td>With two payment types on different brands, the system takes the one for the selected agency. With two on the same brand, it takes the first.</td></tr><tr><td><strong>Override agency DIBS</strong></td><td>On the guide: use the DIBS settings of a chosen agency for all payments by this guide.</td><td>Applies only in the mobile apps. Default uses the agency selected in the app.</td></tr></tbody></table>

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
In the **CXL/Error** menu in Tourpaq Office, you see bookings where the service cancelled an Extra Order, but the payment was still confirmed. Use it to find and resolve these differences. The status of an order in the app is cleared when the guest travels home.\
![](https://155167782-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F4ho2ecpjkno5JvDRSja9%2Fuploads%2Fgit-blob-a18e48168c1c487ac8ae3ca77fede223f1f60f10%2Fimage%20\(1\)%20\(2\).png?alt=media)
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
