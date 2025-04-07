# Introduction

### Purpose <a href="#purpose" id="purpose"></a>

Transport Dynamic Packaging Anchored on Pricelist is connecting Tourpaq to the GDS system and enables it to book transport over GDS and sell it under an existing pricelist (fix price). This document specification describes how this feature works in Tourpaq.

### Goals <a href="#goals" id="goals"></a>

1. eliminate empty leg flights
2. lower costs on prorate seats and lower the need of using guarantee seats
3. dynamically pack transport anchored on a pricelist
4. enable the system to define round-trips and hotel combinations

### Definitions <a href="#definitions" id="definitions"></a>

City pair (Leg): any pair of valid airports IATA codes eg: BLL-AYT

Segment: direct flight

Flight: one or more segments linked to make up a travel between cities of a city pair
