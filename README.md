---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Dashboard

The dashboard is the application start page. The main reason for this page is to receive information about the booking system quickly.

The Dashboard includes the following areas:

* Unpaid bookings
* Upsale
* Overbookings Outbound
* Overbookings Inbound
* Overbookings Hotel
* Overbookings Rooms
* Seats vs Beds
* Transport Warnings
* Warnings
* Error Bookings
* Error discount
* Waitlist
* GDS Queue
* GDS Ready For Submit
* Not Generated Vouchers
* Hotel Special Offers
* Extra Special Offers
* PrList Unlock
* Unbooked Guar Rooms
* Hotel Sold Out
* HCW
* Q Manag
* Stop Sales
* Sold Out PLTAs
* Refund Money
* Campaign Alarm
* Wrong PltaID Pass
* Extras with Allotments

### **Unpaid bookings**

This area represents a table with bookings that are selected by the following criteria:

* The booking must belong to the current selected agency (in case no agency is selected it will be taken the default agency)
* The customer didn’t pay the amount before the due date minus PDO (payment dashboard overdue. The number of days and this value are set under the System Setup menu by the user.)

Note: If the Due date is 17-05-2010, PDO is 4 and the booking is not paid before 13-05-2010 the booking will be shown in the table.

In case the departure date of the booking is within 10 days and is unpayd the booking will appear in the table when the criteria due date minus one day is met.

Table 1: Unpaid booking column description

| Column Name      | Value Type                        | Description                                                                                        |
| ---------------- | --------------------------------- | -------------------------------------------------------------------------------------------------- |
| Booking no       | number                            | It’s the unique number identifier of a booking. It’s a hyper link that points to the Booking Page. |
| Due date         | date formated like:day-month-year | Billing due date                                                                                   |
| Departure Date   | date formated like:day-month-year | Date of departure                                                                                  |
| Customer         | text                              | Full name name of the customer first name and last name.                                           |
| Booking total    | number                            | Booking price.                                                                                     |
| Paid amount      | number                            | Amount payed.                                                                                      |
| Balance          | number                            | Outstanding amount of payment                                                                      |
| Overdue          | text                              | Payment deadline                                                                                   |
| Due amount       | number                            | Ammount to be paide until the current due date.                                                    |
| Payment comments | text                              | Comments added by user                                                                             |
| Admin comments   | text                              | Comments added by Super administrator                                                              |

### **Upsale**

This area shows bookings that haven't chosen all available products(including hotel room and transport seating) and sellers can contact them and ask if they would like any more products.

### **Overbooking outbound**

A booking is overbooked, when the transport allotment that the booking is assigned to, has more passengers than the seats allowed.

| Booking no    | Number | It’s the unique number identifier of a booking. It’s a hyper link that points to the booking page |
| ------------- | ------ | ------------------------------------------------------------------------------------------------- |
| Transport     | text   | Code of transport                                                                                 |
| Resort        | text   | Code of resort                                                                                    |
| Customer      | text   | Full name of the customer                                                                         |
| Passengers no | number | Total number of the passengers of current booking.                                                |
| Seats missing | number | Seats that transport that are missing.                                                            |

### **Overbooking Inbound**

Same as **Overbooking Outbound**.

### **Overbooking Hotel**

A booking is overbooked, when the hotel that the booking is assigned to, has more passengers than the room available.

| Booking no    | Number | It’s the unique number identifier of a booking. It’s a hyper link that points to the booking page |
| ------------- | ------ | ------------------------------------------------------------------------------------------------- |
| Transport     | text   | Code of transport                                                                                 |
| Resort        | text   | Code of resort                                                                                    |
| Customer      | text   | Full name of the customer                                                                         |
| Passengers no | number | Total number of the passengers of current booking.                                                |
| Seats missing | number | Rooms that are missing in current hotel.                                                          |

### **Overbooking Room**

A room is overbooked when the total number of rooms of the same type booked is greater than the allotmed number of rooms of the same type.

**Destination seats vs Beds**

Shows the number of seats and number of beds for each departure grouped by destination. It indicates if there are too many flight seats (not incl. Dynamic P.) compared to numbers of beds.

