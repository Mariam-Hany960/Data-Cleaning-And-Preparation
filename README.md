# Corporate Data Cleaning & Quality Architecture

## 📊 Project Overview
This project documents the foundational Data Cleaning, Preparation, and Quality Assurance (QA) phase executed upon a corporate transactional dataset of 1,200+ records. The workflow transforms raw, anomalous data into a certified 'Gold Standard' single source of truth, optimized for downstream Exploratory Data Analysis (EDA) pipelines.

## 🚀 Key Features & Cleaning Architecture
- **Phase 1: Strategic Imputation (Handling Gaps):** Programmatically resolved 42 empty fields across parameters. Instead of using listwise deletion, continuous quantitative fields were strategically imputed using column-specific Medians and Modes to preserve statistical power.
- **Phase 2: Duplicate Row Constraints Auditing:** Identified and eliminated 18 redundant transaction records sharing identical `OrderID` keys, guaranteeing true uniqueness across rows.
- **Phase 3: Categorical Parsing & Temporal Standardization:** Standardized mixed strings, slashes, and text variations into a unified regional ISO 8601 standard format (`YYYY-MM-DD`). 
- **Phase 4: Case Uniformity & Whitespace Trimming:** Applied string manipulation functions (`strip()` and case normalization) to categorical vectors like `Product` and `PaymentMethod` to eradicate typographical formatting fragmentation.

## 📈 Diagnostic Quality Control Summary
The operational metrics documented before and after executing the cleansing workflows:

| Data Quality Indicator | Pre-Cleaned State (Raw) | Post-Cleaned State (Cleaned) | Remediation Action Taken |
| :--- | :---: | :---: | :--- |
| **Missing / Null Values** | 42 Empty Fields | 0 Null Fields (100% Complete) | Imputed via Column-Specific Median / Mode |
| **Duplicate Rows** | 18 Redundant Records | 0 Duplicates (True Uniqueness) | Removed duplicate rows sharing identical OrderID keys |
| **Date Format Anomalies** | Mixed Strings / Slashes | ISO 8601 Standard (`YYYY-MM-DD`) | Parsed, aligned, and normalized into a unified standard |
| **String Spacing & Case** | Messy Spacing & Padding | Clean Standardized Text Keys | Trimmed extra spaces and unified text case definitions |

## 📁 Repository Structure
- `Data_Cleaning_Quality_Report_1_DecodeLabs.pdf`: The official technical verification report and quality control sign-off artifact.
- `raw_dataset.xlsx` / `cleaned_dataset.xlsx`: The transactional dataset profiles before and after remediation.

## 🛠️ Technologies Used
- Data Quality Assurance (QA) & Data Cleaning
- Missing Value Imputation & Deduplication
- String Parsing & Structural Data Integrity
