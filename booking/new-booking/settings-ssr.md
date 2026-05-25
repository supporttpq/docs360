---
tags:
  - v15.2
---

# Settings (SSR)

## SSR Configuration – Booking Settings Tab

### Overview

The **SSR Configuration** feature allows users to manage **Special Service Requests (SSR)** directly from the **Settings** tab of a booking.

The feature provides a centralized overview of all passengers in the booking together with their assigned SSR codes. SSRs can originate from:

* **Extras** added to the booking
* **Manual SSR assignments** added directly in the Settings tab

The functionality ensures that airline-related passenger requirements are visible, manageable, and synchronized throughout the booking flow and reporting processes.

***

## Purpose

The SSR Configuration page is designed to:

* Display all SSRs assigned to passengers
* Distinguish between SSRs added automatically via Extras and manually added SSRs
* Allow users to add additional SSRs per passenger
* Prevent duplicate SSR assignments
* Ensure only valid SSRs configured for ticket usage are available
* Improve visibility during booking handling, ticketing, and reporting

***

## Location in System

**Booking → Settings Tab → Special Service Request (SSR)**

<figure><img src="../../.gitbook/assets/SSR settings (1).png" alt=""><figcaption></figcaption></figure>

The page contains a dedicated section with the headline:

> **Special Service Request (SSR)**

***

## SSR Table Structure

The SSR table displays all passengers included in the booking.

| Column        | Description                          |
| ------------- | ------------------------------------ |
| **PAX**       | Passenger number in the booking      |
| **Passenger** | Passenger full name                  |
| **SSR**       | Assigned SSR codes for the passenger |

***

## SSR Display Rules

### SSR Format

All SSR codes are displayed using the following format:

```
<CODE> - <NAME>
```

#### Example

```
DBML - Diabetic Meal
AVIH - Animal in Hold
WCHR - Wheelchair Required
```

***

## SSR Sources

### 1. SSR Added via Extras

SSR codes automatically added through Extras are displayed in the SSR list.

<figure><img src="../../.gitbook/assets/ssl extras.png" alt=""><figcaption></figcaption></figure>

#### Rules

* Cannot be deleted manually
* No garbage bin is shown
* Always visible for the passenger

#### Example

A passenger purchases a **Diabetic Meal Extra**.

The system automatically adds:

```
DBML - Diabetic Meal
```

The SSR appears in the table without a delete icon.

***

### 2. Manually Added SSR

Users may manually add SSRs directly from the Settings tab.

<figure><img src="../../.gitbook/assets/ssr 2.png" alt=""><figcaption></figcaption></figure>

#### Rules

* Can be deleted
* Garbage bin icon is displayed
* Multiple SSRs can be added per passenger

***

## Add SSR Functionality

Each passenger row contains an:

> **Add SSR**

button or selection field.

Users can assign additional SSRs to the passenger.

***

## Dropdown Behavior

The SSR dropdown follows these rules:

| Rule                 | Description                                     |
| -------------------- | ----------------------------------------------- |
| Searchable           | Users can search SSR codes                      |
| Alphabetical Sorting | SSR list sorted alphabetically                  |
| Show on Ticket Only  | Only SSRs marked _Show on Ticket_ are displayed |
| No Duplicates        | Already assigned SSRs are hidden                |
| SSR Format           | Displayed as `<CODE> - <NAME>`                  |

***

## Searchable Dropdown

The dropdown allows users to quickly locate SSRs.

#### Example Searches

| Search Input | Result                       |
| ------------ | ---------------------------- |
| `DB`         | `DBML - Diabetic Meal`       |
| `wheel`      | `WCHR - Wheelchair Required` |
| `meal`       | Multiple meal-related SSRs   |

***

## SSR Selection Logic

The system excludes SSRs that are already assigned to the passenger.

This includes:

* SSRs added manually
* SSRs added via Extras

***

## Delete SSR

Manually added SSRs can be removed using the garbage bin icon.

### Rules

| SSR Type         | Can Delete |
| ---------------- | ---------- |
| Added via Extras | No         |
| Added manually   | Yes        |

***

## Tooltips

### SSR Headline Tooltip

Tooltip shown on:

> **Special Service Request (SSR)**

#### Tooltip Text

```
List the SSR assigned to a passenger. SSR codes without a possibility to delete them are added via an Extras
```

***

### Add SSR Tooltip

Tooltip shown on:

> **Add SSR**

#### Tooltip Text

```
Add an SSR code to the passenger. More than one SSR code can be selected.
```

***

### Garbage Bin Tooltip

Tooltip shown on delete icon.

#### Tooltip Text

```
Delete the SSR code for this passenger.
```

***

## Configuration Requirements

### SSR Master Configuration

SSR codes must exist in the SSR master configuration.

Each SSR should contain:

| Field          | Description                     |
| -------------- | ------------------------------- |
| Code           | Airline SSR code                |
| Name           | SSR description                 |
| Show on Ticket | Determines if SSR is selectable |
| Active         | Determines if SSR can be used   |

***

## Booking Flow Behavior

### During Booking Management

Users can:

* Review SSR assignments
* Add additional SSRs
* Remove manually added SSRs
* Identify SSRs added through Extras

***

### Example – Manual SSR Addition

#### Scenario

Passenger requires wheelchair assistance.

#### Steps

1. Open booking
2. Navigate to **Settings**
3. Locate passenger row
4. Click **Add SSR**
5.  Search for:

    ```
    WCHR
    ```
6.  Select:

    ```
    WCHR - Wheelchair Required
    ```

#### Result

The SSR is added to the passenger and can later be removed if necessary.

***

### Example – SSR Added via Extra

#### Scenario

Passenger purchases a Vegetarian Meal Extra.

#### Result

The system automatically adds:

```
VGML - Vegetarian Meal
```

The SSR:

* Appears in the SSR list
* Cannot be deleted manually
* Does not display a garbage bin

***

## Web Booking Manifestation

When SSR-linked Extras are selected during web booking:

* The corresponding SSR is automatically assigned
* SSR appears in the booking Settings tab
* SSR becomes visible for operations and ticketing

#### Example

Customer purchases:

```
Pet Transportation Extra
```

Automatically assigned SSR:

```
AVIH - Animal in Hold
```

***

## Reporting Manifestation

SSR information can be included in operational and airline reporting.

Typical usages:

* Passenger manifests
* Airline exports
* Ticketing files
* Operational handling reports

#### Example Report Output

| Passenger  | SSR                        |
| ---------- | -------------------------- |
| John Smith | DBML - Diabetic Meal       |
| Anna Brown | WCHR - Wheelchair Required |

***

## User Interface Guidelines

The SSR section should follow the styling of existing modern booking pages.

Recommended UI behavior:

* Clear table layout
* Consistent spacing
* Searchable dropdown
* Readable SSR badges/tags
* Tooltip support
* Disabled delete option for Extra-generated SSRs

***

## Example – Complete Passenger Scenario

| PAX | Passenger  | SSRs                                  |
| --- | ---------- | ------------------------------------- |
| 1   | John Smith | DBML - Diabetic Meal _(via Extra)_    |
| 1   | John Smith | WCHR - Wheelchair Required _(manual)_ |
| 2   | Anna Brown | AVIH - Animal in Hold _(manual)_      |

#### Behavior

* `DBML` cannot be deleted
* `WCHR` can be deleted
* `AVIH` can be deleted
