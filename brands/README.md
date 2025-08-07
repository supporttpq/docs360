# Brands

This documentation outlines the structure and management of brands within the system. Each brand has associated metadata used for display, contact handling, and booking identification.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Table Columns Explanation

1. **Name**
   * The brand name displayed publicly or internally.
   * Example: "Primo Tours"
2. **Company**
   * The parent company name owning the brand.
   * Example: "Primo Tours A/S"
3. **Address**
   * The physical address of the brand's office.
   * Example: "Rindumgaards Alle 3"
4. **Place**
   * Includes postal code and city location.
   * Example: "DK-6950 Ringkøbing"
5. **Booking IDs From / To**
   * Range of booking IDs assigned to this brand.
   * Used to associate bookings with the correct brand.
   * Example: From 600000 to 799999
6. **Use Contact Info in List**
   * A checkbox indicating if the brand's contact info should be shown in lists.
   * Possible Values: Checked (true), Unchecked (false)
7. **Is Hidden**
   * Indicates if the brand is hidden from the user interface.
   * Represented by:
     * Green check (✓) = Hidden (true)
     * Red cross (✘) = Not Hidden (false)
8. **Payment Rules**
   * A link to view or edit the payment rules for the brand.
   * Labeled as "Payment rules"
9. **Delete Icon**
   * Trash bin icon allowing deletion of the brand.

#### Notes

* Ensure booking ID ranges do not overlap between brands.
* Only set "Use Contact Info in List" if the brand's contact details are required in list views.
* Regularly review hidden status to ensure correct visibility in the UI.
