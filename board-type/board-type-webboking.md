# How to use a Board Type

## How to use a Board Type

### Overview

This page walks through a complete example of setting up and using a [.](./ "mention"), from initial configuration through to how it appears on a booking and its ticket.

The example covers two parts:

* **Setup** — creating the Hotel Allotment, the Extras Category, and the Board Basis and Board Supplement extras that represent the board type.
* **Booking** — searching Webbooking, adding a passenger, and confirming how the board type and any Board Supplement upgrade appear on the booking and the generated ticket.

```mermaid
flowchart TD
subgraph SETUP["Setup"]
A1["1. Create a Hotel Allotment<br/>Configures the Board Basis for the period, the board included in the room price"]
A2["2. Create an Extras Category<br/>Type equals Pension, required for Board Basis and Board Supplement extras"]
A3["3. Create extras for Board Types<br/>Board Basis plus Board Supplement, tied together by the Board type field"]
A1 --> A2 --> A3
end
subgraph BOOKING["Booking"]
B1["4. Open Webbooking<br/>Search hotel and dates, included board and eligible upgrades appear"]
B2["5. Add passenger details<br/>Enter the traveller information for the booking"]
B3["6. Confirm extra availability<br/>The Board Type extra is shown as an eligible upgrade"]
B4["7. Finish the booking<br/>The booking is finalized and saved"]
B5["8. Open the ticket<br/>The generated ticket shows the board type in the hotel section"]
B6["9. Verify extra details in the ticket<br/>The hotel section lists the board extra and its details"]
B1 --> B2 --> B3 --> B4 --> B5 --> B6
end
A3 -. Board type field matches .-> B3
```

### 1. Create a Hotel Allotment

Create a Hotel Allotment for the room type. Configure its Board Basis for the relevant period. This setting determines the board included in the room price.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2).png" alt="Hotel Allotment grid with the Board Basis column set to HB"><figcaption></figcaption></figure></div>

### 2. Create an Extras Category

Create an Extras Category with the type Pension. Board Basis and Board Supplement extras must belong to a category of this type.

### 3. Create extras for Board Types

Create a Board Basis extra for the board included in the room price, and a Board Supplement extra for any upgrade. The **Board type** field identifies the board represented by the extra. Tourpaq uses this field to match extras on the web and support upgrades. The **Board basis filter** limits a Board Supplement extra to rooms with a matching Board Basis. For example, create a Breakfast (BB) Board Basis extra, then create an All Inclusive Board Supplement extra with **Board basis filter** set to Breakfast.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2).png" alt="Board Type extra configuration"><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2) (1) (1).png" alt="Board Type extras list"><figcaption></figcaption></figure></div>

### 4. Open Webbooking

Open Webbooking. Search for the hotel and travel dates. Rooms appear with the Board Basis included in the price and eligible Board Supplement upgrades.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (5) (1) (3).png" alt="Webbooking platform"><figcaption></figcaption></figure></div>

### 5. Add passenger details

Enter passenger details.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (6) (1) (2).png" alt="Passenger details in Webbooking"><figcaption></figcaption></figure></div>

### 6. Confirm extra availability

Tourpaq shows the Board Type extra as an eligible option.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (7) (1) (3).png" alt="Board Type extra in the Webbooking list"><figcaption></figcaption></figure></div>

### 7. Finish the booking

Finalize the booking. The booking is saved successfully.

### 8. Open the ticket

Open the generated ticket. The ticket shows the board type in the hotel section.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (8) (5).png" alt="Board Type in the hotel section of a ticket"><figcaption></figcaption></figure></div>

### 9. Verify extra details in the ticket

The ticket's hotel section shows the board type together with the extra's details.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (9) (5).png" alt="Board Type extra details in a ticket"><figcaption></figcaption></figure></div>
