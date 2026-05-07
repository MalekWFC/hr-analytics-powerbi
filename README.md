# HR Analytics: Employee Performance & Attrition Insights

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Modeling](#data-modeling)
- [Data Analysis](#data-analysis)
- [Results / Findings](#results--findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [Future Improvements](#future-improvements)


---

## Project Overview

This HR analytics project was developed to analyze employee attrition, employee demographics, and employee performance using Power BI.

The goal of the project is to help HR teams monitor key employee KPIs, identify employee trends, and understand the major factors impacting attrition through interactive dashboards and data-driven insights.

The project follows dimensional modeling principles using the Kimball approach and includes data transformation, DAX calculations, and dashboard design.

---

## Data Sources

### HR Dataset
The dataset used in this project is a fictional HR dataset from Atlas Labs, designed to simulate real-world HR analytics scenarios. It contains employee-related information such as demographics, education levels, performance reviews, satisfaction metrics, and workforce details used to analyze employee attrition and employee trends.

### Dataset Files
- `EducationLevel.csv` – Employee education level information  
- `Employee.csv` – Core employee demographic and employee data  
- `PerformanceRating.csv` – Employee yearly performance review records  
- `RatingLevel.csv` – Performance rating categories and levels  
- `SatisfiedLevel.csv` – Employee satisfaction metrics and classifications  
### Tables Used
- FactPerformanceRating
- DimEmployee
- DimEducationLevel
- DimRatingLevel
- DimSatisfiedLevel
- DimDate

---

## Tools

- **Power BI** – Dashboard creation and reporting
- **Power Query** – Data cleaning and transformation
- **DAX** – KPI calculations and analytics
- **Dimensional Modeling** – Snowflake schema design

---

## Data Cleaning & Preparation

In the data preparation phase, the following steps were performed:

- Loaded CSV datasets into Power BI
- Checked and corrected data types
- Renamed tables and columns
- Structured datasets into fact and dimension tables
- Created relationships between tables
- Implemented active and inactive relationships

---

## Exploratory Data Analysis

EDA was performed to answer important HR business questions such as:

- What is the current employee attrition rate?
- Which department has the highest number of employees?
- What age groups dominate the workforce?
- How does salary vary across demographics?
- What factors may influence employee attrition?

---

## Data Modeling

The project follows the **Kimball modeling approach** using a **snowflake schema**.

### Model Structure
- 1 Fact Table
- 5 Dimension Tables

### Key Features
- Active & inactive relationships
- USERELATIONSHIP() implementation
- KPI-focused measures table

---

## Data Analysis

Created multiple DAX measures and calculations including:

```DAX
Total Employees = COUNT(DimEmployee[EmployeeID])

Attrition Rate % =
DIVIDE([Inactive Employees], [Total Employees])
```

### Advanced DAX Functions Used
- CALCULATE()
- USERELATIONSHIP()
- IF()
- MAX()
- DIVIDE()

### Dashboards Created
- HR Overview Dashboard
- Demographics Dashboard
- Performance Tracker Dashboard

---

## Results / Findings

The analysis revealed the following insights:

- Atlas Labs employed over **1,470+ employees**
- Approximately **1,200 employees are currently active**
- Employee attrition rate is **16%**
- Technology is the largest department
- Majority of employees are aged **20–29**
- Diversity and salary distribution trends were identified across demographics

---

## Recommendations

Based on the analysis, the following recommendations were identified:

- Improve employee retention strategies in high-attrition areas
- Monitor employee satisfaction and work-life balance metrics regularly
- Enhance diversity and inclusion initiatives
- Use performance tracking dashboards for employee review planning
- Focus HR efforts on departments with higher turnover trends

---

## Limitations

- Dataset is fictional and created for analytics practice purposes
- Some employee factors affecting attrition may not be represented in the dataset
- Analysis depends on available historical employee records only

---

## Future Improvements

Potential future enhancements include:

- Predictive attrition modeling
- Machine learning integration
- Employee retention forecasting
- Department drill-through analysis
- Real-time HR KPI monitoring

---
