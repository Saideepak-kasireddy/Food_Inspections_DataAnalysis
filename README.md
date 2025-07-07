# 🥗 Food Inspections Data Analysis: Chicago & Dallas

This project analyzes food inspection data from two major cities — **Chicago** and **Dallas** — using a modern data engineering and BI approach. The goal is to profile, clean, model, and visualize food establishment inspection results, providing insights into inspection outcomes, violations, and risk factors.

---

## 📂 Data Sources

- **Chicago Food Inspections:**
  - [City of Chicago Open Data Portal](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections/4ijn-s7e5)

- **Dallas Food Inspections:**
  - [Dallas Open Data Portal](https://www.dallasopendata.com/Services/Restaurant-and-Food-Establishment-Inspections-Octo/dri5-wcct)

---

## 🛠️ Tools & Technologies

- **Data Processing & ETL:**
  - Alteryx (Profiling)
  - Databricks (Cleaning, transformation, medallion architecture)
  - Azure Data Factory (Orchestration)
  - Snowflake (Data warehouse)

- **Visualization:**
  - Power BI

---

## 📐 Project Architecture

This project follows the **Medallion Architecture**:

1. **Bronze Layer:**
   - Load raw TSV data into stage tables (`stg_` prefix).
   - Profile and document data issues.

2. **Silver Layer:**
   - Cleanse and standardize data.
   - Convert data to Parquet format.
   - Apply schema alignment across both cities despite structural differences.

3. **Gold Layer:**
   - Design and deploy a dimensional model with fact and dimension tables:
     - Dimensions: e.g., `dim_business`, `dim_location`, `dim_violation`
     - Fact table: `fact_inspections`
   - Source-to-target mappings documented.

4. **BI Layer:**
   - Build dashboards in Power BI showing inspection trends, violation patterns, facility risks, and detailed inspection reports.

---

## 📊 Dashboard Requirements

The final BI dashboards visualize insights from the data, including:

- Inspection results distribution (pass, fail, etc.)
- Inspection types (routine, complaint, license, etc.)
- Risk categories
- Facility types (restaurant, grocery, etc.)
- Violations — codes and descriptions
- Business details (DBA, AKA, license)
- Inspection locations (maps)
- Inspection-level report with inspection #, license #, violations, and inspector comments

---

## ✅ Deliverables

✔️ **Data Profiling Reports** — Clear documentation of data quality issues  
✔️ **Data Cleansing Steps** — Transformations, adjustments, and standardizations performed  
✔️ **Dimensional Model** — Deployed in Snowflake with prefixed `dim_` and `fact_` tables  
✔️ **BI Dashboards** — Comprehensive Power BI reports for business users  
✔️ **Screenshots & Documentation** — Proof of results as required

---

## 📝 Good Practices Followed

- Adhered to best practices discussed in class, including clear data lineage, proper medallion layer separation, and meticulous documentation.
- Ensured consistency across datasets from different cities by harmonizing schema and data types.
- Applied rigorous profiling to highlight missing, inconsistent, or invalid records.
- Incorporated detailed comments on cleansing logic and modeling decisions.

---

## 🔗 References

- [Chicago Food Inspections Dashboard](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb)
- [Chicago Health Code Requirements](https://www.chicago.gov/city/en/depts/cdph/provdrs/food_safety/svcs/understand_healthcoderequirementsforfoodestablishments.html)
- [Chicago Business Licenses](https://data.cityofchicago.org/Community-Economic-Development/Business-Licenses/r5kz-chrr)

---

## 📎 Author

*This project was developed as part of a data engineering and analytics coursework assignment, demonstrating end-to-end data pipeline design and BI storytelling capabilities.*

---

Feel free to fork or contribute!

