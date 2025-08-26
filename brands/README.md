# Brands

### **Overview / Purpose**

The **Brands Management** section allows administrators to define, organize, and manage brands within the Tourpaq system. Each brand contains metadata that is used for **display, booking identification, and contact handling**. Proper configuration ensures bookings are associated with the correct brand and that brand-specific rules are applied consistently.

***

### **How It Works**

* Each brand entry stores information such as **name, parent company, address, and booking ID ranges**.
* Brands can be displayed or hidden in the user interface depending on administrative needs.
* Special flags (e.g., “Use Contact Info in List”) control whether contact details are shown in relevant lists.
* Brands are directly tied to **payment rules, booking visibility, and system behavior**.
* Administrators can **create, edit, or delete brands** while ensuring booking ID ranges remain unique.

<figure><img src="../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

### **Key Features / Functions**

#### **Table Columns Explained**

* **Name**: The brand’s name, used for display internally or publicly.
* **Company**: The parent company associated with the brand.
* **Address**: The brand’s physical office address.
* **Place**: Postal code and city of the brand.
* **Booking IDs From / To**: The numeric range of booking IDs assigned to this brand. Ensures bookings are linked correctly.
* **Use Contact Info in List**: Checkbox that determines whether the brand’s contact information is displayed in system lists.\
  &#xNAN;_&#x56;alues: Checked = Yes, Unchecked = No_
* **Is Hidden**: Indicates brand visibility in the user interface.\
  &#xNAN;_&#x47;reen check (✓) = Hidden, Red cross (✘) = Visible_
* **Payment Rules**: Link to view or configure payment-related rules specific to the brand.
* **Delete Icon**: Trash bin icon that removes the brand from the system.

***

### **Notes / Best Practices**

* Ensure **booking ID ranges do not overlap** across brands to avoid mislinked bookings.
* Only enable **“Use Contact Info in List”** if brand details are required in search results or reports.
* Regularly **review hidden brands** to confirm correct visibility settings.
* Keep brand metadata (company, address, payment rules) updated to ensure accurate reporting and communication.
