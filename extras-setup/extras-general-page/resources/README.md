# Resources

### Overview

The resource tab is used to limit the availability of an extra. This is mainly due to the fact that certain products are available only to certain transports, destinations or hotels.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Resources tab for an Extra."><figcaption></figcaption></figure></div>

The limit number of resources that can be added is 100. If the number of resources of the same type exceeds this number, a warning message will appear at the bottom of the page.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Warning for the maximum number of resources."><figcaption></figcaption></figure></div>

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

When an extra has more than one resource type, the **Product Resourser Type** setting decides how they are combined. Set it in **System Setup -> General Information -> Other Settings**.

* **AND** – the booking must match **every** resource type on the extra.
* **OR** – the booking must match **at least one** resource type on the extra.

**Example:** an excursion has the resources Resort **Rhodos** and Hotel **City Hotel**.

| Booking                   | AND           | OR            |
| ------------------------- | ------------- | ------------- |
| City Hotel, Rhodos        | ✅ Offered     | ✅ Offered     |
| Another hotel in Rhodos   | ❌ Not offered | ✅ Offered     |
| A hotel in another resort | ❌ Not offered | ❌ Not offered |

The setting also applies to Extra Orders in the Guide App and Guest App. An excursion that does not match the booking is not offered, and an order for it is refused with the message _Product \<name> can't be booked for this booking!_

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/image (277).png" alt="Resource filter settings."><figcaption></figcaption></figure></div>

### Resources overview

| Resource Type           | Description                                                                                                          |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Arrivals**            | Shows which arrival was added as resources                                                                           |
| **Resorts**             | Specifies the resorts associated as resources                                                                        |
| **Hotels**              | Specifies the hotels associated as resources                                                                         |
| **Transport Modes**     | Allow the resource to distinguish between different transport modes (Bus, Car, Fly, Train)                           |
| **Transport Types**     | Allow the resource to distinguish between different types of Transport (Charter, Dynamic, SysReal, System Transport) |
| **Transports**          | Specifies the transports associated as resources                                                                     |
| **Rooms**               | Associates the room types as resources                                                                               |
| **Real transports**     | Specifies the real transports associated as resources                                                                |
| **Arrival airport**     | Specifies the arrival airports associated as resources                                                               |
| **Destinations**        | Specifies the destinations associated as resources                                                                   |
| **Transport Suppliers** | Specifies the transport suppliers associated as resources                                                            |
| **Use as excluded**     | If checked, the extras are eligible for all except the listed resources.                                             |

Each section has an **Edit** button allowing detailed configuration for that specific resource.

***

### How to configure

1. For the desired resource type, click **Edit**.
2. **Select the appropriate values** (e.g., choose a specific hotel, transport segment, or destination).
3. **Save** your selection using the "Save" button at the bottom of the page.
4. If changes are not required, click **Cancel** to discard.
