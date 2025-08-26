# Creditor

### **Overview / Purpose**

The **Autobilling feature** in Tourpaq automates the process of generating invoices for suppliers, hotels, extras, and other services. To use this functionality, the system requires that at least one **creditor** is created and linked to the relevant supplier or service.

### **How It Works**

* **Creditors** act as financial entities representing the suppliers or partners that Tourpaq invoices on behalf of.
* When Autobilling is triggered, the system uses the **creditor details** to generate invoices automatically.
* Without a creditor, Autobilling cannot process or issue invoices.

### **Notes**

* To create a creditor, go to **Users → Creditors** and add the required details.
* Always double-check creditor details (company name, financial data) to ensure invoices are generated correctly.
* Each supplier that requires automated invoicing should be linked to its own creditor.

<figure><img src=".gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

#### **General Information Section**

1. **Name (**_**Required**_**)** – Input field for entering the creditor's name.
2. **Email (**_**Required**_**)** – Input field for the creditor’s email address.
3. **Swift Code** – Field for entering the SWIFT code used for international bank transactions.
4. **IBAN Number** – Field for entering the IBAN (International Bank Account Number).
5. **Account Credit (**_**Required**_**)** – Field for specifying the credit limit or balance.
6. **Intern Comment** – Field for internal notes or comments about the creditor.

#### **Address & Location Details**

7. **Postcode & Place** – Fields for entering the postal code and corresponding place.
8. **Country** – Field for specifying the country.
9. **Address** – Field for entering the creditor’s address.

#### **Financial & Payment Settings**

10. **Credit No** – Unique identifier for the creditor.
11. **Currency** – Dropdown to select the currency.
12. **Approval Interval (**_**Required**_**)** – Field for entering the approval period.
13. **Payment Days (**_**Required**_**)** – Field for specifying the number of days for payments.
14. **Payment Terms** – Additional field for specifying custom payment terms.

#### **Additional Options**&#x20;

15. **Automatic** – Option to enable automatic payments or processes.
16. **Invoices as PDF** – Option to generate invoices in PDF format.
17. **Include Specification in PDF** – Option to include detailed specifications in invoices.
18. **Remove QR Code** – Option to remove QR codes from invoices.

#### **Other Fields**

19. **Assigned Agency (Default: "All brands")** – Dropdown for selecting an assigned agency.
20. **Logo** – Placeholder for uploading or displaying a logo.
