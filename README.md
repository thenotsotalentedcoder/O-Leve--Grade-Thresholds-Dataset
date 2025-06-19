# O-Level Grade Thresholds Dataset

## Overview
This dataset contains grade threshold data for Cambridge O-Level examinations from 2016-2024, covering the impact of COVID-19 on grading standards.

**O-Levels (Ordinary Levels)** are internationally recognized academic qualifications offered by Cambridge Assessment International Education. They are typically taken by students aged 14-16 and serve as:
- Foundation for higher secondary education (A-Levels)
- Equivalent to GCSE in the UK education system

### Grading System
O-Levels use letter grades from **A*** (highest) to **E** (passing), with **U** (ungraded/fail). Grade thresholds are the minimum marks required to achieve each grade, set after each examination session based on student performance.

## Dataset Structure

### File 1: Overall Thresholds (`overall_thresholds.csv`)
Contains **188 records** of complete subject grade boundaries.

| Column | Description | Example |
|--------|-------------|---------|
| `Year` | Examination year | 2023 |
| `Session` | Exam session (M_J = May/June, O_N = October/November, July = July 2021 special) | M_J |
| `Subject` | Subject name | Mathematics |
| `Max_Total_Mark` | Maximum possible marks for the complete subject | 200 |
| `Grade_A_Star_Threshold` | Minimum marks needed for A* grade (highest) | 172 |
| `Grade_A_Threshold` | Minimum marks needed for A grade | 145 |
| `Grade_B_Threshold` | Minimum marks needed for B grade | 105 |
| `Grade_C_Threshold` | Minimum marks needed for C grade | 66 |
| `Grade_D_Threshold` | Minimum marks needed for D grade | 52 |
| `Grade_E_Threshold` | Minimum marks needed for E grade (lowest passing) | 39 |
| `COVID_Period` | Time period classification | Post_COVID |

### File 2: Component Thresholds (`component_thresholds.csv`)
Contains **413 records** of individual paper/component grade boundaries.

| Column | Description | Example |
|--------|-------------|---------|
| `Year` | Examination year | 2023 |
| `Session` | Exam session | M_J |
| `Subject` | Subject name | Mathematics |
| `Component` | Paper/component number (12=Paper 1, 22=Paper 2, 42/62=ATP) | 12 |
| `Max_Mark` | Maximum marks for this specific paper | 80 |
| `Grade_A_Threshold` | Minimum marks for A grade on this paper | 61 |
| `Grade_B_Threshold` | Minimum marks for B grade on this paper | 45 |
| `Grade_C_Threshold` | Minimum marks for C grade on this paper | 29 |
| `Grade_D_Threshold` | Minimum marks for D grade on this paper | 22 |
| `Grade_E_Threshold` | Minimum marks for E grade on this paper | 16 |
| `COVID_Period` | Time period classification | Post_COVID |

## Key Features

### Time Periods
- **Pre_COVID** (2016-2019): Normal examination conditions
- **During_COVID** (2020-2021): Modified assessments and grading
- **Post_COVID** (2022-2024): Return to normal with adjusted standards

### Subjects Covered
- **Core**: Mathematics, English Language, Urdu, Pakistan Studies, Islamiat
- **Sciences and Commerce**: Computer Science, Biology, Chemistry, Physics, Additional Mathematics, Business Studies, Economics

### Component Numbers (Paper Types)
- **12**: Theory Paper 1 (usually multiple choice or structured questions)
- **22**: Theory Paper 2 (usually structured questions and essays)
- **42/62**: Alternative to Practical (ATP) - practical/coursework assessment

## AI/ML Project Ideas

### 1. Grade Prediction Model
Build a machine learning model to predict likely overall grades based on individual component scores. Use historical threshold data to train models that can forecast final grades given performance on Theory 1, Theory 2, and ATP components.

### 2. Educational Analytics Dashboard
Create an interactive web application with visualizations showing grade threshold trends, subject comparisons, and COVID-19 impact analysis. Include features for students to explore historical data and understand grading patterns.

### 3. Multi-Component Grade Optimization *(Fun but Challenging)*
Create an intelligent system that recommends optimal score distributions across different papers (Theory 1, Theory 2, ATP) to achieve target grades, considering each component's weight and historical threshold patterns.
