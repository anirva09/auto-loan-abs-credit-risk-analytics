# Auto Loan ABS Credit Risk & Securitisation Analytics

A Power BI and Excel-based BFSI analytics project built to monitor an Auto Loan Asset-Backed Securities portfolio across portfolio exposure, delinquency, IFRS 9 expected credit loss, realised losses, recoveries, prepayment behaviour, stress testing and investor reporting.

---

## Project Overview

This project presents an end-to-end **Auto Loan ABS Credit Risk & Securitisation Analytics** workflow using **Power BI, Excel and DAX**.

The dashboard converts loan-level and pool-level data into a structured risk monitoring framework. It helps analyse portfolio health, borrower quality, collateral risk, delinquency movement, expected credit loss, realised losses, recovery performance, prepayment speed, stress adequacy and investor reporting readiness.

The project is positioned as a **BFSI credit risk analytics case study** focused on dashboard development, data modelling, DAX measure creation, Excel validation and business interpretation.

---

## Business Problem

Auto Loan ABS portfolios require continuous monitoring because borrower repayment behaviour, delinquency, collateral risk, recoveries, prepayments and expected losses can change over time.

A credit risk or securitisation monitoring team needs to answer questions such as:

* Is the loan pool amortising as expected?
* Is portfolio credit quality stable?
* Where is delinquency building?
* What is the expected credit loss exposure?
* Are recoveries reducing realised loss impact?
* Is credit enhancement adequate under stress?
* Can the output support investor-style reporting?

This project solves the problem by creating a Power BI monitoring dashboard supported by Excel-based validation.

---

## Tools Used

| Tool     | Purpose                                     |
| -------- | ------------------------------------------- |
| Power BI | Dashboard development and visual analytics  |
| DAX      | Metric calculation and business logic       |
| Excel    | Independent validation and reconciliation   |
| GitHub   | Project documentation and portfolio hosting |

---

## Dashboard Modules

| Page | Module                     | Focus                                                   |
| ---- | -------------------------- | ------------------------------------------------------- |
| 1    | Executive Risk Overview    | High-level portfolio health and risk summary            |
| 2    | Portfolio Composition      | Borrower, collateral and exposure mix                   |
| 3    | DPD & Delinquency Analysis | Arrears, overdue amount and delinquency severity        |
| 4    | IFRS 9 ECL Analysis        | Expected credit loss and provisioning view              |
| 5    | Loss & Recovery Analysis   | Realised losses, recoveries and net loss impact         |
| 6    | Prepayment Analysis        | Prepayment speed and pool run-off behaviour             |
| 7    | Stress Testing Analysis    | Adverse scenario impact and credit enhancement adequacy |
| 8    | Investor Report            | Monthly pool movement and reporting-ready metrics       |

---

## Dashboard Preview

### Executive Risk Overview
<img width="2400" height="1350" alt="483553A_AnirvaManchikatla_Page01_Executive_Risk_Overview" src="https://github.com/user-attachments/assets/da2ad818-59e7-4014-ad97-52b84b77612e" />


### DPD & Delinquency Analysis
<img width="2400" height="1350" alt="483553A_AnirvaManchikatla_Page03_DPD_Delinquency_Analysis" src="https://github.com/user-attachments/assets/80df4f5b-f78b-45a2-bfb0-831216cd943a" />

### Stress Testing Analysis
<img width="2400" height="1350" alt="483553A_AnirvaManchikatla_Page07_Stress_Testing_Analysis" src="https://github.com/user-attachments/assets/8c0c8a5a-e4a6-4427-9ef5-2651916fa670" />

---

## Key Metrics Tracked

