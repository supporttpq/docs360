# Attributes

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

### **Overview**

This page provides details on how to configure and manage attributes for the extra product. The attributes section allows users to assign specific tags or labels that describe or influence how the product behaves or is displayed across brands.

### **Navigation Path**

**Menu > Product > Extra > Attributes Tab**

Users can choose one or more of the attributes defined in the [Extras Attributes](../../extras-attributes.md). The limit number of resources that can be added is 100. If the number of resources of the same type exceeds this number, a warning message will appear at the bottom of the page.

<figure><img src="../../.gitbook/assets/image (419).png" alt=""><figcaption></figcaption></figure>

#### Workarounds

It is recommended to analyze whether the configuration can be optimized before applying the change. The following workarounds can help reduce the number of resources and improve performance:

* **Review unnecessary resources:**\
  Check if some of the resources included in the filter are not actually needed. Remember that filtering is used to _restrict_ what matches.
  * If there are **no hotels** listed in the resources, then **all hotels match**, meaning there is effectively no limitation.
  * The same principle applies to other resource types (e.g., transports, resorts).
* **Use as Excluded:**\
  The **Exclude** option specifies that there is _no match_ for the listed resources. In some cases, it is more efficient to exclude a few items than to include many.
* **Use Transport Supplier filtering:**\
  In scenarios where many transports are listed individually, consider filtering by **Transport Supplier** instead. This can greatly simplify the setup and reduce the number of entries.
* **Filter on a higher level:**\
  Sometimes filtering can be done more efficiently at another level. For example, specifying a **number of arrivals** can be simpler and faster than defining filters for many individual resorts.
* For extras used for transportation seating (SEAT products), the limitation has been removed.

An attribute will appear automatically on the Ticket and in Customer Centre. It allows the guests to influence the behaviour of the extra or select a product that fits them. (Example: A Sky equipment product can have an attribute with the height of the guest so that the suppliers or the agency can know what lenght the sky equipment will be needed for the guest).

Hotel Lists, Extra Lists and Vouchers will also display the attribute if they are selected.

User can select start day from drop-down list, in Edit Passenger for a certain booking, if the extras has an attribute for this already defined and Extras has in Prices, at field Days, a number of days defined.

More information can be found in [Extras Attributes](../../extras-attributes.md).

### **Attributes Section**

The _Attributes_ tab displays all current tags or characteristics assigned to the product.

#### **Fields:**

* **Attributes**: Displays the current attribute(s) applied. In this example, the attribute is:\
  &#xNAN;**→ Birthday**\
  This could relate to special configurations, offers, or logic specific to birthday-related services.
* **Edit Button**: Click this button to open the attribute editor and modify existing attributes or add new ones.
* **Automatically Select Default Attribute Value**:\
  A checkbox that, when enabled, will automatically apply a default value for the attribute during usage (e.g., during booking or offer creation).
