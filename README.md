# SQL Financial Database Analysis

This project contains advanced SQL queries and stored procedures developed for the final SQL assignment at CodersLab. It focuses on analyzing anonymized banking data, including loans, clients, account balances, and expiring credit cards.

## Project Overview

The dataset includes:
- ~5,300 clients
- ~700 granted loans
- ~900 issued credit cards

The project explores:
- Loan trends and repayment behavior
- Client demographic analysis
- Account-based loan rankings
- Regional loan distribution
- Credit card expiration tracking

## Key Analyses

1. **Granted Loan History**
   - Aggregates loans by year, quarter, and month using `ROLLUP`.

2. **Loan Status Breakdown**
   - Separates repaid (statuses A & C) vs. unpaid (B & D) loans.

3. **Account Loan Rankings**
   - Uses CTE + `ROW_NUMBER()` to rank accounts by loan count and total loan amount.

4. **Client Gender & Loan Repayment**
   - Evaluates number of loans repaid by men vs. women.

5. **Client Age Analysis**
   - Calculates average age by gender using a temporary table.

6. **Regional Loan Patterns**
   - Compares districts by total loans, number of clients, and repayment share using `SUM OVER()`.

7. **Client Filtering**
   - Attempts to find high-balance, young, multi-loan clients (result: none match criteria).

8. **Credit Card Expiration**
   - Tracks cards expiring 3 years after issue, simulated with the date `'2001-01-01'`.

9. **Stored Procedure: `expiring_cards_VELCOVSKY()`**
   - Automatically creates a table with expiring cards, client info, and region.

## SQL Techniques Used

- `ROLLUP`, `HAVING`, `CTE`, `WINDOW FUNCTIONS`, `ROW_NUMBER()`
- Stored procedures with conditional table logic
- Robust joins and aggregation

## Files

- `financial-database.sql` – Complete SQL script
- `SQL Final project for CodersLab.pdf` – Project report
