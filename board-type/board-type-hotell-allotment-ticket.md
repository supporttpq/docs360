# Board Type - Hotell allotment / Ticket

To be able to use the board type in hotel allotment, you should have defined one or more board types in Extras.&#x20;

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

For every allotment, it shall be possible to specify the default BOARD type. The possible options are the ones defined for the company.

The next guide describes how to create a room allotment with a specific board type, configure pricing, and verify that the board type appears correctly in the booking ticket.

### Step 1: Access the Hotel Allotment Configuration

1. **Navigate to** `Hotel → Hotels`\
   → The system displays a list of all available hotels.
2. **Select a hotel** from the list\
   → The detailed view for the selected hotel opens.
3. **Click on the “Allotment” tab**\
   → The allotment configuration page opens, showing all existing room allotments.

### Step 2: Create a New Room Allotment

1. **Click “Create”**\
   → A new row appears for inputting allotment details.
2. **Enter the required details**
   * Room type, capacity, date range, etc.
3. **For the “Board” field**, select a board type from the dropdown\
   → The board type (e.g., _All Inclusive_, _Summer board_) created earlier should be available in the list.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

4. **Click the Save icon**\
   → The new allotment is saved and the board type appears correctly in the allotment row.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

### Step 3: Configure Pricing and Create a Booking

1. **Create a price list** for the newly created room allotment\
   → Ensures the room can be booked and priced correctly.
2. **Click “New booking”**\
   → The booking menu opens, allowing selection of hotel, room, and guest details.
3. **Create a booking using the configured room**\
   → The booking status should update to **OK**, indicating successful creation.

### Step 4: Verify Ticket and Board Type Visibility

1. **Click “Print Ticket”** on the completed booking\
   → A file containing the booking ticket is generated and opened.
2. **Check the ticket**\
   → The selected board type should be clearly visible on the ticket.

<figure><img src="../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Expected Outcomes

| Step                     | Expected Result                        |
| ------------------------ | -------------------------------------- |
| Board type is selected   | Dropdown lists created board types     |
| Save allotment           | Row is saved and board is shown        |
| Room added to price list | Room is available for booking          |
| Create booking           | Booking status becomes **OK**          |
| Print ticket             | Ticket includes the correct board type |
