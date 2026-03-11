---
description: >-
  Having trouble? This page covers the most common issues users encounter in
  Tourpaq, organised by module. Each issue includes a clear cause and
  step-by-step fix.
noIndex: true
icon: hammer-brush
---

# TROUBLESHOOTING

{% hint style="info" %}
**Can't find your issue here?** Use `Ctrl + K` to search the full manual, or jump to Getting Help at the bottom of this page.
{% endhint %}

### Quick Navigation

| Module                | Jump to                  |
| --------------------- | ------------------------ |
| 🔐 Login & Access     | Login & Access Issues    |
| 📋 Bookings           | Booking Issues           |
| 💰 Finance & Payments | Finance & Payment Issues |
| 🏷️ Price Lists       | Price List Issues        |
| 🏨 Hotels             | Hotel Issues             |
| ✈️ Transport          | Transport Issues         |
| 📧 Email & SMS        | Email & SMS Issues       |
| 📤 Exports            | Export Issues            |
| ⚙️ System & Setup     | System & Setup Issues    |

***

***

### 🔐 Login & Access Issues

***

#### I can't log in — my credentials aren't working

**Likely cause:** Incorrect password, expired session, or account not yet activated.

**Steps to fix:**

1. Double-check your user is entered correctly
2. Make sure **Caps Lock** is off
3. Click **Forgot Password** on the login screen and follow the reset link sent to your email
4. Check your spam/junk folder if you don't receive the reset email within 5 minutes
5. If you still can't log in, contact your system administrator — your account may be inactive or locked

***

#### I'm not seeing the Brand or module I need

**Likely cause:** Your user role doesn't have permission to access that Brand or module.

**Steps to fix:**

