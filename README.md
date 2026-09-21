# E-Commerce Data Cleaning & Reporting Automation

> Turning messy recurring e-commerce transaction exports into
> validated, analysis-ready data and automated business reports.

## Project Status

    Phase 1 — Business Understanding

This project uses the publicly available UCI Online Retail II dataset to simulate an e-commerce reporting automation engagement. The business scenario, reporting workflow and automation requirements are constructed for portfolio and demonstration purposes.

    Phase 2 — Data Understanding

## 2.2.11 Non-Standard StockCode Investigation

The `StockCode` field contains both numeric-leading and alphabetic-leading
values. Further investigation showed that alphabetic StockCodes do not
represent a single type of data-quality problem.

Several codes are associated with operational or financial transactions.
For example:

- `C2` is associated with `CARRIAGE`.
- `ADJUST` is associated with adjustment records.
- `BANK CHARGES` is associated with bank charge transactions.
- `AMAZONFEE` is associated with Amazon fee transactions.
- `M` represents another non-standard transaction type with a substantial
  number of negative-quantity records.
- `POST` occurs frequently and represents a non-standard transaction
  category requiring separate treatment.
- `DOT`, `DCGS...`, `gift_0001_*`, and other codes also appear in the
  non-standard StockCode population.

Some non-standard codes have substantial missing `Customer ID` values,
while others contain positive or negative quantities and zero or positive
prices.

### Key Finding

Alphabetic or non-numeric `StockCode` values cannot be treated as invalid
product records solely because they are non-numeric.

The investigation indicates that the raw dataset contains multiple
transaction types beyond ordinary merchandise sales, including operational,
financial, shipping, fee, adjustment, gift, and test-like records.

### Data-Quality Implications

The cleaning pipeline should therefore classify transaction records based
on multiple fields rather than removing rows solely according to the
`StockCode` format.

Relevant fields for later transaction classification include:

- `StockCode`
- `Description`
- `Invoice`
- `Quantity`
- `Price`
- `Customer ID`

No records are removed at this stage. Final inclusion/exclusion rules will
be established during the Data Preparation phase after transaction
classification has been completed.

## Business Problem

Coming soon.

## Solution

Coming soon.

## Dataset

Online Retail II — UCI Machine Learning Repository.

## Methodology

CRISP-DM

## Technology

- Python
- Pandas
- NumPy
- Excel
- Matplotlib
- pytest

## Project Architecture

Coming soon.

## Results

Coming soon.

## How to Run

Coming soon.

## Portfolio Case Study

Coming soon.

## Loom Demonstration

Coming soon.

## Data Source

UCI Machine Learning Repository