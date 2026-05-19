# MTS Globe hotel reporting

## Overview

The **MTS Globe Hotel Reporting** interface defines the structure and delivery method for booking information exchanged between distributors and handling offices using `.csv` files.\
The reporting process supports:

* New bookings
* Modified bookings
* Cancelled bookings
* Hotel accommodations
* Transfers and additional services

The import structure is designed to standardize booking communication between distributors and MTS Globe operational systems.

***

## Purpose

The purpose of this documentation is to help team members understand:

* How hotel reporting files are structured
* Which fields are mandatory
* How bookings and cancellations are processed
* How accommodation and transfer services are mapped
* The expected formatting rules for successful imports

***

## File Naming Convention

Each file must follow a strict naming structure based on the booking action type.

| Booking Type       | Example File Name         |
| ------------------ | ------------------------- |
| New Bookings       | `XXXX_new_20170907.csv`   |
| Cancelled Bookings | `XXXX_canx_20170907.csv`  |
| Modified Bookings  | `XXXX_amend_20170907.csv` |

#### Notes

* `XXXX` = Distributor code (the "Brand Code" from the brand page is used as the distributor. This is the same code used for flight transfer. Brand Code; this is the name of the Brand.)
* Date format = `YYYYMMDD`

***

## File Format Requirements

The import file must use the following format:

| Setting        | Requirement       |
| -------------- | ----------------- |
| File Type      | `.csv`            |
| Separator      | Semicolon `;`     |
| Text Delimiter | Double Quotes `"` |

#### Example

```csv
"Office";"Distributor";"Reference";"Pax Name"
"PMI";"XXXX";"INH19BZ4VQC";"KOLEN, ROSA JOHANNA"
```

***

## Delivery Methods

Booking files can be delivered in two ways:

### 1. FTP Delivery

* One file for all destinations
* Or separate files per destination office
* Automatically imported

### 2. Email Delivery

* `.csv` file attached to email
* Sent to destination-specific email addresses
* Imported manually by destination teams

{% hint style="info" %}
Email delivery is sometimes preferred when:

* Data quality cannot be guaranteed
* Manual verification is required
{% endhint %}

***

## New & Modified Booking Structure

New and modified bookings use the same file format.

### Modification Logic

When a booking is modified:

1. Existing booking items are cancelled
2. New booking items are recreated from the file data

***

## Booking Field Definitions

### General Booking Information

| Field       | Required | Description              | Example               |
| ----------- | -------- | ------------------------ | --------------------- |
| Office      | Yes      | Handling office code     | `PMI`                 |
| Distributor | Yes      | Distributor code         | `XXXX`                |
| Brand       | No       | Brand code               | `MTS`                 |
| Reference   | Yes      | Unique booking reference | `INH19BZ4VQC`         |
| Pax Name    | Yes      | Lead passenger           | `KOLEN, ROSA JOHANNA` |

***

### Passenger Information

| Field             | Required | Description                            |
| ----------------- | -------- | -------------------------------------- |
| ADT               | Yes      | Number of adults                       |
| Additional Adults | No       | Additional adult names separated by \` |
| Adult\_Ages       | No       | Adult ages separated by `,`            |
| CHD               | No       | Number of children                     |
| CHD Ages          | No       | Child ages separated by `,`            |
| Child Names       | No       | Child names separated by \`            |
| INF               | No       | Number of infants                      |
| Infant Names      | No       | Infant names separated by \`           |

#### Example

```
"KOLEN, ROSITA JOHANNES | KOLEN, JUAN CARLES"
```

***

### Date Fields

| Field      | Required | Description                    |
| ---------- | -------- | ------------------------------ |
| Book Date  | Yes      | Original booking creation date |
| Start Date | Yes      | Check-in/service start         |
| End Date   | Yes      | Check-out/service end          |

***

## Product Information

| Field  | Required | Description                 |
| ------ | -------- | --------------------------- |
| P.Type | Yes      | Product type                |
| P.Code | Yes      | Product code/name           |
| Unit   | Yes      | Room or transfer unit       |
| Base   | Yes      | Board or transfer direction |

***

## Product Type Codes

| Code | Meaning                    |
| ---- | -------------------------- |
| AC   | Accommodation              |
| TR   | Transfer Airport to Resort |
| TRS  | Seaport to Resort          |
| XA   | Excursions & Activities    |
| CT   | Circuit and Tours          |
| CR   | Car Rental                 |
| IC   | Inter-Company Transfer     |
| AR   | Accommodation + Car        |
| FD   | Hotel Package              |
| MP   | Other Package              |
| OP   | Other Services             |
| PX   | Package and Excursion      |
| VS   | Visa Services              |
| GS   | Airport Services           |
| MI   | MICE Services              |
| MM   | Museums & Monuments        |
