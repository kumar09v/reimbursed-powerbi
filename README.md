# 💼 Power BI Expense Reimbursement Report

This Power BI project showcases a complete data cleaning and reporting process for an **expense reimbursement** dataset. The goal was to clean and transform raw data, apply business logic, and build interactive visuals for insights.

---

## ✅ Steps Completed

### 1. Data Cleaning (Power Query)
- **Corrected spelling and punctuation** issues in the `Expense Type` column.
- Standardized **project names** to ensure consistency.
- Created a **custom column** for `Currency`:
  - `INR` if `Amount >= 1000`
  - `USD` if `Amount < 1000`
  - `EURO` for any other case
  - new customer column `NewCurrency`

### 2. Currency Conversion
- Created a **custom column** `AmountInINR`
- Converted all values in the `Amount` column to **INR** using exchange rates:
  - `USD → INR` = 83
  - `EURO → INR` = 90
  - `INR` and `blank` values were left unchanged

### 3. DAX Measures
- Created a measure to **sum the reimbursed amount in INR**.
- Used the `CALCULATE` function to filter and show **total reimbursement for `Project_B`**.
- Created a measure to **count declined requests**.

### 4. Visualizations
- **Slicer** for both Project and Employee
- **Column Chart**: Employee vs Amount
- **Pie Chart**: Project vs Amount

---

## 📊 Tools Used
- Power BI Desktop
- Power Query (M Language)
- DAX (Data Analysis Expressions)

---

## 🗂️ File Contents
- `Expense_Reimbursement.pbix`: Main Power BI report file
- `README.md`: Project documentation (this file)

---

## 📌 Notes
- Exchange rates used are fixed and assumed for demo purposes.
- Data used is sample data for learning and visualization practice.

---
