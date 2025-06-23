# 🧪 Pathology ETL & SQL Analysis Demo (Python + SQLite)

This project simulates an end-to-end data engineering workflow for a pathology lab. It includes data generation, cleaning, transformation, and structured analysis using Python (pandas) and SQL (SQLite).

## 📌 Key Features

- 🔄 **ETL Pipeline** from raw CSV to structured SQLite database
- 🧪 Simulated pathology test types: *HbA1c, Glucose, Creatinine, Cholesterol*
- 📊 SQL Analysis for quality assurance and reporting
- 💡 Designed for healthcare data engineering interview showcase

---

## 🧱 Workflow Overview

### 1. **Simulated Data**
- `patients_df`: 10 patients with ID, name, gender, and date of birth
- `samples_df`: Randomized pathology test results with types, values, and dates

### 2. **ETL Process**
- **Merge patient + sample data**
- **Convert date formats and clean NULL values**
- **Export as CSV**
- **Load into SQLite database** (`Pathology.db`)

### 3. **SQL Reporting Examples**

| Report Type | Description |
|-------------|-------------|
| ✅ **Abnormal filter** | Remove abnormal HbA1c results (above 15%) |
| 🕒 **Latest sample** | Get each patient's most recent result |
| ♀♂ **Gender summary** | Average result values by gender and test type |
| 🎂 **Age group summary** | Classify by `<40`, `40–64`, `65+` and analyze average values |

---

## 📊 Example Output (Pivot Summary)

| patient_id | HbA1c | Glucose | Creatinine | Cholesterol |
|------------|-------|---------|------------|-------------|
| P001       | 4.8   | NaN     | 138.0      | NaN         |
| P002       | 5.1   | NaN     | 89.0       | NaN         |
| P004       | 6.1   | 9.1     | 111.0      | NaN         |
| P005       | 8.4   | NaN     | NaN        | 7.6         |

---

## 🛠 Skills Demonstrated

- `pandas` for data cleaning: `groupby`, `pivot_table`, `fillna`, `merge`
- `sqlite3` for query-based reporting: `JOIN`, `CASE`, `ROW_NUMBER`, `AVG`
- Simulated **ETL pipeline**
- Realistic healthcare data use case

---

## 💬 How to Use

```bash
# Run in Google Colab or Jupyter
!pip install pandas sqlite3

# Run the .ipynb notebook
