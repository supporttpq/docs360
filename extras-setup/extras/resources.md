# Resources

### Overview Tab

The resource tab is used to limit the availability of an extra. This is mainly due to the fact that certain products are available only to certain transports, destinations or hotels.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

The limit number of resources that can be added is 100. If the number of resources of the same type exceeds this number, a warning message will appear at the bottom of the page.

<figure><img src="../../.gitbook/assets/image (420).png" alt=""><figcaption></figcaption></figure>

### Workarounds

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

**Arrival Airport** resource for products is not recognized by the old webbooking. The use of this resource is not recommended for companies using the old webbooking.

> Combining multiple resource filters **types** behaves differently in Tourpaq, as follows:

> combining with **AND** condition

* For a product with both Hotel and Transport (or other) resources => offer has the product eligible ONLY IF it contains one of the Hotels **AND** one of the Transport resources center round important 60%>

> combining resources with **OR** condition

* For a product with both Hotel and Transport (or other) resources => offer has the product eligible ONLY IF it contains one of the Hotels **OR** one of the Transport resources

This behavior is available by default to all the other companies in the system. It can be set on System Setup -> General Information -> Other Settings

<figure><img src="../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

### **Resources Overview:**

| Resource Type           | Description                                                |
| ----------------------- | ---------------------------------------------------------- |
| **Arrivals**            | Shows which arrival was added as resources                 |
| **Resorts**             | Specifies the resorts associated as resources              |
| **Hotels**              | Specifies the hotels associated as resources               |
| **Transports**          | Specifies the transports associated as resources           |
| **Rooms**               | Associates the room types as resources                     |
| **Real transports**     | Specifies the real transports associated as resources      |
| **Arrival airport**     | Specifies the arrival airports associated as resources     |
| **Destinations**        | Specifies the destinationss associated as resources        |
| **Transport Suppliers** | Specifies the transport supplierss associated as resources |

Each section has an **Edit** button allowing detailed configuration for that specific resource.

***

### How to Configure

1. **Click on the `Edit` button** for the desired resource type.
2. **Select the appropriate values** (e.g., choose a specific hotel, transport segment, or destination).
3. **Save** your selection using the "Save" button at the bottom of the page.
4. If changes are not required, click **Cancel** to discard.
