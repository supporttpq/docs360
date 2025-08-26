# Validate Phone Number

### **Overview / Purpose**

Tourpaq WebBooking allows brands to collect customer phone numbers in a **split format** to ensure correct international dialing. This improves data accuracy and ensures phone numbers are properly formatted for booking confirmations and communications.

***

### **How It Works**

* The phone number field is split into **two parts**:
  1. **Country Code** – pre-filled based on the selected country but editable via a dropdown list.
  2. **Phone Number** – accepts only numeric characters and must meet a minimum of 8 digits.
* The full phone number (including country code) is saved with the booking.
* This feature is enabled via the checkbox in **Brand → Web Booking Settings**.

***

### **Key Features / Functions**

#### **Country Code Field**

* Autofilled based on the selected country.
* Editable to allow a different country code from the dropdown list.
* Uses country codes defined by the system (configured by Super Administrators).

#### **Phone Number Field**

* Accepts only numeric characters.
* Minimum length: 8 digits.
* Validates input to prevent incorrect entries.

#### **Full Number Saving**

* If the **country code differs from the selected country**, the system saves the **complete number,** including the prefix.
* If the **country code matches the country**, the phone number is saved **without a prefix** and displayed correctly on the booking.

<figure><img src="../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

### **Examples / Scenarios**

1. **Matching Country Code**
   * Country: Denmark (+45)
   * Phone: 12345678
   * Booking saved as: 12345678
2. **Different Country Code**
   * Country: Denmark (+45)
   * Country Code Edited: +49 (Germany)
   * Phone: 12345678
   * Booking saved as: +4912345678
3. **Validation**
   * Entering letters or fewer than 8 digits triggers a validation error.

***

### **Notes / Best Practices**

* Ensure the **checkbox in Brand → Web Booking Settings** is enabled to activate this feature.
* Regularly update **country codes** in the system to reflect valid international dialing codes.
* Test bookings with both matching and differing country codes to verify correct saving and display.
