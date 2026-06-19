# 🏥 Healthcare EDA Assignment
### BrightLearn · AI & Data Skills · Practical Assignment (100 Marks)

---

## 📋 Project Overview

This project is an end-to-end Exploratory Data Analysis (EDA) of a real-world-style
healthcare admissions dataset containing approximately 55,500 hospital admission records.
The analysis was completed using Python and the pandas library inside a Jupyter Notebook,
written for a non-technical audience — specifically a hospital manager.

---

## 📁 Repository Contents

```
├── Healthcare_EDA_.ipynb       # Main Jupyter Notebook (all sections)
├── Heathcare_dataset.csv       # Raw dataset (55,500 rows · 15 columns)
└── README.md                   # This file
```

---

## 🗂️ Dataset

| Property | Detail |
|---|---|
| Rows | ~55,500 |
| Columns | 15 |
| Source | BrightLearn (synthetic healthcare admissions data) |
| File | `Heathcare_dataset.csv` |

**The 15 columns include:**
`Name`, `Age`, `Gender`, `Blood Type`, `Medical Condition`, `Date of Admission`,
`Doctor`, `Hospital`, `Insurance Provider`, `Billing Amount`, `Room Number`,
`Admission Type`, `Discharge Date`, `Medication`, `Test Results`

---

## 🔧 Tools & Libraries

- Python 3
- pandas
- matplotlib
- Jupyter Notebook

---

## 📓 Notebook Structure

The notebook is divided into 10 sections following the BrightLearn brief:

| Section | Description | Marks |
|---|---|---|
| 01 | Data Overview — shape, dtypes, sample | 10 |
| 02 | Data Dictionary — all 15 columns described | — |
| 03 | Data-Quality Checks — missing values, duplicates, unusual values | 15 |
| 04 | Data Cleaning — duplicates removed, dates converted, bad billing handled | 15 |
| 05 | Feature Engineering — 8 new columns using `.loc` pattern | 15 |
| 06 | EDA Analysis & Groupby — Q7 to Q18 answered with sorted tables | 20 |
| 07 | Visualisations — 6 labelled charts supporting the analysis | 10 |
| 08 | Written Insights — 6 evidence-based findings with real numbers | 15 |
| 09 | Executive Summary — 150–200 word plain-English summary | — |
| 10 | Recommendations — 4 actionable suggestions tied to insights | — |

---

## 🛠️ Feature Engineering

Eight new columns were created in Section 5:

| New Column | Description | Method |
|---|---|---|
| `Length_of_Stay` | Days between admission and discharge | Date arithmetic |
| `Admission_Year` | Year of admission | `.dt.year` |
| `Admission_Month` | Month number (1–12) | `.dt.month` |
| `Admission_Month_Name` | Month name (e.g. January) | `.dt.month_name()` |
| `Admission_Day_Name` | Weekday name (e.g. Monday) | `.dt.day_name()` |
| `Age_Group` | Child / Young Adult / Adult / Senior / Elderly | `.loc` |
| `Billing_Bucket` | Low / Medium / High / Very High | `.loc` |
| `Stay_Category` | Short / Medium / Long | `.loc` |

---

## 📊 Charts Produced

1. Bar Chart — Admissions by Medical Condition
2. Bar Chart — Patients by Insurance Provider
3. Histogram — Age Distribution of Patients
4. Line Chart — Total Admissions by Year
5. Bar Chart — Average Billing Amount by Medical Condition
6. Box Plot — Length of Stay by Admission Type
7. Pie Chart — Distribution of Test Results

---

## 🔍 Key Findings

1. All six medical conditions are recorded in near-equal volumes (~9,100–9,200 each), suggesting a synthetically balanced dataset.
2. Obesity generates the highest average bill at R25,859 per admission, above the dataset average of R25,595.
3. Elderly patients (age 66+) make up the largest age group at 29.3% of all admissions.
4. Asthma patients have the longest average stay at 15.7 days, impacting bed availability.
5. Admissions grew 53% from 2019 to 2020 and have remained stable since.
6. Patient load is evenly spread across all five insurance providers, with Cigna leading at 11,139 admissions.

---

## ✅ How to Run the Notebook

1. Clone or download this repository
2. Make sure `Heathcare_dataset.csv` is in the **same folder** as the notebook
3. Open `Healthcare_EDA_.ipynb` in Jupyter Notebook or JupyterLab
4. Click **Kernel → Restart & Run All**
5. The notebook should complete with no errors from top to bottom

---

## ⚠️ Data Cleaning Decisions

- **Duplicate rows** were removed using `drop_duplicates()`
- **Date columns** were converted from text to `datetime64` using `pd.to_datetime()`
- **Negative billing amounts** (106 rows) were set to `NaN` rather than deleted — preserving all other columns for those admissions while flagging the billing figure as unreliable
- **Patient names** were standardised to title case using `.str.title()`

---

## 📌 Academic Integrity

This is individual work submitted as part of the BrightLearn AI & Data Skills programme.
The code and write-up are the author's own. Submissions are checked for plagiarism.

---

*BrightLearn · Healthcare EDA Assignment · 100 Marks*
