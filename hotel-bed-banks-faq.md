# Hotel Bed Banks - FAQ

*   ### 1. Test Bookings

    **Q:** Can we make a test booking live in our system and then cancel it without payment to Hotelbeds?\
    **A:** No. Hotelbeds does not provide a working test environment, so live test bookings will involve actual contracts. There is currently no workaround for test bookings without payment.

    ### 2. Contract Expiration Notifications

    **Q:** How will we know if a contract expires?\
    **A:** There is no current notification for hotel contract expiration. This has been noted as an improvement idea for future development.

    **Q:** Will we get a notification if a contract changes?\
    **A:** No automatic notification exists. Hotels are not tied to a specific contract, so after each contract change, you must manually check the price list.

    ### 3. Importing New Periods and Rates

    **Q:** When a hotel contract expires, can we import a new period and new rates on the same hotel, or must a new hotel be created?\
    **A:** You can import multiple contracts for the same hotel, but not for the same room. You can choose a different contract per room, allowing multiple contract periods per hotel.

    ### 4. Children and Extra Bed Rates

    **Q:** How can we see information regarding children, ages, and rates? Are these imported into Tourpaq?\
    **A:** Only limited data is imported from Hotelbeds:

    * Extra bed discounts are imported into Tourpaq.
    * Children’s prices are calculated as a discount from the base price.
    * Discount details for children are available in the contract overview screen of the Hotelbeds module.

    ### 5. Non-Refundable Rates

    **Q:** How can we see if the hotel or rates are non-refundable?\
    **A:** This is currently unclear. Cancellation fees from Hotelbeds can be confusing. A ticket has been raised with Hotelbeds, but no direct answer is available yet.

    ### 6. Room Type Names and Filters

    **Q:** When we disable filters under room types and create or choose our own names, why do the room costs still show the original contract room type? Can this be changed?\
    **A:** This is a known behavior. Even if you rename rooms, the system currently retains the contract room type in the Room Cost tab. A fix is planned for a future release.

    ### 7. Room Cost Periods

    **Q:** Sometimes room cost periods are imported as date ranges (e.g., 01-02-2020 to 08-02-2020). Searching for a specific day (e.g., 04-02-2020) may show no cost. Why?\
    **A:** Currently, the system does not support per-day rate searches within a period. You need to review the entire period to verify costs. This limitation may be addressed in a future improvement if approved.
