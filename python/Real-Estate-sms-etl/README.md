# 🏠 Real Estate SMS Marketing - ETL Pipeline

This project performs a comprehensive **ETL (Extract, Transform, Load)** process on a database of expired property listings to prepare data for automated SMS marketing campaigns.

## 🚀 Key Features
* **Data Cleaning:** Automates the removal of records missing mobile contact information and handles the normalization of phone numbers.
* **Transformation:** Uses intelligent concatenation to merge Address, City, State, and Zip columns into a single standardized "Full Address" format.
* **Messaging Logic:** Implements a rotation of 3 distinct message templates using a modulo operator on the dataframe index. This approach helps bypass SPAM filters by ensuring variety in the sent texts while dynamically inserting the specific property address.

## 🛠️ Tech Stack
* **Python 3.13**
* **Pandas:** Main library used for data manipulation, filtering, and cleaning.
* **Openpyxl:** Engine used for reading the raw property data and exporting the final results to Excel.

## 📊 Project Workflow
1. **Load:** Import raw Excel data containing over 50 property detail columns.
2. **Process:** Filter out entries without mobile numbers and extract the primary contact from multiple entries.
3. **Format:** Generate personalized SMS drafts for each lead.
4. **Export:** Deliver a clean, 3-column spreadsheet (`Full Address`, `Mobile Cleaned`, `SMS`) ready for marketing software.

---
*Note: For privacy and security reasons, the original raw data files (.xlsx) are not included in this repository