# Assumptions and Notes

## Project Assumptions

- The dataset is treated as synthetic internship project data.
- All monetary values are in INR.
- M refers to Million.
- B refers to Billion.
- Stress testing uses a 1.5x stress multiplier.
- Credit enhancement is assumed at 8% of current balance.
- PD and LGD are treated as available estimates, not predictive model outputs.
- Monthly_Loss is treated as pool-level monthly data.
- Monthly_Loss is intentionally not directly connected to Loan_Master because it does not contain loan-level segmentation fields such as region, vehicle type, employment type or IFRS 9 stage.
- The project does not include a full tranche-level cash-flow waterfall.
- Recovery Rate is validated according to the existing Power BI dashboard measure logic.

## Validation Notes

Excel was used as an independent validation layer to reconcile key Power BI dashboard values against raw data and formula logic.

Validation covered:
- Executive risk metrics
- Portfolio composition metrics
- DPD and delinquency metrics
- IFRS 9 ECL metrics
- Loss and recovery metrics
- Prepayment metrics
- Stress testing metrics
- Investor reporting metrics

## Project Scope

This project is designed as a BFSI credit risk analytics case study using Power BI, Excel and DAX. It focuses on monitoring, validation and business interpretation rather than production-grade banking implementation.
