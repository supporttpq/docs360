# Remove (Undo) Stop Sale

**Setup**

| Steps                                                                                          | Expected Results                                                                                                                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Go to "Hotel" menu -> "Stop Sales"                                                          | <p>Stop sales page is displayed<br>All stop sales defined in the system are listed with filter on "Start/End date" set as current date by default</p>                                                                                                                                                                 |
| 2. Filter the list if necessary to bring the desired stop sale rule and choose an enabled one. | Result list is displayed according to filters used                                                                                                                                                                                                                                                                    |
| 3. Press "Edit" button                                                                         | New "Remove or Split" button is displayed.![](<../.gitbook/assets/image (172).png>)                                                                                                                                                                                                                                   |
| 4. Press "Remove or Split"                                                                     | <p>A new dedicated section is displayed underneath.<br>"Remove" checkbox is displayed but disabled while stop sale rule is still enabled; Info button displays explanatory text "This will remove the stopsale and enable the initial allotment" on hover . <img src="../.gitbook/assets/image (173).png" alt=""></p> |
| 5. Mark the "Remove" checkbox"                                                                 | Checkbox is checked                                                                                                                                                                                                                                                                                                   |
| 6. Press "Save" button                                                                         | Rule is updated and saved. Remove or split section is closed. Rule is not in edit mode anymore                                                                                                                                                                                                                        |
| 7. After step 6 press "Cancel"                                                                 | Updates are not saved. Remove or split section is closed.                                                                                                                                                                                                                                                             |

**Check results in Stop sales logs**

| Steps                                          | Expected Results                                                                                                           |
| ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| 1. After step 6 in setup, press "View details" | Stop sales logs page is displayed, having the filters automatically set by default for the period and room set on the rule |
| 2. Check records                               | Initial r.No is the final R no after stop sale was enabled, and Final r. no is the initial allotment set before stop sale  |
|                                                |                                                                                                                            |

**Check results in Allotment per day on hotel**

| Steps                                                                                          | Expected Results                                                 |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| 1. After step 6 in setup, go to hotel edit page                                                | Edit page of the hotel is displayed                              |
| 2. Go to "Allotment per day" tab and filter the dates and room according to stop sale rule set | Allotment per day for the room is displayed                      |
| 3. Check allotment                                                                             | Main allotment is restored to initial allotment before stop sale |

**Check results in Pricelist**

| Steps                                                        | Expected Results                                                                                    |
| ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| 1. After step 6 in setup, go to Pricelist menu -> Pricelist  | Edit page of the hotel is displayed                                                                 |
| 2. Filter the dates and room according to stop sale rule set | Corresponding pricelists are listed                                                                 |
| 3. Check FHA                                                 | FHA is populated with available number of rooms according to initial allotment set before stop sale |
