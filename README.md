# E-Commerce Data Cleaning & Reporting Automation

> Turning messy recurring e-commerce transaction exports into validated, analysis-ready data and automated business reports.

## Project Status

**Phase 2 — Data Understanding Complete**
**Phase 3 — Data Preparation Next**

This project uses the publicly available **UCI Online Retail II** dataset to simulate an e-commerce reporting automation engagement. The business scenario, reporting workflow, and automation requirements are constructed for portfolio and demonstration purposes.

The project follows the **CRISP-DM** methodology and focuses on building a repeatable workflow for transforming messy transaction exports into validated business information and management-ready reports.

---

## Business Problem

Recurring e-commerce transaction exports can contain missing customer information, duplicate records, cancellations, returns, inconsistent transaction types, non-merchandise records, unusual prices, and other data-quality issues.

When these exports are prepared manually for reporting, the process can be time-consuming and may introduce inconsistent business rules or reporting errors.

The business need is to establish a repeatable process that can:

* ingest recurring transaction exports
* identify and document data-quality issues
* apply consistent business rules
* distinguish sales, returns, cancellations, and other transaction types
* produce validated analysis-ready data
* calculate reliable business metrics
* generate management-ready reports with minimal manual intervention

---

## Solution

The project is developing a modular Python-based data pipeline that will transform raw e-commerce transaction exports into validated analytical datasets and automated business reports.

The solution will include:

1. **Data ingestion** — loading recurring transaction exports.
2. **Data profiling** — identifying completeness, duplication, validity, and structural issues.
3. **Data preparation** — applying documented cleaning and business rules.
4. **Transaction classification** — distinguishing merchandise sales, returns, cancellations, adjustments, and other transaction types.
5. **Business metrics** — calculating validated sales and performance measures.
6. **Automated reporting** — generating recurring business reports from the processed data.
7. **Validation and testing** — checking that the pipeline produces reliable outputs.

The objective is not simply to clean one dataset, but to demonstrate a workflow that can be adapted to recurring e-commerce reporting processes.

---

## Dataset

**Online Retail II — UCI Machine Learning Repository**

The dataset contains transaction-line records from an online retailer covering December 2009 through December 2011.

The workbook contains two reporting-period worksheets:

* `Year 2009-2010`
* `Year 2010-2011`

Combined, the dataset contains approximately **1.07 million transaction-line records** across eight fields.

### Data Source

UCI Machine Learning Repository:

https://archive.ics.uci.edu/dataset/502/online%2Bretail

The dataset is used under its published **CC BY 4.0** license.

The raw dataset is retained locally and is not committed to the repository.

---

## Methodology

The project follows **CRISP-DM**:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment

The current project stage is:

> **Business Understanding ✅**
> **Data Understanding ✅**
> **Data Preparation ⏭️**

---

## Technology

* Python
* Pandas
* NumPy
* Excel
* Matplotlib
* pytest
* Git / GitHub

---

## Project Architecture

```text
E-Commerce-Data-Cleaning-Reporting-Automation/
│
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
│
├── docs/
│
├── notebooks/
│
├── src/
│
├── reports/
│
├── tests/
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

The project is being developed as a modular workflow so that data preparation, validation, analysis, and reporting can be maintained separately.

---

## Current Data Understanding

Initial investigation identified several important characteristics of the raw data:

* The dataset is transaction-line based rather than one row per invoice.
* Invoice numbers can legitimately appear across multiple rows.
* Customer ID contains substantial missingness.
* Description contains a smaller amount of missing data.
* Exact duplicate transaction rows exist and require business-rule-based investigation.
* Negative quantities occur and are associated with returns and cancellation activity.
* Zero-price and negative-price records exist.
* The dataset contains operational and financial transaction types in addition to ordinary merchandise transactions.
* StockCodes can be numeric or alphanumeric and cannot be classified solely by their format.
* Invoice dates are complete across the observed records.
* Country information is complete, although country labels may require semantic standardization.
* Transaction values contain unusual and extreme observations that require contextual treatment rather than automatic removal.

No records have been removed or transformed as part of Data Understanding.

Cleaning and inclusion/exclusion rules will be established during **Data Preparation**.

---

## Results

**In progress**

Final results will document:

* data-quality improvements
* validated transaction classifications
* cleaned analytical datasets
* business performance metrics
* reporting outputs
* validation and testing results
* automation workflow

---

## How to Run

**To be completed after the data pipeline and reporting workflow are implemented.**

The final instructions will cover:

1. Environment setup
2. Dependencies
3. Raw data placement
4. Pipeline execution
5. Validation
6. Report generation

---

## Portfolio Case Study

**Coming after project completion.**

The final case study will present the project from a business perspective, including:

* business problem
* approach
* data-quality challenges
* solution
* business insights
* automation workflow
* measurable project impact

---

## Loom Demonstration

**Coming after project completion.**

A short demonstration will show the workflow from raw transaction data through the cleaning pipeline and automated reporting output.

---

## License

This project is released under the license included in this repository.

The underlying **Online Retail II** dataset is provided by the UCI Machine Learning Repository under **CC BY 4.0**.

## Data Source

**UCI Machine Learning Repository — Online Retail II**

https://archive.ics.uci.edu/dataset/502/online%2Bretail
