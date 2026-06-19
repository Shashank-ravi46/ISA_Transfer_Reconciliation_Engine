ISA Transfer Reconciliation Engine

## Overview
Automated reconciliation system comparing internal position ledger vs custodian feed
for ISA accounts. Identifies exact matches, near-matches (via fuzzy logic), and
classifies operational breaks by type and priority.

## Tech Stack
- Python 3.10+ | pandas | rapidfuzz | openpyxl | plotly

## Reconciliation Stages
1. **Exact Match** — ISIN + Account ID outer merge
2. **Fuzzy Match** — rapidfuzz token_sort_ratio on residuals
3. **Break Classification** — 7 break types, 3 priority levels

## Output
- `reconciliation_report.xlsx` — colour-coded Excel workbook
- `waterfall_chart.html` — interactive Plotly break resolution
- `master_reconciliation_report.csv` — full audit trail
- `break_summary.json` — machine-readable summary

## Regulatory Context
Aligns with FCA ISA transfer SLAs: 15 working days (cash) / 30 days (stocks).
Settlement convention: T+2.

## Author
Shashank Ravi | MSc Economics & Finance | King's College London