1. Check the top of the screen — confirm which Brand is currently selected
2. If the Brand you need isn't in the selector, your account hasn't been granted access to it
3. Contact your system administrator and ask them to update your **user permissions** under [Users](https://manual.tourpaq.com/users/users)

{% hint style="warning" %}
&#x20;Only system administrators can grant access to Brands and modules. This cannot be self-served.&#x20;
{% endhint %}

***

#### I've been locked out after failing 2FA

**Likely cause:** Lost access to your authenticator app, or the time on your device is out of sync.

**Steps to fix:**

1. Make sure your phone's clock is set to **automatic/network time** — 2FA codes are time-sensitive
2. If you've lost your authenticator device, use your **recovery code** (provided during 2FA setup)
3. If you don't have a recovery code, contact your administrator to reset your 2FA under [2 Factor Authentication](https://manual.tourpaq.com/2-factor-authentication)

***

#### The page looks broken or doesn't load correctly

**Likely cause:** Browser compatibility issue or cached data.

**Steps to fix:**

1. Try **hard refreshing** the page: `Ctrl + Shift + R` (Windows) or `⌘ + Shift + R` (Mac)
2. Clear your browser cache and cookies, then reload
3. Disable browser extensions temporarily (especially ad blockers) as these can interfere with the interface
4. If the issue persists, contact your administrator and note which page and browser version you're using

***

***

### 📋 Booking Issues

***

#### No transport or hotel results appear when I search in New Booking

**Likely cause:** Missing or misconfigured price lists, allotment, or brand selection.

**Steps to fix:**

1. Confirm you have the correct **Brand** selected at the top of the screen
2. Check that your **travel dates** fall within a valid price list period
3. Widen your search — try different dates, destinations, or number of passengers
4. Verify that there is available **allotment** for the hotel/transport combination you're searching
5. Check that a valid **Price List** exists for the period under [Price List](https://manual.tourpaq.com/price-list/pricelist)
6. If nothing appears after the above, contact your administrator to check transport and hotel configuration

{% hint style="info" %}
The most common cause of empty search results is a missing or expired price list. Always check this first.&#x20;
{% endhint %}

***

#### The price shown in a booking is 0 or looks incorrect

**Likely cause:** Missing price list entry, misconfigured discount/supplement rule, or wrong brand selected.

**Steps to fix:**

1. Open **Profit** within the booking to see a full breakdown of price components
2. Confirm the correct **Brand** is active
3. Check that a valid **Price List** covers the booking dates and room/transport combination
4. Look for **discount or supplement rules** that may be adjusting the price unexpectedly — see [Discounts/Supplements](https://manual.tourpaq.com/discounts-supplements)
5. If the price is still incorrect, escalate to your pricing team or administrator

***

#### I can't save a booking — I'm getting a validation error

**Likely cause:** Required fields are missing or contain invalid data.

**Steps to fix:**

1. Look for **red highlighted fields** on the page — these indicate missing or invalid entries
2. Make sure all **passenger details** are complete (name, date of birth, etc.)
3. Check that a valid **payment method** has been selected
4. Verify that the **Brand** and **travel components** (hotel, transport) are all correctly assigned
5. If the error message is unclear, note the exact text and contact your administrator

***

#### A booking I created has disappeared

**Likely cause:** You may be searching under the wrong Brand, or the booking was cancelled by another user.

**Steps to fix:**

1. Go to [All Bookings](https://manual.tourpaq.com/booking/all-bookings) and search by **booking number** or **customer name**
2. Make sure the **Brand filter** is set to the correct brand (or "All Brands")
3. Check whether the **status filter** is hiding cancelled or archived bookings — remove all filters and search again
4. Open the **History** tab within the booking to see if it was modified or cancelled, and by whom

***

#### The booking price changed after I edited it

**Likely cause:** Automatic discount recalculation triggered after editing a booking component.

**Steps to fix:**

1. Open **Economics** to review which price components changed
2. Check whether **automatic discount rules** are set to recalculate on edit — see [Keep Automatic Discounts Prices](https://manual.tourpaq.com/booking/new-booking/keep-automatic-discounts-prices)
3. Use the **History** tab to compare the price before and after the edit
4. If needed, manually override the price components in Economics

***

***

### 💰 Finance & Payment Issues

***

#### A payment isn't showing on a booking after registration

**Likely cause:** The payment was saved under the wrong booking number or Brand, or it's still processing.

**Steps to fix:**

1. Go to [Payment Registration](https://manual.tourpaq.com/finance/payment-registration) and search for the payment by date, amount, or customer
2. Confirm the payment was linked to the **correct booking number**
3. Refresh the booking page — processing can occasionally take a moment to reflect
4. If the payment is confirmed but still not showing, contact your administrator to check for a sync issue

***

#### An autobilling charge was processed twice

**Likely cause:** Duplicate autobilling rule or a known bug (fixed in v3.1.2).

**Steps to fix:**

1. Check the booking's **payment history** to confirm the duplicate charge
2. Go to [Autobilling](https://manual.tourpaq.com/autobilling) and review the rules applied to this booking
3. Initiate a **refund** for the duplicate amount via [Refund File Import](https://manual.tourpaq.com/finance/refund-file-import) or manual registration
4. Contact your administrator to review the autobilling rule configuration and prevent recurrence

***

#### I can't generate an invoice for a booking

**Likely cause:** The booking is not in a confirmed state, or invoice settings are not configured for the Brand.

**Steps to fix:**

1. Confirm the booking status is **Confirmed** — invoices cannot be generated for pending or cancelled bookings
2. Check that invoice settings are correctly configured for your Brand under [Company](https://manual.tourpaq.com/company)
3. Ensure the customer profile has a valid **billing address**
4. If the option is greyed out, your user role may not have invoice generation permissions — contact your administrator

***

#### Missed Payments report is showing bookings that have been paid

**Likely cause:** Payment registration was done but not correctly linked, or there's a filter mismatch.

**Steps to fix:**

1. Open the booking from the report and check the **Economics** and payment history
2. Confirm the payment is registered with the correct **method of payment** and **amount**
3. Check whether the payment date falls within the report's filter period
4. If everything looks correct but the booking still appears, contact your administrator to check for a data sync issue

***

***

### 🏷️ Price List Issues

***

#### A price list migration didn't carry over all rules

**Likely cause:** Certain rule types (e.g. supplement rules or special offers) are not included in the default migration scope.

**Steps to fix:**

1. Go to [Migrate Pricelist](https://manual.tourpaq.com/price-list/migrate-pricelist) and review the migration settings
2. Check whether **discount/supplement rules**, **regulation rules**, and **tags** were included in the migration scope
3. Manually add any missing rules to the new price list
4. Run a test search in **New Booking** to validate that prices are displaying correctly for the new period

***

#### Prices are not appearing for a specific destination or hotel

**Likely cause:** The price list doesn't cover that hotel/transport combination, or the allotment is zero.

**Steps to fix:**

1. Open [Pricelist](https://manual.tourpaq.com/price-list/pricelist) and search for entries matching the destination and travel period
2. Confirm the hotel and room type are included in the price list
3. Check **allotment** — if it's zero, the option won't appear in search results even if a price exists
4. Verify that the price list is **active** and not in draft status

***

***

### 🏨 Hotel Issues

***

#### A hotel is not appearing in New Booking search results

**Likely cause:** Stop Sales, Close Out, zero allotment, or missing price list entry.

**Steps to fix:**

1. Check [Stop Sales](https://manual.tourpaq.com/stop-sales) — confirm no stop sales rule is active for the dates searched
2. Check [Close Out](https://manual.tourpaq.com/close-out) — confirm the hotel/room type is not closed out for the period
3. Verify **allotment** is greater than zero for the dates and room type
4. Confirm a valid **Price List** entry exists for this hotel and the searched period
5. Check that the hotel is set to **active** in [Hotels](https://manual.tourpaq.com/hotel/hotels)

***

#### Hotel confirmation emails are not being sent to the supplier

**Likely cause:** Supplier email address is missing or the confirmation email rule is not configured.

**Steps to fix:**

1. Go to [Hotel and Transfer Confirmation Emails to Suppliers](https://manual.tourpaq.com/hotel-and-transfer-confirmation-e-mail-to-suppliers) and check the configuration
2. Confirm the supplier profile has a valid **email address** under [Suppliers](https://manual.tourpaq.com/suppliers)
3. Check the **Email Setup** section to confirm the confirmation email template is active
4. Review the **E-mail/SMS Center Statistics** to see if the email was sent but bounced

***

***

### ✈️ Transport Issues

***

#### A flight is showing as fully booked but I know seats are available

**Likely cause:** Allotment in Tourpaq is depleted, even if the airline still has seats (the two systems are independent).

**Steps to fix:**

1. Go to [Transport](https://manual.tourpaq.com/transport/transport) and find the relevant flight
2. Check the **available seat count** — if it's zero, the system will treat it as fully booked
3. Update the allotment to reflect the actual available seats
4. If the transport is a **Real Transport**, check the [Real Transport Dashboard](https://manual.tourpaq.com/real-transport-dashboard) for sync status

***

#### Seat assignments are not saving correctly

**Likely cause:** Conflict with another booking or a display bug (known issue fixed in v3.2.0).

**Steps to fix:**

1. Refresh the booking and check [Transport Seating](https://manual.tourpaq.com/booking/new-booking/transport-seating) again
2. Ensure no other user is editing the same booking simultaneously
3. Try assigning different seats and saving — then reassign to the desired seats
4. If the issue persists after v3.2.0, contact your administrator and provide the booking number and flight details

***

#### GDS Queue items are reappearing after being actioned

**Likely cause:** A known issue fixed in v3.1.2, or the item was actioned by your session but not synced correctly.

**Steps to fix:**

1. Confirm your Tourpaq version is **3.1.2 or later** — earlier versions had a known GDS Queue sync bug
2. Log out and back in, then check the GDS Queue again
3. If the item genuinely requires re-action (e.g. a schedule change), process it again and monitor
4. Contact your administrator if items continue to reappear after actioning

***

***

### 📧 Email & SMS Issues

***

#### Booking confirmation emails are not being received by customers

**Likely cause:** Wrong customer email address, email marked as spam, or sending rule not triggered.

**Steps to fix:**

1. Open the booking and go to the **E-mails** tab — check whether the email shows as sent
2. Verify the customer's **email address** is correct in [Customers](https://manual.tourpaq.com/customer/customers)
3. Ask the customer to check their **spam/junk folder**
4. Check [E-mail/SMS Center Statistics](https://manual.tourpaq.com/e-mail-sms-center-statistics) to see the delivery status
5. If the email was never triggered, review the sending rules in [Dynamic E-mail/SMS Center](https://manual.tourpaq.com/email-setup/dynamic-e-mail-sms-center)

***

#### An automated email is firing at the wrong time

**Likely cause:** The trigger condition or timing offset in the Dynamic E-mail/SMS Center is misconfigured.

**Steps to fix:**

1. Go to [Dynamic E-mail/SMS Center](https://manual.tourpaq.com/email-setup/dynamic-e-mail-sms-center) and locate the relevant rule
2. Review the **trigger event** and **timing offset** (e.g. "X days before departure")
3. Check whether **multiple rules** are overlapping and triggering the same email more than once
4. Make a test booking and monitor whether the email fires at the expected time

***

***

### 📤 Export Issues

***

#### An export file is empty or missing expected bookings

**Likely cause:** Filter settings are too restrictive or the export period doesn't match the bookings.

**Steps to fix:**

1. Go to [Export](https://manual.tourpaq.com/export-1/export) and review the **date range and filter settings**
2. Confirm the **Brand** filter includes the bookings you expect
3. Check the booking status filter — cancelled bookings may be excluded by default
4. Try exporting with all filters cleared to see if data appears, then narrow down from there

{% hint style="warning" %}
If you are using the **Legacy Daily Export v1 format**, note that this is deprecated as of v3.1.0 and will be removed in v3.3.0. Migrate to the v2 format as soon as possible.&#x20;
{% endhint %}

***

#### The export file format doesn't match what our supplier expects

**Likely cause:** The wrong export type is selected, or the export hasn't been configured for that supplier.

**Steps to fix:**

1. Confirm with your supplier which **exact format and fields** they require
2. Check all available export types under [Lists](https://manual.tourpaq.com/export-1/lists) and [Extras List](https://manual.tourpaq.com/export-1/extras-list)
3. If a custom format is needed, contact your Tourpaq administrator — custom export configurations may require system-level changes

***

***

### ⚙️ System & Setup Issues

***

#### Changes I made in Setup are not taking effect

**Likely cause:** Changes require a page refresh, cache clear, or may only apply to new bookings (not existing ones).

**Steps to fix:**

1. **Hard refresh** the page after saving: `Ctrl + Shift + R` (Windows) or `⌘ + Shift + R` (Mac)
2. Log out and back in to ensure your session is picking up the latest configuration
3. Note that some setup changes (e.g. pricing rules, allotment) only apply to **new searches or bookings** — existing bookings are not retroactively updated
4. If the change still isn't reflected, contact your administrator to check whether the setting requires a system-level restart or cache flush

***

#### I'm getting an API authentication error

**Likely cause:** Using the deprecated API key method, or the Bearer token has expired.

**Steps to fix:**

1. Confirm you are using **Bearer token authentication** — API key authentication was removed in v3.0.0
2. Check that your token has not expired — tokens must be refreshed periodically
3. Review the integration documentation under [Restful API Authentication](https://manual.tourpaq.com/restful-api-authentication)
4. If you are a third-party developer, contact the Tourpaq administrator for your organisation to issue a new token

***

#### Currency rates are not updating automatically

**Likely cause:** The automatic rate update schedule is not configured, or the external rate feed is unavailable.

**Steps to fix:**

1. Go to [Setup → Currency Rates](https://manual.tourpaq.com/setup/price-currency) and check the current rates and last update timestamp
2. Confirm that automatic rate updates are enabled and the schedule is set correctly
3. If the feed is unavailable, rates can be updated manually by entering them directly
4. Contact your administrator if automatic updates have stopped working unexpectedly

***

***

### 🆘 Getting Help

If you've worked through the relevant steps above and the issue is still unresolved, here's how to get further support:

| Channel               | When to use                                | Contact                                           |
| --------------------- | ------------------------------------------ | ------------------------------------------------- |
| 📧 **Email Support**  | Non-urgent issues, configuration questions | [support@tourpaq.com](mailto:support@tourpaq.com) |
| 💬 **Internal Admin** | Permissions, user access, Brand setup      | Your system administrator                         |
| 🐛 **Bug Reports**    | Confirmed bugs with reproducible steps     | Contact your Tourpaq account manager              |
| 📖 **Full Manual**    | Detailed feature documentation             | [manual.tourpaq.com](https://manual.tourpaq.com)  |

#### When contacting support, always include:

* The **Brand** and **booking number** (if relevant)
* A description of the **steps to reproduce** the issue
* Any **error messages** — copy the exact text or take a screenshot
* The **browser and operating system** you're using

{% hint style="success" %}
&#x20;The more detail you provide upfront, the faster your issue can be resolved. 😊&#x20;
{% endhint %}

