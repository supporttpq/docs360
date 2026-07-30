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

* Enforce booking and payment rules.
* Control visibility for prices, filters, and allotments.
* Automate reminders, vouchers, and notifications.
* Keep behavior consistent across brands and agencies.

### Available settings

#### General Information

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

This section controls core financial logic, reminder timing, and export formats:

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
| **Export Text Format**               | Sets the format for Payment Registration export (C5 – text, NAV – CSV/Excel).                           |
| **Vouchers Generation**              | Defines the number of days before departure when vouchers are generated.                                |

#### Settings

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

This area contains global preferences, voucher display rules, and profit margin behavior:

| **Setting**                                                | **Description**                                                                                                                                                              |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Use supplier as voucher issuer**                         | When enabled, vouchers use the supplier's logo and details. If the supplier has no logo, the logo area is blank.                                                             |
| **Retrieve Age From**                                      | Defines how passenger age is calculated (“Age” or “Date of birth”).                                                                                                          |
| **Financial Export Email Address**                         | Destination email address for financial exports.                                                                                                                             |
| **Default Currency**                                       | Sets the global company currency.                                                                                                                                            |
| **PriceList GoUpPrice / GoDownPrice Limit**                | Maximum number of price increases/decreases allowed before requiring special permission.                                                                                     |
| **Photo Upload Notification URL**                          | URL used to send notifications after photo uploads.                                                                                                                          |
| **Max. Budget Select Offer**                               | Sets the maximum budget threshold in Select Offer.                                                                                                                           |
| **Average Hotel Costs Day Numbers**                        | Number of days used to calculate average hotel cost values for dashboard comparison.                                                                                         |
| **Cost Margin**                                            | Defines the difference threshold used in dashboard reporting.                                                                                                                |
| **Stop sale note mandatory**                               | Requires a note for Hotel Stop Sale when selected.                                                                                                                           |
| **Stop Sale Email**                                        | Email address for receiving Stop Sale notifications.                                                                                                                         |
| **Manager Statistic mail**                                 | Sends an email with manager statistics to the configured addresses.                                                                                                          |
| **Disable Room Edit Days**                                 | Restricts how many days before departure customers can edit room choices.                                                                                                    |
| **Destination App Chat Adjustment days**                   | Number of days before departure when a conversation becomes available in the Destination Guides App.                                                                         |
| **Disable Name Change**                                    | Prevents customers from editing names after booking. This affects only the customer center.                                                                                  |
| **Ignore Transport Cost**                                  | Excludes transport costs from Profit columns in the Price List.                                                                                                              |
| **Use Early Booking and Stay and Pay for Discount**        | Uses discounted costs from Room Discount Early Booking and Stay and Pay when calculating discounts through Profit Margin.                                                    |
| **Allow for same name for different rooms**                | Allows the same passenger name to be used for different rooms (plain text or list text).                                                                                     |
| **Hide Age On Vouchers and Lists**                         | Hides adult ages on vouchers and lists. “Adult” is shown instead. For children, only the birth year is shown.                                                                |
| **Show Creditor Currency in Export**                       | Shows costs for transport, extras, supplements, and discounts in Finance Export using the original entered currency.                                                         |
| **Disable Email Confirmation**                             | Disables email confirmations when selected.                                                                                                                                  |
| **Show uncommitted return payments on guide sales ledger** | Shows uncommitted return payments in the Sales Ledger on Guide login. Guides can view payments awaiting administrator confirmation.                                          |
| **Don't autofill passenger 'Title' in Booking Details**    | Stops auto-filling the passenger “Title”. Select a title before saving.                                                                                                      |
| **Assign passengers to existing customers**                | Assigns new web bookings to existing customers when duplicates are found. It prioritizes phone number, email, and name.                                                      |
| **Show QR Code in Vouchers**                               | Shows a QR code on generated booking vouchers.                                                                                                                               |
| **QR Code in Vouchers - hide passenger name**              | Hides passenger names on vouchers when QR codes are enabled.                                                                                                                 |
| **Show Details on customer**                               | Allows users to view and edit the Details field in booking and customer-center dialogs.                                                                                      |
| **Lock Managed by AvailPro hotels on booking**             | Prevents changes to AvailPro-managed hotels on existing bookings.                                                                                                            |
| **Show Room prices on financial export for canceled pax**  | Financial export contains the room price when showing canceled pax with the cancellation fee.                                                                                |
| **Order extras in the booking window**                     | Sorts Extras in the booking window by the "Category order booking" setting in Extras Category.                                                                               |
| **Order extras on e-ticket**                               | Sorts Extras on the e-ticket by the "Category order booking" setting in Extras Category. <mark style="color:red;">This feature is supported only on ticket version 3.</mark> |
| **Enable multiple cancellation insurance**                 | Enables multiple overlapping cancellation insurance policies per destination.                                                                                                |
| **Enable highlight rows on Booking**                       | Highlights passenger rows when selected.                                                                                                                                     |
| **Hotel Contract Logo**                                    | If a logo is selected, it will override the agency logo from the hotel contract.                                                                                             |
| **Show customer chat on guide login**                      | If checked, the guides will have access to all the customer chat features on their login.                                                                                    |
| **Enable new firebase credentials**                        | Uses the chat and guest app Firebase credentials for the new credential setup when selected.                                                                                 |

#### Other settings

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

This section covers default age rules, offer follow-up defaults, and a few integrations:

<table data-header-hidden data-search="true"><thead><tr><th></th><th></th></tr></thead><tbody><tr><td><strong>Setting</strong></td><td><strong>Description</strong></td></tr><tr><td><strong>Default Adult Age</strong></td><td>Overrides the default adult age value (default is 99).</td></tr><tr><td><strong>Default Child Age</strong></td><td>Overrides the default child age value (default is 11).</td></tr><tr><td><strong>Offer default availability days</strong></td><td>Defines the number of days an offer remains available.</td></tr><tr><td><strong>Offer default follow up days</strong></td><td>Defines the number of days before a sales agent follows up on a sent offer.</td></tr><tr><td><strong>Product Resourser Type</strong></td><td>Rule that controls how a resource is used.</td></tr><tr><td><strong>Hotel Special Offer Email</strong></td><td>Email address that receives notifications when a Special Offer is added by the Supplier or Hotel Manager.</td></tr><tr><td><strong>Days number for check Paxport</strong></td><td>Number of days before departure used for Paxport Reporting checks.</td></tr><tr><td><strong>Reset Newsletter choice</strong></td><td>Resets the “Asked about the newsletter” option after X days.</td></tr><tr><td><strong>Account Service Case</strong></td><td>Account used when a Service Case is deducted from a hotel.</td></tr><tr><td><strong>Set Ex.Bed Discount 4th+</strong></td><td>Applies “Extra bed discount 4” to passenger 5+ in the room (when enabled).</td></tr><tr><td><strong>Informative text per company</strong></td><td>Company-specific informational text.</td></tr><tr><td><strong>Web Hook URL</strong></td><td>Defines the URL used for webhook configurations.</td></tr></tbody></table>
