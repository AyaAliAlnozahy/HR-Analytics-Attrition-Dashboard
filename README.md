# HR-Analytics-Attrition-Dashboard
Interactive HR Analytics Dashboard built using Power BI Desktop to analyze employee data, track key KPIs, and identify factors affecting employee attrition. The project provides insights into workforce trends and supports data-driven HR decisions.
# 📊 HR Analytics & Attrition Dashboard (Power BI Project)

## 📌 Project Overview

This project presents an interactive HR Analytics dashboard built using Power BI to analyze employee data and uncover key insights related to workforce composition and employee attrition.

The dashboard helps HR teams understand patterns, identify high-risk attrition areas, and support data-driven decision-making.

---

## 🎯 Business Objectives

* Analyze employee distribution by department, age, gender, and job role
* Track key HR KPIs such as employee count, average salary, and job satisfaction
* Identify factors influencing employee attrition
* Detect trends and patterns across different employee segments

---

## 📊 Key KPIs

* Employee Count
* Attrition Count & Attrition Rate
* Average Salary
* Average Age
* Job Satisfaction Score
* Gender Ratio

---

## 🧮 DAX Measures Used

```DAX
Employee Count = DISTINCTCOUNT(HR_Analytics[EmpID])

Attrition Count = 
CALCULATE([Employee Count], HR_Analytics[Attrition] = "Yes")

Attrition Rate = 
DIVIDE(
    [Attrition Count],
    CALCULATE([Employee Count], ALL(HR_Analytics[Attrition])),
    0
)

Average Age = AVERAGE(HR_Analytics[Age])

Average Salary = DIVIDE([Monthly Salary], [Employee Count])

Monthly Salary = SUM(HR_Analytics[MonthlyIncome])
```

---

## 📈 Dashboard Features

### 🔹 Overview Page

* Employee distribution by department and education
* KPI cards (Employee Count, Salary, Age, etc.)
* Employee count by age group

### 🔹 Attrition Analysis Page

* Attrition rate by job role, salary, and age
* Department-wise attrition comparison
* Insights into factors affecting employee turnover

---

## 🎛️ Interactivity Features

* Slicers (Department, Gender, Job Role, Age Group)
* Bookmark Navigation between pages
* Dynamic filtering and cross-highlighting

---

## 📸 Dashboard Preview

### Overview

![Overview](<img width="1347" height="717" alt="Overview" src="https://github.com/user-attachments/assets/f240f564-24c9-4b51-84eb-a8894e80fbd4" />
)

### Attrition Analysis

![Attrition](<img width="1337" height="717" alt="Attrition" src="https://github.com/user-attachments/assets/ab41301e-911d-4bc7-af70-f3b03957f962" />
)

---

## 🚀 Tools & Technologies

* Power BI Desktop
* DAX (Data Analysis Expressions)
* Data Modeling & Visualization

---

## 📌 Key Insights

* Attrition rate is higher in Sales department
* Employees with low job satisfaction are more likely to leave
* Frequent business travel increases attrition risk
* Younger employees show higher turnover trends

---

## 📎 How to Use

1. Download the `.pbix` file
2. Open using Power BI Desktop
3. Interact with filters and visuals

---

## 💡 Author

Aya Ali
