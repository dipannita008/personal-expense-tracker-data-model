# Personal Expense Tracker Database Design

## Overview

This project presents a relational database design for a Personal Expense Tracker application. The database enables users to manage multiple financial accounts, record transactions, categorize expenses, analyze spending by merchant, and track monthly budgets.

## Business Requirements

The database is designed to support:

- Expense tracking across multiple accounts
- Spending categorization
- Merchant-wise spending analysis
- Monthly budget management
- Spending trend analysis
- Budget vs. actual spending comparison

## Conceptual Data Model

The conceptual model identifies the core business entities and their relationships at a high level.

<img width="1230" height="1071" alt="Personal_Expense_Tracker_Conceptual_Model" src="https://github.com/user-attachments/assets/b6709cd6-5e8b-4708-9627-5914f52ba025" />


## Entity Relationship Diagram

<img width="2602" height="1350" alt="Screenshot 2026-10-28 141752" src="https://github.com/user-attachments/assets/a9f3d56b-f781-45f4-90ec-ceb9b2ad69cd" />

## Entities

- Users
- Account_Info
- Transactions
- Expense_Category
- Merchant_Info
- Budget_Info

## Key Relationships

- Users (1:N) Account_Info
- Account_Info (1:N) Transactions
- Merchant_Info (1:N) Transactions
- Expense_Category (1:N) Transactions
- Users (1:N) Budget_Info
- Expense_Category (1:N) Budget_Info

## Design Decisions

- Merchant information is stored in a separate table to eliminate duplication and support merchant-level spending analysis.
- Expense categories are normalized to maintain data consistency and simplify reporting.
- Users can own multiple financial accounts.
- Transactions are classified as Credit or Debit to support both income and expense tracking.
- Budgets are maintained by category, month, and year to support historical budget tracking and comparisons.
- Foreign key relationships ensure referential integrity across the database.

## Business Questions Supported

- How much did a user spend in each category this month?
- What are the spending trends over time?
- Is a user staying within the allocated budget?
- Which merchants receive the highest spending?
- What is the average monthly spending of a user?

## Skills Demonstrated

- Data Modeling
- Database Design
- Entity Relationship Diagrams (ERD)
- Database Normalization
- Primary & Foreign Key Design
