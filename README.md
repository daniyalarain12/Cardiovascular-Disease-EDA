# Cardiovascular Disease EDA — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.x-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-orange?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13.x-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

> A complete Exploratory Data Analysis on 70,000 patient records — uncovering cardiovascular disease risk factors including age, BMI, blood pressure and cholesterol levels using Python, Pandas, NumPy, Matplotlib and Seaborn.

---

## 📁 Repository Structure

```
Cardiovascular-Disease-EDA/
│
├── Cardiovascular_Disease_Analysis.ipynb
├── cardio_train.csv
└── README.md
```

---

## 📂 Dataset

| Detail | Info |
|--------|------|
| **File** | cardio_train.csv |
| **Source** | [Kaggle — Cardiovascular Disease Dataset](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset) |
| **Rows** | 70,000 patients |
| **Columns** | 13 |
| **Separator** | Semicolon (;) |
| **Target Column** | `cardio` — 0 = No Disease, 1 = Has Disease |
| **Age Range** | ~29 to ~65 years |

### Column Description

| Column | Description | Values |
|--------|-------------|--------|
| `age` | Patient age | In days (converted to years) |
| `gender` | Gender | 1 = Female, 2 = Male |
| `height` | Height | cm |
| `weight` | Weight | kg |
| `ap_hi` | Systolic blood pressure | Continuous |
| `ap_lo` | Diastolic blood pressure | Continuous |
| `cholesterol` | Cholesterol level | 1=Normal, 2=Above Normal, 3=Well Above Normal |
| `gluc` | Glucose level | 1=Normal, 2=Above Normal, 3=Well Above Normal |
| `smoke` | Smoking status | 0=No, 1=Yes |
| `alco` | Alcohol intake | 0=No, 1=Yes |
| `active` | Physical activity | 0=No, 1=Yes |
| `cardio` | Cardiovascular disease | 0=No Disease, 1=Has Disease |

---

## 🧹 Data Cleaning

| Step | Action |
|------|--------|
| Dropped column | `id` — unique identifier, not needed for analysis |
| Age conversion | Converted from days to years — `age / 365` then `astype(int)` |
| Blood pressure filter | Removed unrealistic readings — `ap_hi` 60–180, `ap_lo` 40–120 |
| BMI calculation | Computed from height and weight — `weight / (height/100)²` using `np.square()` |
| BMI filter | Removed unrealistic values — kept only BMI between 10 and 60 |

---

## 📊 Analyses Performed

| # | Analysis | Chart Type | Key Question |
|---|----------|------------|-------------|
| 01 | Cardiovascular Disease Distribution | Pie Chart | What % of patients have cardiovascular disease? |
| 02 | Age Distribution of Patients | Histogram + axvline | What age group is most common? |
| 03 | Age vs Disease by Smoking Status | Box Plot | Are older/smoking patients at higher risk? |
| 04 | BMI Distribution | Histogram + 3 axvlines | How many patients fall in each WHO BMI category? |
| 05 | Cholesterol vs Disease Rate | Bar Plot | Does higher cholesterol increase disease risk? |
| 06 | Height vs Weight by Disease | Scatter Plot | Is there a height-weight pattern in disease patients? |
| 07 | Blood Pressure Trend by Age | Line Plot | Does BP increase as patients get older? |
| 08 | Final Dashboard | 3x2 Subplots | All 6 analyses in one complete view |

---

## 🔑 Key Insights

- Dataset is nearly **balanced** — roughly 50% disease, 50% no disease
- Patients with **Well Above Normal cholesterol** have ~76% cardiovascular disease rate vs ~44% for normal cholesterol
- **Older patients** have significantly higher disease rates — age is a strong risk factor
- **Blood pressure increases consistently** with age across all patients
- Most patients fall in the **Overweight to Obese BMI range** (25–35)
- Smoking showed **no clear pattern** in this dataset — likely due to underreporting

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| **Pandas** | Data loading, cleaning, filtering and transformation |
| **NumPy** | BMI calculation using `np.square()` and numerical operations |
| **Matplotlib** | Pie chart, histograms, line plot and subplots dashboard |
| **Seaborn** | Box plot, bar plot and scatter plot with automatic hue coloring |

---

## ▶️ How to Run

1. Clone the repository
```bash
git clone https://github.com/daniyalarain12/Cardiovascular-Disease-EDA.git
```

2. Install required libraries
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Launch Jupyter Notebook
```bash
jupyter notebook
```

4. Open `Cardiovascular_Disease_Analysis.ipynb` and run all cells

---

## 🗺️ My Data Science Learning Journey

This project is part of my ongoing Data Science & AI Engineering roadmap:

| Repository | Status |
|-----------|--------|
| [Python — Basics to Advanced](https://github.com/daniyalarain12/Python-Basics-to-Advanced) | ✅ Completed |
| [NumPy — Basics to Advanced](https://github.com/daniyalarain12/NumPy-Basics-To-Advanced) | ✅ Completed |
| [Pandas — Basics to Advanced](https://github.com/daniyalarain12/Pandas-Basics-to-Advanced) | ✅ Completed |
| [Matplotlib — Basics to Advanced](https://github.com/daniyalarain12/Matplotlib-Basics-to-Advanced) | ✅ Completed |
| [Netflix EDA — Project](https://github.com/daniyalarain12/Netflix-EDA-Visualization) | ✅ Completed |
| [Seaborn — Basics to Advanced](https://github.com/daniyalarain12/Seaborn-Basics-to-Advanced) | ✅ Completed |
| [IPL Data Analysis — Project](https://github.com/daniyalarain12/IPL-Data-Analysis) | ✅ Completed |
| **Cardiovascular Disease EDA — Project** | ✅ Completed |
| Machine Learning | 🔜 Coming Soon |

---

## 📬 Connect With Me

[![GitHub](https://img.shields.io/badge/GitHub-daniyalarain12-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/daniyalarain12)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniyal-arain)

---

⭐ **If you find this repository helpful, please give it a star!** ⭐
