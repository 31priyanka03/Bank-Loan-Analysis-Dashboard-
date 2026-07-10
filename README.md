# 🏦 Bank Loan Analysis Dashboard (Power BI)

An end-to-end Power BI dashboard analyzing a bank's loan portfolio — covering loan volume, funding, repayment performance, and credit risk across **38,576 loan applications** issued between **January 2021 and December 2021**.

---

## 📌 Project Overview

This project analyzes a bank's lending data to answer key business questions:
- How much has the bank funded, and how much has it recovered?
- What percentage of the loan book is "good" (performing) vs "bad" (charged off)?
- Which loan purposes, grades, terms, and states carry the most risk?
- How has loan demand trended month over month?

The dashboard is built as a 3-page interactive Power BI report: **Summary**, **Overview**, and **Risk Analysis**.

---

## 🗂️ Dataset

| Field | Description |
|---|---|
| `ISSUE_DATE` | Date the loan was issued |
| `LOAN_STATUS` | Fully Paid / Current / Charged Off |
| `Good vs Bad` | Derived flag — Good (Fully Paid/Current) vs Bad (Charged Off) |
| `PURPOSE` | Reason for the loan (Debt Consolidation, Credit Card, etc.) |
| `GRADE` / `SUB_GRADE` | Credit grade assigned to the loan |
| `HOME_OWNERSHIP` | Rent / Mortgage / Own / Other |
| `ADDRESS_STATE` | Borrower's US state |
| `TERM` | 36 or 60 months |
| `INT_RATE` | Interest rate |
| `DTI` | Debt-to-income ratio |
| `LOAN_AMOUNT` | Amount funded |
| `TOTAL_PAYMENT` | Total amount received |
| `ANNUAL_INCOME`, `EMP_LENGTH`, `EMP_TITLE` | Borrower profile fields |

**Rows:** 38,576 | **Table:** `financial_loan`

---

## 📊 Dashboard Pages

### 1. Summary
KPI cards (Total Applications, Total Funded, Total Received, Avg Interest Rate, Avg DTI), Good vs Bad loan donut charts, and status-wise breakdowns of funded amount, applications, interest rate, and DTI.

### 2. Overview
Monthly application trend (line chart), loan term split (donut), applications by home ownership (bar), loan purpose breakdown (treemap), and a US state map of applications with average interest rate.

### 3. Risk Analysis
Portfolio Risk Score (gauge), a Grade × Loan Status pivot table, and a state-wise Bad Loan % bar chart to flag high-risk geographies.

---

## 💡 Key Insights

**Portfolio Health**
- Total Loan Applications: **38,576**
- Total Funded Amount: **$435.76M**
- Total Amount Received: **$473.07M** — recoveries exceed funding at the portfolio level
- Average Interest Rate: **12.05%** | Average DTI: **13.33%**

**Loan Quality**
- **86.18%** of loans are Good (Fully Paid/Current) vs **13.82%** Bad (Charged Off)
- Bad loans returned only **$37.28M** against **$65.53M** funded — the primary loss driver in the portfolio

**Borrower Behavior**
- **Debt Consolidation** is the dominant purpose (18,214 apps, ~47% of all loans)
- Credit grades skew safe: **B (30%) > A (25%) > C (20%)**, with F/G grades under 4% combined
- **73%** of loans are 36-month terms; 60-month loans carry a notably higher average interest rate (~15.1% vs ~11–12%)
- Renters (18,439) and mortgage-holders (17,198) make up the vast majority of borrowers

**Geographic Risk**
- Highest application volume: **California, New York, Florida, Texas**
- Highest bad-loan rates (among states with 100+ applications): **Nevada (20.95%), Florida (17.27%), Hawaii (16.47%)** — flagged as elevated-risk regions despite lower volume

**Growth Trend**
- Monthly applications grew from **~2,332 in January to ~4,314 in December**, an ~85% increase over the year

---

## 🛠️ Tools & Techniques Used
- **Power BI Desktop** — data modeling, DAX measures, interactive visuals
- **DAX** — custom measures (Good/Bad Loan %, Portfolio Risk Score, MTD/aggregated KPIs)
- **Data Modeling** — star-schema style table with date hierarchies
- Visuals: KPI cards, donut/column/bar charts, treemap, filled map, gauge, pivot table, slicers

---



## 🚀 How to Use
1. Clone/download this repo
2. Open `dashboard.pbix` in **Power BI Desktop**
3. Use the slicers (Purpose, Grade, Term, Loan Status) to filter and explore

---

## 👤 Author
*Your Name* — feel free to connect on [LinkedIn](#) or check out more projects on [GitHub](#).
