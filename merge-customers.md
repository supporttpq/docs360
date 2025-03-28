---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Merge customers

Available for Administrator type of user.

Customers are displayed in groups based on:

* the phone number,
* e-mail address and
* by ZIP code and address. Actions in this group will have a slightly, different outcome, please read about it here. Allows the merging, deleting and accepting of customers from the same group. Also, subgroups can be formed inside a bigger group.

**After a customer has been processed, that customer will no longer appear as a merge proposal in the future**. If similar (by merge criteria) customers will be created, the merge proposals will not include the previously merged customers.

### Usage tips for dublet customer management

There are three operations that can be applied on dublet customers and two work scenarios. You can work on the entire group proposal or you can create a subgroup within this group by checking the dublet customers that should belong to the subgroup.

The operations are:

**Merging**

* **Group** - select a radio button of the customer that is to remain in the system as a single representative of the group and click the Merge button. All the other customers will have their bookings moved to this customer, details that they have and the remaining customer does not (e.g., fax number, etc) will be ported to the remaining customer and they will be deleted.
* **Subgroup** - use checkboxes to determine the subgroup, then select a radio button inside the subgroup for the customer to be merged. After the merge, all the subgroups disappear from the merge proposal, and all the customers within the subgroup will be deleted from the system except the remaining customer.

**Deleting**

* **Group** - do not check anything, you can directly click the Delete button and all the customers inside the group will be deleted from the list.
* **Subgroup** - use the checkboxes to determine the subgroup to be deleted and click the delete button. Similar behavior as on group delete.

**Accepting**

* **Group** — click the Accept button and all the customers inside the group will be accepted as individual customers inside the system, they will not be deleted, only that they will not appear in the merge proposal anymore.
* **Subgroup** — use the checkboxes to determine the subgroup and click the Accept button. Similar behaviour as in the group accepted.

### Special behavior of ZIP code and address merging

By using this type of grouping, doublet customers are not deleted, but instead are linked to the customer that is selected as merge source. The other customers can still be accessed and also keep their bookings, but all bonuses are sent to the 'parent customer'.

When accessing the 'parent' customer page, links will be present to the doublet customers. Similar link to the 'parent' is also present in the dublet customer page.

<figure><img src=".gitbook/assets/69d3b6e8-726a-421c-ba1c-b4ca7124becd.webp" alt=""><figcaption></figcaption></figure>

If in a group, some customers have bookings in the future, one of these must become the 'parent'.

**Please note!** To prevent page blockage or heavy work on the database, on big doublet groups, you can have several subgroup operations followed by a final group operation. For finer adjustments, you can edit the customer's, details.
