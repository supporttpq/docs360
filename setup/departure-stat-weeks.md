# Departure stat weeks

### **Overview / Purpose**

The Year Definition feature allows administrators to configure **departure statistic weeks** for each brand. These definitions determine how weekly reporting and statistics (such as sales, departures, and occupancy) are grouped and displayed in Tourpaq.

If no specific year interval is set for a brand, the system will apply the **Default interval** (if one is defined). This ensures consistency in statistical reporting across all brands.

### **How It Works**

* A year can be defined **per brand** via the agency selector in the upper-right dropdown.
* The definition includes:
  * A **Year Value** (e.g., 2026).
  * An optional **Start/End Period** that sets the range of weeks for the year.
* If **“Set as Default interval”** is enabled, the year definition acts as the fallback for brands without their own configuration.
* The system then calculates **departure statistic weeks**, beginning with the first day of the defined year and ending with the first day of the last week.

### **Key Features / Functions**

* **Agency Selection:** Choose the brand/agency for which the year definition applies.
* **Year Value:** Input the numeric year used in reporting (e.g., 2026).
* **Set as Default Interval (optional):** Allows other brands without a year defined to inherit this interval.
* **Define Start / End Period (optional):**
  * Ensures statistics follow business-specific periods (e.g., seasonal calendars).
  * The first week begins on the selected start date.
  * The last week starts on the chosen end date.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Examples / Scenarios**

1. **Default Year Setup:**\
   Brand A has no year defined. A Default Year is set from **01-01-2026 to 27-12-2026**, so Brand A automatically uses this setup.
   * First departure stat week: **05-01-2026 → 11-01-2026**
   * Last departure stat week: **Starts 27-12-2026**
2. **Custom Year Definition:**\
   Brand B defines its own year interval for 2026: **15-12-2025 to 13-12-2026**.\
   This ensures reporting matches the company’s operational year (not the calendar year).
   * First departure stat week: **15-12-2025 → 21-12-2025**
   * Last departure stat week: **Starts 13-12-2026**
