# Price currency

### Currency rate <a href="#currency-rate" id="currency-rate"></a>

#### Overview

The system allows administrators to configure and manage currency rates used across the company and its brands. Currency settings impact how totals and statistics are displayed in bookings, ensuring consistent reporting and calculations.

#### Purpose

This feature provides flexibility in handling multi-currency operations by allowing rates to be created, updated, or removed, while defining default currencies at both **company** and **brand** levels.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

#### Managing Currency Rates

* **Create a Currency Rate**
  1. Navigate to **Setup → System Setup → Currency** tab.
  2. Click **Add**, enter the new rate, and press **Save**.
* **Delete a Currency Rate**
  * In the same tab, select the rate and click **Delete**.

#### Setting Default Currencies

* **Company Currency**
  * Go to **System → System Setup → General Information**.
  * Choose the company’s default currency from the **Default Currency** dropdown.
* **Brand Currency**
  1. Navigate to **Users → Brands**.
  2. Click **Edit** next to the brand.
  3. Select the desired currency code from the **Currency** dropdown.

Currency in Bookings

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

* **Totals Panel**
  * The totals are displayed in the currency of the selected brand (from the **Brand** dropdown in the top-left).
  * If **All Brands** is selected, totals are converted into the **Company Currency** and shown with the company’s currency code.
* **Statistics Panel**
  * Open the **Statistics** tab under **View All Bookings & Statistics**.
  * If **Additional Sales per Seller / Turnover** is checked, totals appear in the selected brand’s currency.
  * If **All Brands** is selected, totals are converted into the **Company Currency**.
