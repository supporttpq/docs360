# System Setup – General Information Settings

### Overview

General Information controls company-wide defaults and “baseline rules” in Tourpaq.

These settings affect dashboards, booking behavior, reminders, vouchers, and exports.

Go to **Setup → System Setup → General Information**.

{% hint style="warning" %}
Changes apply system-wide.

Test changes on a safe brand/environment when possible.
{% endhint %}

### Purpose

Use these settings to:

* Enforce your booking and payment rules.
* Control visibility for prices, filters, and allotments.
* Automate reminders, vouchers, and notifications.
* Keep behavior consistent across brands and agencies.

### Screenshot

<figure><img src="../../.gitbook/assets/image (579).png" alt="General Information settings in System Setup"><figcaption><p>General Information settings</p></figcaption></figure>

### Available settings

#### 1. Section: General Information (Left Column)

This section controls core financial logic, reminder timing, and export formats.

| **Setting**                          | **Description**                                                                                         |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Payment Dashboard Overdue**        | Defines the number of days before an overdue booking appears on the dashboard.                          |
| **Upsale Days Before Departure**     | Sets how many days before departure the Upsale tab is displayed.                                        |
| **Payment Reminder Tolerance**       | Controls tolerance for overdue payment reminders.                                                       |
| **Questionnaire Percentage / Value** | Defines the minimum percentage of respondents required to validate questionnaire results.               |
| **Offer Reminder Days**              | Sets the reminder interval for pending offers.                                                          |
| **Hide Prices**                      | Hides prices older than the defined number of days.                                                     |
| **Hide Filters**                     | Automatically hides transports, hotels, and users with outdated allotments or information.              |
| **Locked Bookings Departure Date**   | Prevents editing of bookings made before the specified departure date.                                  |
| **Locked bookings costs**            | Sets costs dated before the selected date to read-only. Changing the date can unlock those costs again. |
| **Show Allotment Control**           | Toggles the “All. per day” tab in the Edit Hotel page.                                                  |
| **Input Payments Type**              | Defines accepted payment input formats.                                                                 |
| **Export Text Format**               | Sets format for Payment Registration export (C5 – text, NAV – CSV/Excel).                               |
| **Vouchers Generation**              | Number of days before departure when vouchers are generated.                                            |

#### 2. Section: Settings (Right Column)

This area contains global preferences, voucher display rules, and profit margin behavior.

| **Setting**                                                | **Description**                                                                                                                                                                                               |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Use supplier as voucher issuer**                         | When enabled, vouchers use the supplier logo/details as the issuer. If the supplier has no logo, the logo area is blank.                                                                                      |
| **Retrieve Age From**                                      | Defines how passenger age is calculated (“Age” or “Date of birth”).                                                                                                                                           |
| **Financial Export Email Address**                         | Destination email address for financial exports.                                                                                                                                                              |
| **Default Currency**                                       | Sets the global company currency.                                                                                                                                                                             |
| **PriceList GoUpPrice / GoDownPrice Limit**                | Maximum number of price increases/decreases allowed before requiring special permission.                                                                                                                      |
| **Photo Upload Notification URL**                          | URL to send notifications after photo uploads.                                                                                                                                                                |
| **Max. Budget Select Offer**                               | Sets the maximum budget threshold in Select Offer.                                                                                                                                                            |
| **Average Hotel Costs Day Numbers**                        | Number of days used to calculate average hotel cost values for dashboard comparison.                                                                                                                          |
| **Cost Margin**                                            | Defines the difference threshold used in dashboard reporting.                                                                                                                                                 |
| **Stop sale note mandatory**                               | If checked, then the note for Hotel Stop Sale is mandatory.                                                                                                                                                   |
| **Stop Sale Email**                                        | Email address for receiving Stop Sale notifications.                                                                                                                                                          |
| **Manager Statistic mail**                                 | An email will be sent to the set addresses with manager statistics.                                                                                                                                           |
| **Disable Room Edit Days**                                 | Restricts how many days before departure customers can edit room choices.                                                                                                                                     |
| **Destination App Chat Adjustment days**                   | Number of days before departure when a conversation becomes available in the Destination Guides App.                                                                                                          |
| **Disable Name Change**                                    | Disables the ability for customers to edit names after making a booking. This has an effect only in the customer center (the office is not affected).                                                         |
| **Ignore Transport Cost**                                  | Excludes transport costs from Profit columns in the Price List.                                                                                                                                               |
| **Use Early Booking and Stay and Pay for Discount**        | Uses discounted cost that also takes into account Room Discount Early Booking, and Stay and Pay for calculating the Discount via Profit Margin.                                                               |
| **Allow for same name for different rooms**                | Allows the same passenger name to be used for different rooms (plain text or list text).                                                                                                                      |
| **Hide Age On Vouchers and Lists**                         | Hides adult ages on vouchers and lists. “Adult” is shown instead. For children, only the birth year is shown.                                                                                                 |
| **Show Creditor Currency in Export**                       | Shows costs for transport, extras, supplements, and discounts in Finance Export using the original entered currency.                                                                                          |
| **Disable Email Confirmation**                             | If checked, the email confirmation will be disabled.                                                                                                                                                          |
| **Show uncommitted return payments on guide sales ledger** | If checked, the uncommitted return payments will be shown in the Sales Ledger page on Guide login. This way, the guide will be able to see all payments that are awaiting confirmation from an administrator. |
| **Don't autofill passenger 'Title' in Booking Details**    | Stops auto-filling the passenger “Title”. You must select it before saving.                                                                                                                                   |
| **Assign passengers to existing customers**                | Assigns passengers to an existing customer when possible. Matching is by phone, then email, then name.                                                                                                        |
| **Show QR Code in Vouchers**                               | Shows a QR code on generated booking vouchers.                                                                                                                                                                |
| **QR Code in Vouchers - hide passenger name**              | Hides passenger names on vouchers when QR codes are enabled.                                                                                                                                                  |
| **Show Details on customer**                               | The user can view and edit the Details field on the customer dialog on booking and on the customer center.                                                                                                    |
| **Lock Managed by AvailPro hotels on booking**             | Managed by AvailPro hotels will be blocked from being changed on existing bookings.                                                                                                                           |
| **Show Room prices on financial export for canceled pax**  | Financial export contains the room price when showing canceled pax with the cancellation fee.                                                                                                                 |
| **Order extras in the booking window**                     | When checked, the Extras in the booking window will be sorted according to the "Category order booking" set in the Extras Category.                                                                           |
| **Enable highlight rows on Booking**                       | Passengers' rows will be highlighted when selected.                                                                                                                                                           |
| **Hotel Contract Logo**                                    | If a logo is selected, it will override the agency logo from the hotel contract.                                                                                                                              |
| **Show customer chat on guide login**                      | If checked, the guides will have access to all the customer chat features on their login.                                                                                                                     |
| **Enable new firebase credentials**                        | If checked, the chat and guest app Firebase credentials will be used for the new credential setup.                                                                                                            |

