# Setup for Transport Dynamic Packaging (GDS)

## Overview

The **Transport Dynamic Packaging Anchored on Pricelist** feature connects **Tourpaq** to the **GDS system**, allowing the system to book transport services through GDS while selling them under an existing **fixed-price pricelist**.

## Purpose

This functionality ensures that transport bookings made via GDS can be seamlessly integrated into Tourpaq without disrupting predefined pricing structures. It provides a way to leverage the availability and flexibility of GDS while maintaining consistency with the company’s fixed price lists.

## General

GDS transports are available only if the transport is set to use dynamic itineraries.

![](<../.gitbook/assets/image (26)>)

## Legs

When using GDS flights, **Legs** need a general setting like this.

![](<../.gitbook/assets/image (27)>)

![](https://manual.tourpaq.com/~gitbook/image?url=https%3A%2F%2F155167782-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F4ho2ecpjkno5JvDRSja9%252Fuploads%252Fgit-blob-cbc1083b4ceb7ec266cc2235225d2206e11aa000%252Fimage%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%2520%2876%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=315728a6\&sv=2)

The rest of the settings for configuring **Legs** are the same as those used for Real Transports

## Flight Search

Every night, the system is checking for the best flight available for each departure on all transport that uses dynamic itineraries. The system will store timetables, flight numbers, and airlines. When a transport is using OWN real transports and GDS flights, the following list of rules is used to decide when GDS segments are booked instead of OWN segments:

1. Selling of guaranteed seats according to the load matrix (see below)
2. Cost price is lower on GDS
3. GDS price is lower than the “Max price from GDS

The flight found can be viewed under fix quota/view flights:

![](https://manual.tourpaq.com/~gitbook/image?url=https%3A%2F%2F155167782-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F4ho2ecpjkno5JvDRSja9%252Fuploads%252Fgit-blob-cfee9add0e354a7d732698d731638df00844cfb2%252Fimage%2520%282%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%2520%2821%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=5f5e7696\&sv=2)

When a **past reservation** is cancelled, and the **associated flight is no longer active**, the system will automatically trigger the reactivation service to restore the flight. This ensures the booking change can be processed correctly.

Before cancellation:

![](https://manual.tourpaq.com/~gitbook/image?url=https%3A%2F%2F155167782-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F4ho2ecpjkno5JvDRSja9%252Fuploads%252Fgit-blob-4f84a7449dc1c7e9b3d1ea09724195ad3456b982%252Fimage%2520%286%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=adc78f34\&sv=2)

After the booking cancellation, the flight will be reactivated within a few seconds.

![](https://manual.tourpaq.com/~gitbook/image?url=https%3A%2F%2F155167782-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F4ho2ecpjkno5JvDRSja9%252Fuploads%252Fgit-blob-a14a9e95f873f672b426285a68d49fa5eea752c6%252Fimage%2520%287%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=7a1dc76d\&sv=2)

The system automatically reactivates past flights **only** when a change is made to a booking—such as adding or canceling passengers.

* If the service is triggered manually from **Transport → Leg**, it will affect **only future flights**.
* If the service is triggered directly from a **booking**, it will run **only for the specific departure**, regardless of whether the departure date is in the past or future.

![](https://manual.tourpaq.com/~gitbook/image?url=https%3A%2F%2F155167782-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F4ho2ecpjkno5JvDRSja9%252Fuploads%252Fgit-blob-47672f1005f0565672cf7b3d0f0c3ffde3b5dd74%252Fimage%2520%289%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29%2520%281%29.png%3Falt%3Dmedia\&width=768\&dpr=3\&quality=100\&sign=8efc7cac\&sv=2)

## Alternative flights

This feature makes the GDS integration more flexible as it allows more flight options for the same departure dates. These are taken dynamically from GDS.

It is visible in the office. After creating a booking with a GDS transport, when searching for a flight, a forth check box appears. This check box searches only for alternative flights. They are displayed in the same manner as a regular GDS flight, with the exception that the user can now choose which flight he would like to use.
