# Remove (Undo) Stop Sale

#### Overview

This feature allows you to reverse a previously applied **Stop Sale** rule for a hotel room (i.e. re-enable availability that had been blocked).

#### Purpose

If you temporarily marked a room or date range as unavailable using Stop Sale, “Remove (Undo) Stop Sale” restores its original allotment and availability. Use it when you no longer want to block bookings for those rooms/dates.

#### Field & Section Explanations

| Name / Section              | What It Does / Notes                                                                                                          |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Stop Sales List**         | Shows all active Stop Sale rules in your system, filtered by current dates by default.                                        |
| **Edit button**             | Opens the rule so you can apply changes (remove or split).                                                                    |
| **Remove or Split section** | Appears when editing a rule. Here you can choose to fully remove or modify part of the stop sale.                             |
| **Remove checkbox**         | When selected, undoes the Stop Sale entirely and restores the original allotments. (Initially disabled while rule is active.) |
| **Info button (tooltip)**   | Hover to see explanation: _“This will remove the Stop Sale and enable the initial allotment.”_                                |

***

#### Instructions: How to Use Remove (Undo) Stop Sale

1. **Navigate to the Stop Sales page**\
   Go to **Hotel → Stop Sales** from the main menu.\
   The page displays all defined Stop Sale rules, filtered by current dates by default.
2. **Find the rule you want to undo**\
   Use filters (e.g. date range, room type) if necessary to narrow down the list.\
   Select an **enabled** Stop Sale rule to edit.
3. **Click “Edit”**\
   This opens the rule’s configuration. A **Remove or Split** section will appear beneath it.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. **Enable the “Remove” option**\
   Initially, the **Remove** checkbox is disabled (while the rule is still active).\
   Once editable, check the **Remove** box.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

5. **Save your changes**\
   Click **Save**.\
   The rule is updated, the “Remove or Split” section closes, and the rule returns to non-edit mode.
6. **(Optional) Cancel changes**\
   If you press **Cancel** instead of Save, no updates are made, and the section closes without changes.

***

#### What to Check After Removing the Stop Sale

Once you’ve undone the Stop Sale, verify that everything reverted as expected:

* **Stop Sales Logs**\
  Go to **Stop Sales Logs → View details**.\
  You should see entries:
  * _Initial r.No_ = the final record number used when Stop Sale was first enabled
  * _Final r.No_ = the original allotment number before the Stop Sale
* **Hotel — Allotment per Day tab**\
  Open the hotel’s edit page, and go to **Allotment per Day**.\
  Filter by the room and dates you were working on.\
  The allotment values should reflect the pre-Stop Sale values.
* **Pricelist**\
  In the **Pricelist**, filter by hotel, dates, and room type.\
  The FHA (free-hotel-allotment) field should now display the original number of available rooms, as it did before the Stop Sale was applied.
