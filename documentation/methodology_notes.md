# Methodology Notes

## Project Title

**Auto Loan ABS Credit Risk & Securitisation Analytics**

## Project Objective

The objective of this project is to build a structured credit risk analytics workflow for monitoring an Auto Loan Asset-Backed Securities portfolio.

The project uses **Power BI, DAX and Excel validation** to analyse portfolio exposure, borrower quality, collateral risk, delinquency, expected credit loss, realised losses, recoveries, prepayment behaviour, stress testing and investor reporting.

This project is positioned as a **BFSI credit risk analytics case study** focused on dashboard development, metric validation and business interpretation.

---

## Methodology Overview

The project followed this workflow:

1. Data understanding
2. Data preparation
3. Data modelling
4. DAX measure creation
5. Dashboard development
6. Excel validation
7. Business insight generation
8. Reporting and documentation

---

## 1. Data Understanding

The dataset was reviewed to understand the structure, granularity and business purpose of each table.

| Table        | Purpose                                                                        |
| ------------ | ------------------------------------------------------------------------------ |
| Loan_Master  | Loan-level borrower, exposure, vehicle, credit score, LTV, IFRS 9 and ECL data |
| DPD_History  | Monthly loan-level delinquency snapshot data                                   |
| Monthly_Loss | Pool-level monthly performance, loss, recovery and prepayment data             |
| Vintage_Data | Static pool or vintage-level performance reference data                        |

The key focus was to separate **loan-level analysis** from **pool-level monthly reporting** to avoid incorrect metric interpretation.

---

## 2. Data Preparation

The data was prepared before dashboard development.

Preparation steps included:

* Reviewing column names and business meaning
* Checking date fields such as `SnapshotDate` and `ReportingDate`
* Creating required risk bands such as CIBIL Band, LTV Band and Interest Rate Band
* Ensuring monetary fields were interpreted consistently
* Separating loan-level and pool-level calculations
* Preparing fields required for Power BI relationships, slicers and visuals

All monetary values were treated as **INR**.

---

## 3. Data Modelling

A structured Power BI data model was created to support dashboard reporting.

The main model logic was:

* `Loan_Master` is treated as the loan-level master table.
* `DPD_History` is connected to `Loan_Master` through `LoanID`.
* `Date_Table` is connected to `DPD_History` using `SnapshotDate`.
* `Date_Table` is connected to `Monthly_Loss` using `ReportingDate`.
* `Monthly_Loss` is treated as pool-level data and is not directly connected to `Loan_Master`.
* Stress testing and scenario tables are treated as supporting or disconnected tables.

This design avoids misleading segment-level loss analysis where the monthly loss table does not contain loan-level fields such as Region, Vehicle Type, Employment Type or IFRS 9 Stage.

---

## 4. DAX Measure Development

DAX measures were created to calculate portfolio, credit risk, delinquency, ECL, loss, prepayment, stress and investor reporting metrics.

| Category           | Example Metrics                                                  |
| ------------------ | ---------------------------------------------------------------- |
| Portfolio Exposure | Current Balance, Original Balance, Pool Factor, Total Loans      |
| Weighted Metrics   | WAC, WA LTV, WA CIBIL, WA DTI                                    |
| Delinquency        | 30+ DPD Balance, 60+ DPD Balance, 90+ DPD Balance, DPD Rates     |
| IFRS 9 ECL         | EAD, ECL Provision, ECL Rate, Average PD, Average LGD            |
| Loss & Recovery    | Gross Loss, Recoveries, Net Loss, Recovery Rate, Loss Rate       |
| Prepayment         | Prepayment Amount, Prepayment Rate, CPR, SMM                     |
| Stress Testing     | Stressed ECL, ECL Increase, Credit Enhancement, CE Adequacy      |
| Investor Reporting | BOP Balance, EOP Balance, Amortisation, Prepayments, Pool Factor |