| Area               | Metrics                                                                    |
| ------------------ | -------------------------------------------------------------------------- |
| Portfolio Health   | Current Balance, Original Balance, Pool Factor, WAC, WA LTV, WA CIBIL      |
| Delinquency        | 30+ DPD Balance, 60+ DPD Balance, 90+ DPD Balance, Amount Overdue          |
| IFRS 9 ECL         | EAD, ECL Provision, ECL Rate, PD, LGD, Stage 3 Exposure                    |
| Loss & Recovery    | Gross Loss, Recoveries, Net Loss, Recovery Rate, Loss Rate                 |
| Prepayment         | Prepayment Rate, CPR, SMM, Latest Pool Balance                             |
| Stress Testing     | Stressed ECL, ECL Increase, Credit Enhancement, CE Adequacy                |
| Investor Reporting | BOP Balance, EOP Balance, Scheduled Amortisation, Prepayments, Pool Factor |

---

## Data Model Summary

The project uses a structured data model consisting of:

* `Loan_Master`
* `DPD_History`
* `Monthly_Loss`
* `Vintage_Data`
* `Date_Table`
* Supporting stress and scenario tables

The model separates loan-level data from pool-level monthly data.

`Monthly_Loss` is treated as pool-level data and is intentionally not directly connected to `Loan_Master` because it does not contain loan-level segmentation fields such as Region, Vehicle Type, Employment Type or IFRS 9 Stage.

This prevents misleading segmented loss analysis and keeps the dashboard aligned with the correct data grain.

---

## Key Insights

* The portfolio has a current balance of **₹317.8M** across **500 loans**.
* The pool factor of **58.2%** indicates meaningful amortisation from the original balance.
* The weighted average CIBIL score of **742** suggests relatively stable borrower quality.
* The **30+ DPD rate of 4.7%** acts as an early-warning delinquency indicator.
* The **90+ DPD rate of 2.0%** highlights severe delinquency exposure.
* The ECL rate of **3.7%** provides a controlled expected-loss view.
* Monthly gross loss of **₹12.2M** is reduced by recoveries of **₹4.4M**, resulting in net loss of **₹7.8M**.
* Stress testing shows credit enhancement remains **Adequate** under the assumed 1.5x stress scenario.

---

## Validation Approach

Excel was used as an independent validation layer to reconcile dashboard values against raw data and formula logic.

The validation process included:

* Recalculating key dashboard values in Excel
* Comparing Excel results with Power BI visual values
* Validating major DAX measure logic
* Checking page-wise KPI cards
* Documenting match status
* Reviewing assumptions and limitations

Validation was performed across all eight dashboard modules to ensure the dashboard values were not only visually correct but also numerically reconciled.

---

## Project Outputs

| Output                    | Description                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------- |
| Power BI Dashboard        | Interactive dashboard covering credit risk, securitisation monitoring and investor reporting |
| Excel Validation Workbook | Independent reconciliation of key dashboard metrics                                          |
| Main Project Report       | Detailed explanation of methodology, dashboard logic, insights and assumptions               |
| Presentation Deck         | Executive-style summary of the project and findings                                          |
| Documentation             | Data dictionary, assumptions, methodology notes and validation notes                         |

---

## Assumptions and Limitations

* The dataset is treated as synthetic internship project data.
* All monetary values are in INR.
* M refers to Million and B refers to Billion.
* Stress testing uses a 1.5x stress multiplier.
* Credit enhancement is assumed at 8% of current balance.
* PD and LGD are treated as available estimates, not predictive model outputs.
* `Monthly_Loss` is pool-level data and is not directly connected to `Loan_Master`.
* The project does not include a full tranche-level cash-flow waterfall.
* Recovery Rate is validated according to the existing Power BI dashboard measure logic.

---

## Skills Demonstrated

* Power BI dashboard development
* DAX measure creation
* Credit risk analytics
* Auto Loan ABS monitoring
* IFRS 9 ECL analysis
* Delinquency and DPD analysis
* Loss and recovery analysis
* Prepayment analysis
* Stress testing
* Excel-based validation
* Business insight communication
* BFSI analytics reporting

---

## Project Positioning

This project demonstrates an end-to-end credit risk analytics workflow for Auto Loan ABS monitoring. It combines dashboard development, DAX-based metric logic, Excel validation and business interpretation to present the project as a professional BFSI analytics case study.

---

## Author

**Anirva Manchikatla**
B.Tech CSE | Data Analytics | BFSI Analytics | Credit Risk Analytics
