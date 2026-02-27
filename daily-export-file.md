---
description: >-
  Daily financial export emailed as CSV/XLSX. Configure recipients and enable
  Daily Export to share booking and passenger data for reconciliation, ERP, and
  BI.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Daily Export file

### Overview

The **Daily Export file** is an automated daily **financial export** of booking and passenger data from Tourpaq Office.

The export is enabled in system settings and sent to one or more configured email recipients.

This export supports operational reporting, financial reconciliation, and data integration with external tools such as ERP systems or BI dashboards.

***

### Purpose

The Daily Export File provides:

* A structured, automated snapshot of all bookings that meet specified filter criteria
* Comprehensive financial and customer data needed for daily operational oversight
* Support for tasks such as accounting, sales monitoring, commission tracking, and CRM updates

***

### Preconditions

Before using this feature, ensure the following:

1. The **Daily Export** functionality is **enabled** in the database under:\
   `SystemRegister > Daily Export setting`\
   (This may require assistance from a system administrator or developer.)
2. One or more **recipient email addresses** must be configured under:\
   `Setup Menu > System Setup > Financial Export email address(es)`
3. You have the necessary **Administrator** or **Financial** user permissions to manage exports and access booking data.

***

### Instructions

Once enabled and configured, the Daily Export File will run **automatically** based on system-defined triggers (typically scheduled overnight). No manual steps are required after setup.

However, to **verify or adjust the setup**, follow these steps:

#### Step-by-step configuration

1. **Enable the Export**
   * Confirm that the `Daily Export` setting is active in `SystemRegister`.
2. **Set Recipient Emails**
   * Go to: `Setup Menu > System Setup`
   * Locate: **Financial Export Email Address(es)**
   * Enter one or more valid email addresses (comma-separated if multiple).
   * Save the configuration.
3. **Review Export Results**
   * Check the inbox of the configured email addresses after the scheduled export.
   * The export file is typically `.CSV` or `.XLSX`, depending on your setup.

<figure><img src=".gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Daily Export email recipient configuration"><figcaption><p>Configure recipient emails for the Daily Export file in System Setup (Financial Export email addresses).</p></figcaption></figure>

### Exported data fields

The Daily Export contains one row per **passenger** and includes comprehensive booking, customer, and cost-related data. Below is a list of all fields:

#### Booking information

* Booking number
* Booking date
* Booking status
* Booking total price
* Seller
* Agent
* Transport code
* Travel length
* Departure date
* Arrival home date

#### Passenger information

* Adults number
* Children number
* Infants number
* Seats
* First name
* Last name
* Gender
* Age
* Passenger status
* Passenger total price
* Extra bed discount
* Cancellation fee

#### Accommodation details

* Hotel code
* Resort code
* Room code
* Rooms number
* Room price
* Hotel cost

#### Customer contact information

* Customer email
* Customer postcode
* Customer fax
* Customer phone number
* Customer CPR
* Customer city
* Customer address

#### Additional services and products

* Has cancellation insurance
* Cancellation insurance price
* Has transfer
* Transfer price
* Travel insurance type
* Travel insurance price
* VIP product
* VIP product price
* Party package product
* Party package product price
* Pension product
* Pension product price
* Catering product
* Catering product price
* Car product
* Car product price
* Other products

#### Cost breakdown

* Transport cost
* Transfer cost
* VIP cost
* Party package cost
* Pension cost
* Catering cost
* Car cost
* Other products cost
* Insurance cost
* Discounts/supplements
* Discounts/supplements cost
