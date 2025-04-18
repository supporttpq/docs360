# Vouchers

Voucher documents are automatically generated by a windows service that runs several times a day. Vouchers can be generated for:

* hotels
* extras categories
* transfer prices
* discount/supplements

Important aspects in the vouchers generation:

* vouchers are generated with "x" days before departure; "x" value is set from "System setup" - "Vouchers generation" field
* booking status should be "ok"
* booking should be fully paid
* the voucher (for hotel, extra category, transfer price, discount) should have not been generated yet
* for extras categories: if any extra from the category for which vouchers must be generated has required attributes, the values for the attributes must be filled in
* in system setup there is set a value
* vouchers are not generated for bookings with departure date in the past
* the hotel, extra category, transfer price, discount for which vouchers should be generated should have set "issue voucher" and a supplier selected
