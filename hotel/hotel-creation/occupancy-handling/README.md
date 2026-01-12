# Occupancy / Handling

### Overview

The **Occupancy Handling** feature lets you control how rooms can be sold. It supports flexible occupancy rules and single-occupancy pricing.

Where to find it: **Hotel → Room costs → Occupancy / Handling**.

{% hint style="info" %}
This feature must be enabled **per company** before you can use it.
{% endhint %}

### What you can configure

#### Room restrictions

* Define valid bed combinations for each room type.
* Prevent unsupported room configurations from being booked.
* Ensure consistency between hotel capacity and booking options.

See [Room Restriction](room-restriction.md).

#### Different maximum occupancy (Max Pax)

* Set multiple maximum occupancy limits for the same room type.
* Fine-tune availability per configuration.
* Example: A double room can be sold as **2 adults + 1 child** or **3 adults**.

See [Different Max Pax](different-max-pax.md).

#### Single room cost

* Apply pricing adjustments when a room is booked for single occupancy.
* Supports two options:
  * **Fixed amount** supplement.
  * **Percentage-based** supplement.

See [Single Room Cost](single-room-cost.md).

#### Single room supplement

* Automatically applies a supplement when a double room is used for single occupancy.
* Configure the supplement as:
  * **Fixed price**
  * **Percentage of room cost**

See [Single Room Suplement](single-room-suplement.md).

### Benefits for agencies

* **Increased flexibility:** Customize room offerings based on actual usage.
* **Improved pricing accuracy:** Adjust costs for single vs. multiple occupancy.
* **Better availability management:** Reflect real-world capacity more precisely.
* **Optimized sales:** Prevents booking errors and maximizes room utilization.

### FAQ

**Q: Why can’t I see or use Occupancy / Handling?**\
**A:** It must be enabled **per company**. If you don’t have access, ask your system admin.

**Q: What’s the difference between “Single Room Cost” and “Single Room Supplement”?**\
**A:** Both are used for single occupancy pricing, but they are configured in different places and can behave differently. Use the setup that matches your pricing model. See [Single Room Cost](single-room-cost.md) and [Single Room Suplement](single-room-suplement.md).

**Q: How do I block an invalid bed/room setup from being booked?**\
**A:** Use [Room Restriction](room-restriction.md) to define the allowed combinations.

**Q: Can the same room type have different Max Pax values?**\
**A:** Yes. Use [Different Max Pax](different-max-pax.md) and manage availability per configuration.

**Q: Where do I set availability for each Max Pax configuration?**\
**A:** Availability is managed per day in **Hotel → Allotment Per Day**. See [Different Max Pax](different-max-pax.md).

**Q: Should I use a fixed amount or a percentage for single occupancy pricing?**\
**A:** Use **fixed amount** when the uplift is constant. Use **percentage** when it should scale with the room price.
