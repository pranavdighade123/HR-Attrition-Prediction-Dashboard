# 📈 HR Attrition Analytics & Predictive Dashboard

## Project Overview
This is a full-stack data science project focused on predicting and understanding employee turnover to drive targeted retention strategies. The solution integrates Python for modeling with Power BI for interactive visualization, providing a clear, actionable two-page dashboard for HR and leadership.

---

## 🚀 Technical Stack

| Category | Tool / Library | Purpose |
| :--- | :--- | :--- |
| **Data Engineering** | Python (Pandas), Power Query (M) | Cleaning, Feature Engineering, Data Type Enforcement |
| **Predictive Modeling** | Scikit-learn (Random Forest) | Feature Importance Analysis |
| **Business Intelligence** | Power BI, DAX | Visualization, KPI Monitoring, Aggregated Metrics |

---

## 🔍 Key Findings & Business Impact

The overall attrition rate was measured at approximately **47.05%**. The predictive model revealed that attrition is highly correlated with controllable factors related to compensation and workload.

### Top 5 Predictive Drivers (Corrected for Data Leakage)
The following features account for the vast majority of the model's predictive power. This data drives the intervention strategy on the dashboard's second page.

| Driver | Importance Score | Business Recommendation |
| :--- | :--- | :--- |
| **Monthly\_Income** | **35%** | **Targeted Compensation Review:** Focus on raising salaries for employees in low-income quartiles, particularly those in high-attrition job roles. |
| **Overtime\_Num** | **25%** | **Mandatory Overtime Control:** Implement strict policies to track and limit recurring overtime to mitigate burnout risk. |
| **Job\_Satisfaction\_Score** | **18%** | **Engagement & Wellness Programs:** Investigate and improve work environment factors contributing to low satisfaction scores. |
| **Years\_at\_Company** | **12%** | **High-Risk Tenure Intervention:** Introduce mentorship or career path planning at specific tenure milestones (e.g., the 1-3 year mark). |
| **Work\_Life\_Balance\_Score** | **10%** | **Flexible Work Options:** Review remote work policies and workload distribution to support a better balance. |

---

## 🛠️ Project Methodology

### 1. Data Engineering and Modeling
* **Data Preparation:** Consolidated raw data (`hr_analytics_project.csv`) and engineered features such as `Attrition_Num` (target) and `Overtime_Num`.
* **Feature Transformation:** Created ordinal scores (`_Score` columns) for qualitative metrics like Work-Life Balance and Job Satisfaction.
* **Modeling Correction:** Successfully identified and mitigated **Data Leakage** by excluding the target variable from the feature set, ensuring the final feature importance scores were statistically valid.

### 2. Power BI & Visualization
* **DAX Aggregation:** Created the **`Job_Role_Metrics`** table to pre-calculate `Attrition_Rate`, `Total_Employees`, and `Avg_Monthly_Income` by Job Role, improving dashboard performance.
* **Error Resolution:** Addressed common Power BI display errors (e.g., $100\%$ display) by correctly setting the visual property **Show value as: No calculation** on all rate measures.

---

## 📈 Dashboard Screenshots

### Page 1: HR KPI & Attrition Trends
* **Focus:** Overall performance and job role risk assessment.


### Page 2: Predictive Drivers & Intervention Strategy
* **Focus:** Visualizing the root causes based on the Random Forest model.


---

