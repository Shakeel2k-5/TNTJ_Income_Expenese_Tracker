# Product Requirements Document (PRD)

## Simple Mosque Monthly Income & Expense Report Generator (Web App)

**Version:** 2.0\
**Date:** 2026-02-19\
**Usage Type:** Internal, Once Per Month\
**Target Users:** Non-Technical Mosque Staff

------------------------------------------------------------------------

## 1. Product Overview

This web application is a **simple monthly financial entry tool**
designed for mosque administration.

The application will:

-   Allow manual entry of income records
-   Allow manual entry of expense records
-   Automatically calculate totals
-   Generate a **Monthly Report**
-   Export the report as:
    -   PDF file
    -   Excel (.xlsx) file

⚠️ Important Constraints:

-   No database required
-   No login system required
-   No long-term storage
-   Used only once per month
-   Data exists only during the session
-   After exporting, data can be cleared

------------------------------------------------------------------------

## 2. Target User

This application is designed for:

-   Mosque Treasurer
-   Mosque Secretary
-   Accountant (Non-technical)

The UI must be:

-   Very simple
-   Large buttons
-   Clear labels
-   Minimal steps
-   No technical jargon

------------------------------------------------------------------------

## 3. Functional Requirements

### 3.1 Income Entry Section

Each income record must include:

1.  Date
2.  Receipt Book Number
3.  Receipt Number
4.  Type of Income (Dropdown)
5.  Name
6.  Amount

#### Features:

-   "Add Income" button
-   Display income entries in a simple table
-   Edit/Delete option for each row
-   Automatic running total of income

------------------------------------------------------------------------

### 3.2 Expense Entry Section

Each expense record must include:

1.  Date
2.  Voucher Book Number
3.  Voucher Number
4.  Type of Expense (Dropdown)
5.  Expense Amount

#### Features:

-   "Add Expense" button
-   Display expense entries in a simple table
-   Edit/Delete option for each row
-   Automatic running total of expenses

------------------------------------------------------------------------

## 4. Monthly Summary Section

Automatically calculate:

-   Total Income
-   Total Expense
-   Net Balance (Income - Expense)

Display clearly in large bold format.

------------------------------------------------------------------------

## 5. Report Generation

### 5.1 PDF Report

PDF must contain:

-   Mosque Name (Editable Header)
-   Month & Year
-   Income Table
-   Expense Table
-   Total Income
-   Total Expense
-   Net Balance
-   Generated Date

Layout should be clean and printable (A4 size).

------------------------------------------------------------------------

### 5.2 Excel Report

Excel file should contain:

Sheet 1 -- Income\
Sheet 2 -- Expense\
Sheet 3 -- Summary

All totals must be calculated and visible.

------------------------------------------------------------------------

## 6. Non-Functional Requirements

### 6.1 Simplicity

-   One single page application
-   No multiple navigation steps
-   Clear section separation
-   Simple color theme

### 6.2 Performance

-   Should work offline (optional if hosted locally)
-   Must handle up to 500 entries smoothly

### 6.3 Usability

-   Large fonts
-   Clear input labels
-   Confirmation before clearing data
-   "Generate Report" button clearly visible

------------------------------------------------------------------------

## 7. Technical Architecture (Simple Version)

### Frontend Only Approach (Recommended)

-   React / Plain HTML + JavaScript
-   Tailwind CSS (optional)
-   All data stored in browser memory (state)
-   No backend required

### File Generation

-   PDF: jsPDF or similar
-   Excel: SheetJS (xlsx library)

------------------------------------------------------------------------

## 8. Application Flow

1.  User opens web app
2.  Enters mosque name and month
3.  Adds income entries
4.  Adds expense entries
5.  Reviews summary totals
6.  Clicks "Generate PDF" or "Generate Excel"
7.  Files downloaded
8.  User clicks "Clear Data" after saving

------------------------------------------------------------------------

## 9. Out of Scope

-   No database
-   No authentication
-   No cloud storage
-   No multi-user system
-   No audit tracking

------------------------------------------------------------------------

## 10. Success Criteria

-   User can complete monthly report in less than 20 minutes
-   PDF and Excel files generate without errors
-   Non-technical user can operate without guidance

------------------------------------------------------------------------

# End of Document