Note!!! Beds means average number of pax per room sold so far.

### **Error bookings**

Displays all bookings that have errors detected by the system, even though their status is **OK**.

### **GDS queue**

In here are shown all GDS bookings that have the **TKQ** status.

### **GDS Ready For Submit**

This tab displays all bookings that have the **GDS pending** status and have met the requirements for beeing submited.

* Bookings that use Galileo can be submited upon creation.
* Bookings that use ACH can be submited only after the deposit has been paid.

### **Waitlist**

It is possible to book trips out of stock if WL check box is used in the pricelist. When the user tries to book a trip which is sold out, the system displays a warning that the user must accept. The finished booking will have the status of **WL**. There is a running service that checks for allotment to all **WL** bookings and tries to book them. When successful, the system will change the status of the **WL** booking to **WLOK** and list it on the dashboard. When the seller has spoken with the customer, he can manually enter the booking and either cancel the booking or confirm it, changing it's status to **OK** or **CXL**

### **Invoices**

This tab displays the statements that are sent for approval but not yet approved by the creditor. This is also where you can see if a settlement has come back from creditors in the event that the creditor does not agree with the content. It also shows returned and approved statements ready for payment.

### **Sold Out Hotels**

Displays all hotels that have exhausted their allotments and give the user the option to ignore the warning or request more rooms from the hotels.

### **Q. Manag.**

Allows the user to view Travelport Queue as well as changes made by Travelport to reservations.

### **Stop Sales**

This tab displays all hotels that have a stop sale, the period of the stop sale, and actions that can be taken regarding the stop sale:

* Details - will take the user to the stop sale panel
* Hide - hides the stop sale on dashboard

### **Sold Out PLTAs**

Displays the price lists that have depleted either the hotels or transport allotments, or both of them.

### **Refund money**

This tab displays bookings that have paid too much or those that have been modified and the total price became lower than the amount paid. The user must check these bookings, contact the guest and inform him/her of the changes and the fact that the amount paid is larger than the total, and decide with the guest the best course of action.

### **Campaign alarms**

In this tab an alert will appear that will notify the user that a set number of bookings per day have been made for a campaign in progress.

### **Dashboard count for tabs**

We have implemented a solution to calculate real live count for some tabs:

* Unpaid Bkg - GetUnpaidBookingsCount
* Upsale - GetExtrasNotSoldBookingsCount
* Transport Warnings - GetTransportReportingWarningsCount + GetRealTransportWarningsCount
* Warnings - GetWarningsCount
* Error Bkg - GetTurnoverErrOkCountForDashboard, GetTurnoverErrFeeCanceledPassCountForDashboard, GetTurnoverErrFeeLockOkPassCountForDashboard, GetTurnoverErrNoActivePassCountForDashboard,GetTurnoverErrCanceledBookFeeCountForDashboard, GetErrorBookingsByPassengerTotalCountForDashboard
* Error Disc - GetPassengersWithMultipleDiscountsWhileDoNotCombineCount
* Waitlist - GetWaitlistBookingCount
* GDQ Queue - GetGdsQueueCount
* GDS ReadyForSubmit - GetGdsReadyForSubmitCount
* Not Generated Vouchers - GetVouchersNotGeneratedBookingsCount
* Hotel Special Offer - GetHotelPriceExtraCount
* Extra Special Offer - GetNetPriceExtraCount
* PrListUnlock - GetPriceListUnlockCount
* Unbooked Guar Rooms - GetNumberOfUnbookedGuaranteedRoomsCount
* Hotel Sold Out - GetSoldOutHotelsCount
* StopSales - GetStopSalesCount
* SoldOut PLTAs - GetSoldOutPltaCount
* Refund Money - GetTransactionsToBeOverviewedCount
* Campaign alarm - GetTodayWarningMessagesCount
* Wrong PltaID Pass - GetWrongPltaPassengerCount
* Extras With Allotments - GetProductsWithAllotmentsCount
* NFIS in pricelist - GetNfisInPricelistCount

For others we kept old functionality to calculate count by Service:

* Overbkg - out
* Overbkg - in
* Overbkg - hotels
* Overbkg - rooms
* HCW
* Q Manag.
