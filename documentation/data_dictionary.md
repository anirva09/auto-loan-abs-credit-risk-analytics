# Data Dictionary

This project uses synthetic Auto Loan ABS data for credit risk analytics, securitisation monitoring and investor reporting.

## Loan_Master

Loan-level table containing borrower, vehicle, exposure and credit risk fields.

Key fields:
- LoanID
- OriginalLoanAmount
- CurrentBalance
- InterestRate
- CIBIL_Score_Current
- LTV_Current
- DTI_Ratio
- Region
- VehicleType
- EmploymentType
- IFRS9_Stage
- PD_Estimate
- LGD_Estimate
- EAD
- ECL_Provision
- LossAmount
- RecoveryAmount
- NetLoss

Used for:
- Executive Risk Overview
- Portfolio Composition
- IFRS 9 ECL Analysis
- Stress Testing

## DPD_History

Snapshot-level delinquency table used to monitor arrears and DPD migration.

Key fields:
- LoanID
- SnapshotDate
- DPD_Days
- DPD_Bucket
- CurrentBalance
- Amount_Overdue

Used for:
- DPD & Delinquency Analysis

## Monthly_Loss

Pool-level monthly performance table.

Key fields:
- ReportingDate
- BOP_Balance
- EOP_Balance
- ScheduledAmort
- Prepayments
- GrossLoss_ThisMonth
- Recoveries_ThisMonth
- NetLoss_ThisMonth
- SMM
- CPR_Annualised

Used for:
- Loss & Recovery Analysis
- Prepayment Analysis
- Investor Report

## Vintage_Data

Static pool or vintage-level supporting table used for portfolio performance reference.

Key fields:
- Vintage_Month
- Original_Pool_Balance
- Cumulative_Defaults
- Cumulative_Loss
