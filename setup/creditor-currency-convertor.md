# Creditor Currency Convertor

### **Overview / Purpose**

The **Creditor Currency Converter** allows users to convert creditor amounts between different currencies. It ensures that when costs from suppliers (hotels, extras, or discount supplements) are defined in different currencies, the system can automatically recalculate values into the appropriate working currency.

This page is available under:\
**Setup → Creditor Currency Converter**

<figure><img src="../.gitbook/assets/creditor-main-page-9f82fca52cb1aeba549f467970240fc2.png" alt=""><figcaption></figcaption></figure>

### **How It Works**

* When a creditor is changed for **Hotels, Extras, or Discount Supplements**, and the **new creditor uses a different currency** than the previous one, the system automatically creates a new entry in the **Creditor Currency Converter** page.
* These entries define the **currency conversion rules** that allow Tourpaq to calculate consistent prices across different modules.
* For price conversion to take effect, the corresponding rule must be **activated manually** on this page.

<figure><img src="../.gitbook/assets/creditor-currency-convertor-create-e8cbe64c3996bf0b836c8d83884b2a1f.png" alt=""><figcaption></figcaption></figure>

### **Key Features / Functions**

#### **Required Fields** when creating a new converter:

* **Type** – Refers to the entity cost type. Options:
  * Hotel Cost
  * Product Cost
  * Discount Supplement Cost
* **Name** – The name of the selected cost type.
* **From Currency** – The currency to be converted **from**.
* **To Currency** – The currency to be converted **to**.
* **Trigger Price Recalculation on Creditor Change** – When enabled, recalculates prices automatically if the creditor’s currency changes.

### Hotel Currency Convertor Trigger <a href="#hotel-currency-convertor-trigger" id="hotel-currency-convertor-trigger"></a>

<figure><img src="../.gitbook/assets/hotel-creditor-3d7beb8e30273e40dabf227c5c2f46d6.png" alt=""><figcaption></figcaption></figure>

### Extras Currency Convertor Trigger <a href="#extras-currency-convertor-trigger" id="extras-currency-convertor-trigger"></a>

<figure><img src="../.gitbook/assets/extras-creditor-66698e96860b4cfa7bd2200c8c7dc411.png" alt=""><figcaption></figcaption></figure>

#### Discount Supplements Currency Convertor Trigger <a href="#discount-supplements-currency-convertor-trigger" id="discount-supplements-currency-convertor-trigger"></a>

<figure><img src="../.gitbook/assets/disc-supp-creditor-7a1e95924127b87d499e71fb1a7bafe5.png" alt=""><figcaption></figcaption></figure>

### **Examples / Scenarios**

1. **Hotel Supplier Currency Change:**
   * Original creditor currency: EUR
   * New creditor currency: DKK
   * A conversion rule is automatically added to the **Creditor Currency Converter** page (EUR → DKK).
2. **Extra Supplier Update:**
   * An extras supplier switches from SEK to EUR.
   * A new converter entry is created to handle **SEK → EUR** conversions for that extra type.
3. **Discount Supplement Example:**
   * A discount supplement creditor updates from USD to EUR.
   * A rule is created automatically for **USD → EUR** conversion.

<figure><img src="../.gitbook/assets/Untitled (1).png" alt=""><figcaption></figcaption></figure>

### **Notes / Best Practices**

* Price conversion rules must be **activated manually** before they apply.
* Always double-check conversion settings to ensure consistency across bookings and financial exports.
* Keep an eye on automatically created entries when creditors are updated — unused or outdated rules should be cleaned up to avoid confusion.
