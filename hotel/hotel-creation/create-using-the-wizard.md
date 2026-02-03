# Create using wizard

### Overview

The **Add Hotel Wizard** is designed to simplify the process of creating a new hotel in the system. Instead of navigating across multiple tabs and saving several times, the wizard allows you to enter all required information on a single page.

Once saved, the hotel is created automatically. The system then redirects you to the hotel’s edit page. You can add optional details there (contracts, supplements, etc.).

{% hint style="info" %}
This feature is typically available for administrator users.
{% endhint %}

### Purpose

This functionality streamlines the hotel creation process, reduces time spent on setup, and ensures that all minimum required data is entered before the hotel is saved.

### Accessing the Wizard

1. Navigate to the **Hotel List** page.
2. Click the **Create using wizard** button.
3. The system opens the **Add Hotel Wizard** form.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Required Fields

* **Code**\* – A unique identifier for the hotel (used internally in the system).
* **Name**\* – The official name of the hotel.
* **Resort**\* – Select the resort to which the hotel belongs.
* **Stars**\* – Select the hotel’s star rating (1–5, or applicable classification).
* **Contract Type**\* – Define the type of contract used with this hotel (e.g., direct contract, allotment, bed bank).
* **Rooms**\* – Add at least one room type to complete the setup. Click **Edit** to add and configure room types.
* **Standard Room**\* – Select the room type to be used as the standard/default option for this hotel.

### Optional Fields

* **Resort Name** – Optional free-text label for the resort.

<figure><img src="../../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure>

### Brands Assignment

At the bottom of the wizard, you can assign the hotel to specific **Tourpaq brands** (e.g., Tourpaq DK, Tourpaq SE, Tourpaq Live). By default, all are set to _Not assigned_. Assignments should be made if the hotel is to be visible and bookable under a specific brand.

### Saving

* Once all required fields are filled, click **Save**.
* The system creates the new hotel and redirects you automatically to the **Edit Hotel** page, where you can enrich the setup with further optional data (supplier, board basis, contracts, etc.).

### Example Use Case

A new hotel _Sunset Resort_ in _Agia Marina_ can be created by:

1. Entering a code (e.g., **SUNSET01**)
2. Assigning it to the resort _Agia Marina_
3. Selecting **4 stars** and contract type **Allotment**
4. Adding one room type (_Double Room_) and setting it as the standard room
5. Assigning it to the **Tourpaq Live** brand

With these steps, the hotel is created in just one page and ready for further configuration.

***

### FAQ

**Q: Who can create a hotel using the wizard?**\
**A:** Typically administrators. If you can’t see the button, check your role and permissions.

**Q: What’s the difference between “Resort” and “Resort Name”?**\
**A:** **Resort** links the hotel to a resort in the system. **Resort Name** is optional free text.

**Q: Why can’t I save the wizard?**\
**A:** One of the required fields is missing. You also need at least one room type and a selected **Standard Room**.

**Q: My hotel code already exists. What should I do?**\
**A:** Codes must be unique. Use a different code that matches your internal naming standard.

**Q: Do I need to add rooms now, or can I do it later?**\
**A:** You must add at least one room type in the wizard. You can add more room types later on the hotel’s edit page.

**Q: What is “Standard Room”, and why is it required?**\
**A:** It’s the default room type used by the system. It’s required to complete the hotel setup.

**Q: What does “Contract Type” control?**\
**A:** It defines the contract model for the hotel (for example allotment vs bed bank). It also helps guide selection and workflow in related hotel features.

**Q: I created the hotel, but I can’t find it in bookings or WebBooking. Why?**\
**A:** Check brand assignment. If the hotel is **Not assigned** for the relevant brand, it won’t be visible or bookable for that brand.

**Q: Where do I add supplier, board basis, contracts, and other details?**\
**A:** After saving. The wizard redirects you to the hotel’s edit page where you can complete the configuration.
