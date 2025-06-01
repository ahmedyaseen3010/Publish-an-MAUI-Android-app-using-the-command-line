# Orchida E-Invoice Application Overview

**Fast, Reliable Tax Solutions**

---

## Index

- [Document Release History](#document-release-history)
- [1. Introduction](#introduction)
- [2. Purpose and Scope](#purpose-and-scope)
- [3. System Overview](#system-overview)
- [4. Key Features](#key-features)
- [5. Services](#services)
  - [5.1 API Integration](#api-integration)
  - [5.2 Manual User Input](#manual-user-input)
  - [5.3 Peppol Compliance](#peppol-compliance)
- [6. Dashboard Interface](#dashboard-interface)
  - [6.1 Login Page](#login-page)
  - [6.2 Invoices Management Page](#invoices-management-page)
    - [Invoice Table & Pagination](#invoice-table--pagination)
    - [Invoice Details Section](#invoice-details-section)
  - [6.3 Sales Invoices](#sales-invoices)
    - [Add Invoice](#add-invoice)
    - [Rejected and Archived Invoices](#rejected-and-archived-invoices)
  - [6.4 Purchase Invoices](#purchase-invoices)
  - [6.5 Single Invoice Display](#single-invoice-display)
  - [6.6 Main Definitions](#main-definitions)
  - [6.7 Help Screens](#help-screens)
- [7. Peppol Compliance](#peppol-compliance-1)
  - [7.1 Access Point](#access-point)
  - [7.2 Service Metadata Publisher (SMP)](#service-metadata-publisher-smp)
- [8. Setup Requirements](#setup-requirements)
- [9. Conclusion](#conclusion)

---

## Document Release History

| Version | Date       | Reason for Change          |
|---------|------------|----------------------------|
| 0.1     | 25-05-2025 | Initial document creation  |

---

## 1. Introduction

Orchida E-Invoice, developed by Orchida Soft, is a cloud-based platform designed to streamline electronic invoice processing. It ensures tax compliance and Peppol interoperability, offering a user-centric dashboard for managing invoices via manual entry or API integration. This document provides a comprehensive overview of the application's features, dashboard functionalities, and Peppol compliance.

---

## 2. Purpose and Scope

### Purpose
This document aims to provide users, administrators, and developers with a clear understanding of the Orchida E-Invoice system, its interface, and technical capabilities, with a focus on the Invoices Management Page and Peppol compliance.

### Scope
- Overview of the dashboard and core components.
- Detailed description of the Invoices Management Page.
- Key features, including login, invoice management, user rights, and help screens.
- Services: API integration, manual input, and Peppol compliance.
- Technical details of Access Point and SMP solutions.

---

## 3. System Overview

Orchida E-Invoice is a cloud-based platform for managing electronic invoices, supporting businesses in creating, viewing, and tracking sales and purchase invoices. It ensures compliance with tax regulations and Peppol standards, featuring role-based access control, detailed invoice management, and integrated support features.

---

## 4. Key Features

- **Login Page**: Secure OTP-based authentication via Email or WhatsApp.
- **Invoices Management Page**: Centralized hub for tracking and managing invoices.
- **Sales and Purchase Invoices**: Screens for viewing, adding, rejecting, and archiving invoices.
- **Single Invoice Display**: Detailed view with header, product, and summary grids.
- **User Rights**: Role-based access control (Admin/Standard).
- **Product and Client Management**: Centralized management of items and customer/supplier data.
- **Help Screens**: Support resources (news, tickets, FAQs, system info).
- **Peppol Compliance**: Supports Peppol e-invoicing via Access Point and SMP solutions.

---

## 5. Services

### 5.1 API Integration
- Automates invoice creation, submission, and retrieval.
- Integrates with ERP systems and third-party platforms.
- Ensures real-time synchronization of invoice data.

### 5.2 Manual User Input
- Intuitive forms for adding/editing invoices.
- Detailed grids for viewing invoice data.
- User-friendly interface for non-technical users.

### 5.3 Peppol Compliance
- **Access Point**: Facilitates secure invoice exchange within the Peppol network.
- **SMP Solution**: Manages service metadata for dynamic recipient discovery.

---

## 6. Dashboard Interface

The Orchida E-Invoice dashboard is the central hub for all invoicing activities, designed for ease of use and efficiency.

### 6.1 Login Page
Secure access via OTP-based authentication.

| Field Name       | Explanation                       |
|------------------|-----------------------------------|
| OTP Delivery     | Choose OTP via Email or WhatsApp. |
| OTP Input        | Enter OTP received.               |

**Buttons**:
- **Resend**: Resend OTP if not received.
- **Verify**: Submit OTP for login.

![Login Page 1](./media/image2.png)
![Login Page 2](./media/image3.png)

### 6.2 Invoices Management Page
A core component for tracking and managing invoices, supporting financial accuracy and tax compliance.

#### Invoice Table & Pagination
Displays a list of invoices with multiselect and pagination.

| No. | Field Name       | Explanation                                      |
|-----|------------------|--------------------------------------------------|
| 1   | Invoice Number   | Unique identifier.                              |
| 2   | Issue Date       | Date invoice was issued.                        |
| 3   | Currency         | Currency used (e.g., AED, USD, EUR, SAR).       |
| 4   | Customer Name    | Full name of the customer.                      |
| 5   | Company Name     | Legal/trade name of issuing company.            |
| 6   | Total Amount     | Overall invoice value, including charges.       |
| 7   | Tax Amount       | Calculated tax.                                 |
| 8   | Tax Status       | Submission status (e.g., Submitted, Pending).   |
| 9   | Client Status    | Client-side status (e.g., Accepted, Rejected).  |
| 10  | Customer TIN     | Customer Tax Identification Number.             |
| 11  | Customer Code    | Unique customer identifier in seller's system.  |
| 12  | Branch           | Company branch identifier.                      |

**Actions**:
- **Submit**: Sends invoice to tax portal or internal system.
- **Reject**: Prompts for rejection reason.
- **Archive**: Archives the invoice.

![Invoice Table](./media/image4.png)

#### Invoice Details Section
Expandable accordion displaying detailed invoice information.

**Lines (Itemized Products/Services)**:

| No. | Field Name       | Explanation                              |
|-----|------------------|------------------------------------------|
| 1   | Item Code        | Unique identifier for product/service.   |
| 2   | Item Name        | Description or title.                   |
| 3   | Item Description | Brief explanation of product/service.    |
| 4   | Qty              | Number of units.                        |
| 5   | Unit Price       | Cost per unit before discounts/taxes.   |
| 6   | Discount         | Price reduction (percentage or fixed).  |
| 7   | Net Total        | Total after discounts, before taxes.    |
| 8   | Tax              | Tax amount applied.                     |
| 9   | Total            | Total after tax and discount.           |
| 10  | Unit             | Measurement unit (e.g., kg, pcs, L).    |

**Allowances**:

| No. | Field Name | Explanation                             |
|-----|------------|-----------------------------------------|
| 1   | Type       | Charge or Discount.                    |
| 2   | Value      | Monetary amount of allowance/discount.  |
| 3   | Tax        | Tax amount related to allowance.       |
| 4   | Total      | Total value of allowances applied.     |

**Prepayments**:

| No. | Field Name   | Explanation                                    |
|-----|--------------|------------------------------------------------|
| 1   | Prepayments  | Total value of prepayment, including goods/services and taxes. |

![Invoice Details](./media/image5.png)

### 6.3 Sales Invoices
Screens for viewing, adding, rejecting, and archiving sales invoices.

#### Add Invoice
Form for creating new invoices.

| No. | Field Name         | Explanation                              |
|-----|--------------------|------------------------------------------|
| 1   | Invoice Number     | Unique identifier.                      |
| 2   | Customer (TIN/Name/Code) | Customer tax ID, name, or code.  |
| 3   | Items              | List of available items for selection.   |
| 4   | Qty                | Number of units.                        |
| 5   | Unit Price         | Cost per unit before discounts/taxes.   |
| 6   | Discount           | Price reduction for the item.           |
| 7   | Tax                | Tax amount applied.                     |
| 8   | Currency           | Transaction currency (e.g., USD, EUR).  |
| 9   | Branch             | Company branch identifier.              |

**Buttons**:
- **Add**: Creates a new invoice.

![Add Invoice](./media/image6.png)

#### Rejected and Archived Invoices
- **Rejected Invoices**: Lists rejected invoices with a "Reason" field.
  | No. | Field Name | Explanation              |
  |-----|------------|--------------------------|
  | 1   | Reason     | Reason for rejection.    |
- **Archived Invoices**: Stores finalized invoices, mirroring the View Invoices structure.

### 6.4 Purchase Invoices
Mirrors Sales Invoices structure with an additional "Reject Invoice" button prompting for a rejection reason.

### 6.5 Single Invoice Display
Detailed view of a single invoice with header, product, and summary grids.

| No. | Field Name     | Explanation                           |
|-----|----------------|-------------------------------|
| 1   | Invoice Number | Unique identifier.            |
| 2   | Issue Date     | Date of invoice creation.     |
| 3   | Due Date       | Payment due date.             |
| 4   | Total Amount   | Total after tax/discount.     |
| 5   | Buyer Name     | Name of the purchaser.        |
| 6   | Seller Name    | Name of the seller.           |
| 7   | Currency       | Transaction currency.         |
| 8   | Tax Amount     | Total tax applied.            |
| 9   | Buyer taxId    | Buyer's tax ID.               |

**Product Grid**:

| No. | Field Name     | Explanation                          |
|-----|----------------|------------------------------|
| 1   | Product Name   | Name of product/service.     |
| 2   | Description    | Detailed product info.       |
| 3   | Unit Price     | Price per unit before taxes. |
| 4   | Tax Category   | Type of tax applied.         |
| 5   | Net Amount     | Amount before taxes.         |

**Summary Grid**:

| No. | Field Name     | Explanation                          |
|-----|----------------|------------------------------|
| 1   | Subtotal       | Total before tax/fees.       |
| 2   | Tax            | Tax amount applied.          |
| 3   | Delivery Fee   | Shipping/delivery cost.      |
| 4   | Total          | Final amount including all.  |

![Single Invoice](./media/image7.png)

### 6.6 Main Definitions

#### User Rights
Role-based access control for Admin and Standard users with permissions (View/Modify/Deny) per page or feature.

| No. | Field Name   | Explanation                          |
|-----|--------------|------------------------------|
| 1   | User ID      | Unique identifier for each user. |
| 2   | Name         | Full name of the user.       |
| 3   | Role         | Admin or Standard.           |
| 4   | Permissions  | Access levels per page/feature. |

#### Items
Manages the product catalog for invoicing purposes.

| No. | Field Name         | Explanation                          |
|-----|--------------------|------------------------------|
| 1   | Item Code          | Unique identifier for the item. |
| 2   | Description        | Detailed information about the item. |
| 3   | Unit Price         | Price per unit, excluding taxes. |
| 4   | Tax Rate           | Percentage of tax applied.   |
| 5   | Unit of Measurement | Measurement unit (e.g., piece, kg, liter). |
| 6   | Name               | Name or title of the item.   |

#### Clients
Manages the customer and supplier database.

| No. | Field Name      | Explanation                          |
|-----|-----------------|------------------------------|
| 1   | Name            | Name of the buyer or seller. |
| 2   | TIN             | Tax Identification Number.   |
| 3   | Code            | Internal or external reference code. |
| 4   | Address         | Full address details (Street, City, Country, Building No., Postal Code). |
| 5   | Billing Address | Address for sending invoices. |
| 6   | Contact         | Phone number and/or email of the contact person. |

### 6.7 Help Screens
- **E-Invoice News**: System updates and announcements.
  ![News](./media/image8.png)
- **Tickets**: Submit support requests (Ticket ID, Title, Description, Contact Email, Phone, Status).
  ![Tickets](./media/image9.png)
- **FAQ**: Accordion-style list of common questions/answers.
  ![FAQ](./media/image10.png)
- **About**: System version and company information.

---

## 7. Peppol Compliance

Orchida E-Invoice supports Peppol e-invoicing through integrated Access Point and SMP solutions.

### 7.1 Access Point
- Secure transmission using AS4 protocol.
- Supports Peppol BIS Billing 3.0 and other document types.
- Validates invoices against Peppol specifications.

### 7.2 Service Metadata Publisher (SMP)
- Registers participant identifiers and document types.
- Integrates with Peppol Service Metadata Locator (SML).
- Supports Peppol’s four-corner model for secure invoicing.

---

## 8. Setup Requirements

To set up Orchida E-Invoice for Peppol compliance:
1. **Register with a Peppol Authority**: Obtain a participant identifier.
2. **Integrate SMP**: Configure SMP to register services and document types with Peppol SML.
3. **Provide Seller Data**:
   - Seller trading name
   - Seller name
   - Seller postal address
   - Tax registration number
   - Seller contact email address
   - Seller contact telephone number
   - Seller additional legal information
   - Seller VAT registration identifier
   - Seller country code

---

## 9. Conclusion

Orchida E-Invoice, developed by ORCHIDA SOFT BUSINESS SOLUTIONS, offers a robust platform for managing electronic invoices. With its intuitive dashboard, detailed Invoices Management Page, API integration, manual input, and Peppol compliance, it meets the needs of businesses seeking efficient and compliant invoicing solutions. For support, contact us at [insert contact details].

**Thanks for Reading.**
