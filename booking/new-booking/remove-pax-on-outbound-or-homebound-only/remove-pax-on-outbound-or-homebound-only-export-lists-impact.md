---
hidden: true
---

# Remove pax on outbound or homebound only, Export lists impact

### Overview

This document outlines the steps and expected behavior when exporting lists from the **Export → List** section, specifically focusing on the **No-show** feature and its impact on various report types. The goal is to ensure that exported data correctly excludes passengers flagged as "No-show" based on their travel direction.

### 🔧 Steps & Expected Results

<table data-header-hidden><thead><tr><th width="76.5"></th><th width="360"></th><th></th></tr></thead><tbody><tr><td><strong>Step</strong></td><td><strong>Action</strong></td><td><strong>Expected Result</strong></td></tr><tr><td>1</td><td>Navigate to the <strong>Export</strong> menu and select <strong>List</strong></td><td>The <strong>Hotel Lists</strong> page is displayed</td></tr><tr><td>2</td><td><p>Apply filters to include bookings with <strong>No-show</strong> set.<br><br>From the <strong>Report Type</strong> dropdown, select any of the following report types:</p><ul><li>Passenger list</li><li>Departure homebound</li><li>Transfer list</li><li>Transfer list homebound</li></ul></td><td>A report list is exported</td></tr><tr><td>3</td><td>Check the <strong>Passenger list</strong> export</td><td>Passengers marked as "No-show" on <strong>outbound</strong> will <strong>not be included</strong> in the export</td></tr><tr><td>4</td><td>Check the <strong>Departure homebound</strong> export</td><td>Passengers marked as "No-show" on <strong>homebound</strong> will <strong>not be included</strong> in the export</td></tr><tr><td>5</td><td>Check the <strong>Transfer list</strong> export</td><td>Passengers marked as "No-show" on <strong>outbound</strong> will <strong>not be included</strong> in the export</td></tr><tr><td>6</td><td>Check the <strong>Transfer list homebound</strong> export</td><td>Passengers marked as "No-show" on <strong>homebound</strong> will <strong>not be included</strong> in the export</td></tr></tbody></table>

***

### 📌 Notes

* The **No-show** status impacts passenger visibility depending on the travel direction (**outbound** vs **homebound**).
* Exported data dynamically adapts to exclude any passengers marked as "No-show" for the relevant segment.
* Ensure filters and report types are correctly selected to reflect accurate data exclusions.
