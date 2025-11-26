# SkiStar Sync

The SkiStar Sync feature allows Tourpaq to automatically import **allotment** and **cost prices** from SkiStar’s FixedPeriodProduct API. This sync runs once per day and keeps all SkiStar-managed accommodations up to date inside Tourpaq.

This page explains how the feature works, how it is configured, and how Tourpaq processes the allotment and pricing data.

## **Overview**

The SkiStar integration enables automatic synchronization of accommodation allotment and cost data from SkiStar into Tourpaq. The sync operates daily and retrieves availability for the current or upcoming season based on the defined SkiStar Resort IDs assigned to hotels in the system.

In SkiStar, each property is represented as an individual accommodation unit (house/apartment). Availability is always returned as a free allotment of **1** when an accommodation is available. These accommodations are mapped in Tourpaq as Base Room Types linked to hotels that belong to the relevant SkiStar Resort.

The synchronization performs structured requests to the SkiStar API for all configured travel lengths and Sunday departures within the valid season timeframe, updating prices and allotment for matching accommodations.

## **Purpose**

The purpose of the SkiStar Sync feature is to:

* Ensure Tourpaq always has the **current allotment and cost information** for all SkiStar accommodations.
* Remove the need for any manual maintenance of allotment or costs.
* Guarantee that pricing and availability used in offers, bookings, and operations remain correct throughout the ski season.

Bookings in SkiStar are handled externally and manually. The Tourpaq sync only updates **room availability** and **cost prices**.

## **Expected Behavior**

* Tourpaq performs a **daily synchronization** with SkiStar.
* The sync updates **only**:
  * Allotment
  * Cost price
* If the accommodation/room is **hidden** in Tourpaq, no updates are applied.
* Each SkiStar accommodation corresponds to a **Base Room Type** in Tourpaq where:\
  **Room Code = SkiStar Accommodation ID**
* If the returned currency differs from the Hotel’s creditor currency, a **notification warning** will appear.

## **SkiStar Structure**

SkiStar uses the following data structure:

**Resort → Area → SubArea → Group → Accommodation**

Each **Accommodation** is a **unique unit** (house, apartment). If the accommodation is available, the free allotment is always 1.

## Mapping SkiStar Data into Tourpaq

To integrate SkiStar accommodations into Tourpaq, the following structure is used:

* Each SkiStar **Hotel/Resort** is added in Tourpaq and linked using the corresponding **SkiStar Resort ID**.
* Every SkiStar **Accommodation** is created in Tourpaq as a **Base Room Type**, where:
  * **Room Code = SkiStar Accommodation ID**
* The Base Room Type is then assigned to the correct hotel in Tourpaq.

This setup ensures that each accommodation is individually represented and correctly tied to its parent resort, allowing Tourpaq to work with SkiStar’s hierarchical structure while maintaining precise allotment and availability control.

## **Season Logic**

A SkiStar season is always: **12 December → 20 April (next year)**

The system synchronizes according to the current date:

* **21 April 2025 → 20 April 2026:** sync from _today_ until **20 April 2026**
* **From 21 April 2026:** sync from **12 December 2026 → 20 April 2027**
* And so on for future years.

This ensures that the upcoming ski season is always included.

## **Company & Hotel Settings**

For a company to have access to the SkiStar feature, a SuperAdmin will need to activate this feature for the company.

### **Enable/Disable “SkiStar Sync”**

Once the feature is enabled per company, additional hotel-level fields become available:

### **Hotel Settings**

<figure><img src="../../../.gitbook/assets/image (521).png" alt=""><figcaption></figcaption></figure>

* **Managed by (dropdown) SkiStar** - Appears below “Managed by AvailPro”.
* **SkiStar Resort ID** - Only visible when “Managed by SkiStar” is checked.
* **Stay lengths** \
  Defines which stay lengths should be synced for this hotel.

<figure><img src="../../../.gitbook/assets/image (522).png" alt=""><figcaption></figcaption></figure>

* Example:
  * Sälen: **7,5**
  * Hemsedal & Trysil: **7,5,4**

These settings govern which API calls must be performed for the hotel.

Each hotel may have different stay length rules depending on the Resort.

## **Daily Sync Process**

The daily sync performs the following steps:

### **1. Identify Hotels with SkiStar Resort ID**

All hotels marked “Managed by SkiStar” are included. (currently SkiStar is using 1=Sälen, 4=Hemsedal and 5=Trysil)

### **2. Request Allotment & Cost Data**

For each Resort ID:

1. Determine all relevant **Sundays** (departures) within the synchronization period.
2. For each Sunday, request each configured **stay length**.
3. Use SkiStar endpoint:  **/BookingApi/v1/FixedPeriodProduct/Search**
4. To ensure accurate allotment for shorter stays (5 and 4 days), also retrieve data for the **preceding 7-day period**.

### **3. For each Sunday**

For each resort ID, each possible Sunday is considered as a departure and the specified stay lengths for the hotel are used. Thus, for each resort ID, every possible Sunday is considered a departure and the specified hotel stay durations are used.

The Cost and Allocation for the 7-day period before 5 and 4 days will be obtained and added to ensure the allocation is correct.

Example API load per resort:

```
≈ 18 Sundays × 3 stay lengths ≈ 54 requests per Resort per sync
```

### **4. Retrieve Accommodation Results**

Each response includes:

* Accommodation ID
* Pricing container
* Currency
* Availability (allotment = 1 if available)

### **5. Cost Price Calculation**

The Cost price is calculated using:

```
Cost = prices.gross – prices.commission + mandatoryaddonprice.gross
```

### **6. Currency Validation**

If SkiStar’s currency is different then the Hotel creditor currency → A **Notification Warning** will appear

### **7. Update Tourpaq Rooms**

For each returned accommodation:

* Locate Room by **Room Code = Accommodation ID**

<figure><img src="../../../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure>

For each Accommodation ID found in the response, the system checks if the Accommodation ID exists in Tourpaq and will update the Allocation and Price for the corresponding Room, if it exists. If the Hotel Room is hidden, the system will not update the Cost or Allocation.

### **8. Cost Storage**

* The synchronized cost is stored under **Hotel → Room Costs** as **“Per Room Per Stay”** type.

<figure><img src="../../../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure>

#### <br>
