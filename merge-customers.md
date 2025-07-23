# Merge customers

### 🔐 Availability

This module is available **only for Administrator-type users**.

***

### 📌 Purpose

The **Doublet Customer Management** tool identifies and processes **duplicate customer entries**, based on key matching criteria, and allows administrators to **merge**, **delete**, or **accept** these entries—helping maintain a clean and accurate customer database.

***

### 🧮 Grouping Logic

Customers are automatically grouped by one or more of the following matching criteria:

* 📞 **Phone Number**
* 📧 **Email Address**
* 🏠 **ZIP Code + Address**

Within each group:

* You may **act on the entire group**.
* Or you can create and manage **subgroups** (by selecting specific duplicates).

Once a customer is processed (merged, deleted, or accepted), it will no longer be proposed in future doublet matches—even if newly created duplicates share the same data.

***

### 🛠️ Operations on Doublets

There are **three types of actions** available for handling doublet customer groups:

#### 1. ✅ Merging

**🔹 Full Group Merge:**

* **Step 1**: Select the **radio button** of the customer to **keep** as the main record.
* **Step 2**: Click **Merge**.
* ✅ All bookings from other duplicates are moved to this main customer.
* ✅ Non-overlapping info (e.g., fax, alternate phone) is transferred to the main record.
* ❌ Other customers in the group are **deleted** after the merge.

**🔸 Subgroup Merge:**

* **Step 1**: Use **checkboxes** to select duplicate customers.
* **Step 2**: Inside the selected subgroup, pick one customer with the **radio button**.
* **Step 3**: Click **Merge**.
* ✅ Only the subgroup is processed.
* ✅ The subgroup disappears from the merge proposal.
* ❌ All selected customers are deleted **except** the one retained.

***

#### 2. 🗑️ Deleting

**🔹 Full Group Delete:**

* Click **Delete** without selecting anything.
* ❌ Deletes **all customers** in the group.

**🔸 Subgroup Delete:**

* Select a **subset** using checkboxes.
* Click **Delete**.
* ❌ Only the selected customers are deleted.

***

#### 3. ✔️ Accepting

**🔹 Full Group Accept:**

* Click **Accept** without checking any boxes.
* ✅ All customers are accepted **as separate valid entries**.
* ✅ They won’t appear in future duplicate suggestions.

**🔸 Subgroup Accept:**

* Use **checkboxes** to select a subgroup.
* Click **Accept**.
* ✅ Only selected customers are accepted.
* ✅ Others may remain in the duplicate list.

***

### 🏘️ Special Case: ZIP Code + Address Grouping

* Instead of deleting duplicates, this method **links** all customers in the group.
* A **‘parent customer’** must be selected.
  * All **bonuses and rewards** are redirected to the parent.
  * Linked duplicates still retain **their bookings**.
* On the **parent customer page**, you can:
  * View links to the doublets.
* On the **doublet customer page**, a link to the parent is also available.

📌 **Important:** If any customers in the group have **future bookings**, one of them must become the **parent** during the merge.

<figure><img src=".gitbook/assets/69d3b6e8-726a-421c-ba1c-b4ca7124becd.webp" alt=""><figcaption></figcaption></figure>

### ⚠️ Performance Tips

* For large groups:
  * Perform **several subgroup operations** first.
  * Follow up with a **final group-level action**.
* You can manually **edit customer details** for more refined control before merging.

***

### 📘 Summary Table

| Action | Full Group                    | Subgroup                               |
| ------ | ----------------------------- | -------------------------------------- |
| Merge  | Merges all to 1, deletes rest | Merges selected to 1, deletes selected |
| Delete | Deletes entire group          | Deletes only selected                  |
| Accept | Keeps all, skips future match | Accepts selected, skips future match   |

***

Let me know if you'd like a PDF version or internal help page layout with screenshots!
