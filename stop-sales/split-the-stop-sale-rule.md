# Split the Stop Sale Rule

**Setup**

| Steps                                                                                          | Expected Results                                                                                                                                                                                                                                                                                          |
| ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Go to "Hotel" meu -> "Stop Sales"                                                           | <p>Stop sales page is displayed<br>All stop sales defined in the system are listed with filter on "Start/End date" set as current date by default</p>                                                                                                                                                     |
| 2. Filter the list if necessary to bring the desired stop sale rule and choose an enabled one. | Result list is displayed according to filters used                                                                                                                                                                                                                                                        |
| 3. Press "Edit" button                                                                         | New "Remove or Split" button is displayed.                                                                                                                                                                                                                                                                |
| 4. Press "Remove or Split"                                                                     | <p>A new dedicated section is displayed underneath.<br></p>                                                                                                                                                                                                                                               |
| 5. Fill the "Record number to split stop sale in"                                              | <p>Acccording to number of records set, the same number of new lines will be displayed to edit the rule.<br>Each entry is set by default with Start&#x26;End dat as initial rule, having the "Enable" checkbox marked.</p>                                                                                |
| 6. Set the desired periods and actions (remove/agreed allotment)                               | <p>Split works in any combination:<br>There are two validations set:<br>- for the split rules to cover the exact period interval of the initial/parent rule<br>- the split rule to not have overlapping periods</p>                                                                                       |
| 7. Press "Split" button                                                                        | <p>Rule is updated and saved. Remove or split section is closed. Rule is not in edit mode anymore. Stop sale page is refreshed.<br>If validations are not passed, Error message is displayed and split is not done.<br>On the stop sales page, now each split rule is displayed as a stand-alone rule</p> |
| 8. After step 6 press "Cancel"                                                                 | Updates are not saved. Remove or split section is closed.                                                                                                                                                                                                                                                 |

**Check results in Stop sales logs**

| Steps                                                        | Expected Results                                                                                                           |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| 1. After step 7 in setup, press "View details" for each rule | Stop sales logs page is displayed, having the filters automatically set by default for the period and room set on the rule |
| 2. Check records                                             | Initial R .No and Final R no are updated according to setup (removed, agreed allotment)                                    |

**Check results in Allotment per day on hotel**

| Steps                                                                                             | Expected Results                                                                        |
| ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| 1. After step 7 in setup, go to hotel edit page                                                   | Edit page of the hotel is displayed                                                     |
| 2. Go to "Allotment per day" tab and filter the dates and room according to stop sale rules split | Allotment per day for the room is displayed                                             |
| 3. Check allotment                                                                                | Main allotment is updated according to setup on split rules (removed, agreed allotment) |

**Check results in Pricelist**

| Steps                                                                          | Expected Results                                                                                              |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| 1. After step 7 in setup, go to Pricelist menu -> Pricelist                    | Edit page of the hotel is displayed                                                                           |
| 2. Filter the dates and room according to stop sale rules resulted after split | Corresponding pricelists are listed                                                                           |
| 3. Check FHA                                                                   | FHA is populated with available number of rooms according to setup on split rules (final r no - booked rooms) |