#### 3. Section: Other Settings (Bottom Area)

This section covers default age rules, offer follow-up defaults, and a few integrations.

| **Setting**                         | **Description**                                                                                           |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **Default Adult Age**               | Overrides the default adult age value (default is 99).                                                    |
| **Default Child Age**               | Overrides the default child age value (default is 11).                                                    |
| **Offer default availability days** | Default number of days an offer stays available.                                                          |
| **Offer default follow up days**    | Default number of days before the sales agent should follow up on a sent offer.                           |
| **Product Resourser Type**          | Rule that controls how a resource is used.                                                                |
| **Hotel Special Offer Email**       | Email address that receives notifications when a Special Offer is added by the Supplier or Hotel Manager. |
| **Days number for check Paxport**   | Number of days before departure used for Paxport Reporting checks.                                        |
| **Reset Newsletter choice**         | Resets the “Asked about the newsletter” option after X days.                                              |
| **Account Service Case**            | Account used when a Service Case is deducted on a hotel.                                                  |
| **Set Ex.Bed Discount 4th+**        | Applies “Extra bed discount 4” to passenger 5+ in the room (when enabled).                                |
| **Informative text per company**    | Company-specific informational text.                                                                      |
| **Web Hook URL**                    | Defines the URL used for webhook configurations.                                                          |

### FAQ

<details>

<summary><strong>Do these settings affect all brands and agencies?</strong></summary>

Yes. These are company-wide defaults.

</details>

<details>

<summary><strong>Why did transports/hotels/users disappear from filters?</strong></summary>

Check **Hide Filters**.

It can hide items with outdated allotments or information.

</details>

<details>

<summary><strong>What’s the difference between “Hide Prices” and “Locked bookings costs”?</strong></summary>

**Hide Prices** is about what users can see.

**Locked bookings costs** is about what users can edit.

</details>

<details>

<summary><strong>What happens if I change the “Locked bookings costs” date?</strong></summary>

Costs before the date become read-only.

If you move the date, older costs may become editable again.

</details>

<details>

<summary><strong>How does “Retrieve Age From” impact tickets/vouchers?</strong></summary>

It changes how Tourpaq calculates passenger age.

That can affect age-based pricing and how ages display in documents.

</details>

<details>

<summary><strong>When are vouchers generated?</strong></summary>

Vouchers are generated the number of days before departure set in **Vouchers Generation**.

If you change that value, validate voucher timing on a test booking.

</details>