The measures were designed to support both dashboard visuals and Excel validation.

---

## 5. Dashboard Development

The Power BI dashboard was developed as an eight-page credit risk monitoring framework.

| Page                       | Analytical Focus                                        |
| -------------------------- | ------------------------------------------------------- |
| Executive Risk Overview    | High-level portfolio health and risk summary            |
| Portfolio Composition      | Borrower, collateral and exposure mix                   |
| DPD & Delinquency Analysis | Arrears, overdue amount and delinquency severity        |
| IFRS 9 ECL Analysis        | Expected credit loss and provisioning view              |
| Loss & Recovery Analysis   | Realised losses, recoveries and net loss impact         |
| Prepayment Analysis        | Prepayment speed and pool run-off behaviour             |
| Stress Testing Analysis    | Adverse scenario impact and credit enhancement adequacy |
| Investor Report            | Monthly pool movement and reporting-ready metrics       |

The dashboard was structured to move from portfolio overview to detailed risk monitoring and then to investor-style reporting.

---

## 6. Excel Validation

Excel was used as an independent validation layer for Power BI dashboard metrics.

The validation process included:

* Recalculating key dashboard values in Excel
* Comparing Excel results with Power BI visual values
* Validating major DAX measure logic
* Checking page-wise KPI cards
* Documenting match status
* Reviewing assumptions and limitations

Validation was performed for:

* Executive Risk Overview
* Portfolio Composition
* DPD & Delinquency Analysis
* IFRS 9 ECL Analysis
* Loss & Recovery Analysis
* Prepayment Analysis
* Stress Testing Analysis
* Investor Report

The purpose of validation was to ensure that dashboard values were not only visually correct but also numerically reconciled.

---

## 7. Business Insight Generation

After dashboard creation and validation, the metrics were interpreted from a credit risk and securitisation perspective.

The analysis focused on:

* Portfolio size and amortisation
* Borrower credit quality
* Collateral leverage
* DPD migration and severe delinquency
* Expected credit loss burden
* Realised loss and recovery performance
* Prepayment speed
* Credit enhancement adequacy under stress
* Investor reporting readiness

The insights were written in business language so the project can be understood by risk analysts, portfolio managers, securitisation teams and recruiters.

---

## 8. Reporting and Documentation

The final outputs were organised into a professional submission and GitHub portfolio format.

Project outputs include:

* Power BI dashboard
* Excel validation workbook
* Main report
* Presentation deck
* Dashboard screenshots
* Supporting screenshots
* Data dictionary
* Assumptions notes
* Methodology notes
* README file

The report and GitHub repository were structured to present the project as a complete BFSI credit risk analytics case study.

---

## Key Methodological Decisions

| Decision                                    | Reason                                                                                         |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Monthly_Loss kept separate from Loan_Master | Monthly_Loss is pool-level and does not contain loan-level segmentation fields                 |
| Excel validation added                      | To independently verify dashboard values                                                       |
| Stress testing included                     | To assess credit enhancement adequacy under adverse assumptions                                |
| Dashboard split into 8 pages                | To separate portfolio, delinquency, ECL, loss, prepayment, stress and investor reporting views |
| README and documentation prepared           | To make the GitHub repository understandable and portfolio-ready                               |

---

## Tools Used

| Tool     | Purpose                                     |
| -------- | ------------------------------------------- |
| Power BI | Dashboard development and visual analytics  |
| DAX      | Metric calculation and business logic       |
| Excel    | Independent validation and reconciliation   |
| GitHub   | Portfolio hosting and project documentation |

---

## Methodology Summary

This project followed a complete analytics workflow from raw data understanding to dashboard development, validation and reporting.

The methodology focused on building a controlled credit risk monitoring system rather than only creating visuals. By combining Power BI dashboarding with Excel validation and business interpretation, the project demonstrates an end-to-end approach to Auto Loan ABS credit risk and securitisation analytics.
