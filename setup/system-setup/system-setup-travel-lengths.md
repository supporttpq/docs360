---
description: Configure trip-duration intervals for offer selection.
---

# System Setup – Travel Lengths

### Overview

**Travel Lengths** defines trip-duration intervals for offer selection.

In **Select Offer**, these intervals categorize trips by the number of travel days. They support the travel-length criterion in [Create new offer](../../offers/create-new-offer.md).

### Purpose

Use **Travel Lengths** to standardize duration groups across brands and agencies. The configured ranges affect offer filtering and categorization.

### Requirements

Before configuring an interval, meet these requirements:

* Administrator access to **System Setup**.
* Defined, non-overlapping duration ranges for the required offer categories.

### Navigation

In Tourpaq Office, open **Setup → System Setup → Travel Lengths**.

### Interface overview

The page lists configured travel-duration intervals. Use **Add** to create an interval, then save the range.

### Field descriptions

| Field         | Description                                                                                                                                                  |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Days From** | Required for a custom interval. Sets the first travel day included in the range. This value works with **Days To** when **Select Offer** categorizes offers. |
| **Days To**   | Required for a custom interval. Sets the final travel day included in the range. This value must not overlap another configured interval.                    |
| **Add**       | Creates a new interval entry. Select this before entering **Days From** and **Days To**.                                                                     |
| **Save**      | Stores the configured interval. The saved range becomes available for offer selection.                                                                       |

### Configuration steps

To add a travel-duration interval:

1. In **Travel Lengths**, click **Add**.
2. In **Days From**, enter the first day in the range.
3. In **Days To**, enter the final day in the range.
4. Click **Save**.

### System behavior

If no custom interval exists, Tourpaq uses a seven-day travel duration.

Tourpaq applies saved ranges when **Select Offer** categorizes available offers. Reload **Select Offer** to display a saved interval.

Overlapping ranges can produce unclear duration categorization.

### Examples

To create a three-to-seven-day interval:

1. Enter `3` in **Days From**.
2. Enter `7` in **Days To**.
3. Click **Save**.

This interval groups offers with travel durations from three through seven days.

### Related pages

* [Create new offer](../../offers/create-new-offer.md) explains offer search criteria.
* [System Setup](./) describes company-wide configuration.
