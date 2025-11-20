# Introduction

### **Overview**

Real Transport provides a hybrid model that combines dynamic GDS availability with the stability of predefined pricelist prices. Instead of relying solely on preconfigured flights or guarantee seats, the system retrieves live transport options from the GDS and constructs valid round-trip combinations at the moment of booking.

The feature allows Tourpaq to:

* Automatically retrieve available outbound and return flights from the GDS.
* Match flights to the travel dates and city pairs defined in the pricelist.
* Build complete travel packages that follow predefined business rules (minimum/maximum stay, hotel pairing, transport rules).
* Sell GDS flights at the fixed prices specified in the pricelist, independent of the underlying flight cost.
* Reduce reliance on empty-leg flights, minimize guaranteed seat usage, and optimize prorated seat purchasing.

By anchoring the dynamic transport to an existing pricelist, Tourpaq maintains commercial control and pricing consistency while gaining the flexibility and efficiency of real-time transport sourcing.

### **Purpose**

Transport Dynamic Packaging Anchored on Pricelist integrates Tourpaq with the GDS system, enabling the system to dynamically book real-time transport options while selling them under an existing pricelist (fixed price).\
This document describes how the feature works, how transport combinations are created, and how they interact with the Tourpaq booking and pricing structure.

### **Goals**

The primary goals of Transport Dynamic Packaging Anchored on Pricelist are:

* To eliminate empty-leg flights.
* To reduce costs associated with prorated and guarantee seats.
* To dynamically pack transport while maintaining fixed pricing.
* To support round-trip creation and valid hotel combinations within a single booking flow.

### **Definitions**

* **City pair (Leg):** A pair of valid IATA airport codes representing a travel route (e.g., BLL–AYT).
* **Segment:** A single direct flight.
* **Flight:** One or more linked segments creating a complete journey between the airports of a city pair.
