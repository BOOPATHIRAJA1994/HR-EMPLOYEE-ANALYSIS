# 🛍️ Mini Project:  HR-EMPLOYEE-ANALYSIS

---

## 📘 Project Overview
This project focuses on the **HR EMPLOYEE ANALYSIS** using **Microsoft Excel** and **Power BI**.  
The main objective is to **transform, model, and visualize** the raw data to derive **actionable business insigh**, identify **Employees work status**, and measure **performance of employees**.

---

## 📂 Source Datasets
The analysis is based on **four core datasets**:

| File Name | Description |
|------------|--------------|
| `employee_data.csv.` | Contains Employee details |
| `employee_engagement_survey_data.csv` | Includes Employees engagement score,satisfaction score |
| `recruitment_data.csv` | includes applicants full details |
| `training_and_development_data.csv` | Provides training data,training abserving level and training outcome details  |
---

## ⚙️ Tools & Technologies Used
- **Microsoft Excel** – Data preparation and initial exploration  
- **Power BI** – Data transformation, modeling, and interactive dashboard creation  
- **DAX (Data Analysis Expressions)** – For calculated columns and business measures  

---

## 🔄 Phase 1 – Data Transformation & Data Modeling

### **Data Import & Cleaning**
1. Imported all three CSV files into Power BI.  
2. Limited the *employee_data.csv* table to the **first 3000 rows** for optimized analysis.  
3. Changed data types appropriately:  
   - *first name,last name → full name*  
   - *dd-mm-yyyy → yyyy-mm-dd*  
4. Formatted *Employee id & Termination Description* into **Proper Case** for consistency.  
5.Limited the *recruitment_data.csv* table to Merged *City* and *State* columns to create a new **Country** column in the format `City, State`.  
6. Added a **AGE(YEARS)** column using the formula:  
AGE(YEARS) ==DATEDIF(E2,TODAY(),"Y")

markdown
Copy code
7. Added a **Year of Work** column using the formula:  
Year of Work = DATEDIF(C2, D2, "Y") & " Years, " & DATEDIF(C2, D2, "YM") & " Months"
8. Merged *employee_engagement_survey_data.csvr* and *employee_data.csv.* into a unified table **EMPLOYEE ID** using *EMPLOYEE ID*.  
9. Identified and handled **missing values** and **duplicate rows**.  
10. **Grouped & Aggregated Metrics**:
 - Average SATISFIED WORK EMPLOYEE by Category   

### **Relationships Established**
- *employee_engagement_survey_data.csv* ↔ *employee_data.csv* ↔ *raining_and_development_data.csv* → via **EMPLOYEE ID** 

---

## 🧮 Phase 2 – DAX & Data Visualization

### **Calculated Measures**
| Measure | Formula / Description |
|----------|----------------------|
| **total employees** | `COUNTROWS(employee_data))` |
| **total applicants** | `COUNT(recruitment_data[Applicant ID])` |
| **male** | `CALCULATE([total employees],employee_data[Gender]="male")")` |
| **female** | `CALCULATE([total employees],employee_data[Gender]="female")` |

---

## 📊 Data Visualizations & Dashboards
Interactive dashboards were designed in Power BI to visualize sales and performance trends.

| Visualization | Description |
|----------------|-------------|
| **Clustered BAR Chart** | DEPARTMENT BASED EMPLOYEES SERVICE YEAR |
| **Donut Chart** | TERMINATED EMPLOYEE DETAILS |
| **Line Chart** | EMPLOYEE ENGAGEMENT SATISFACTION  |
| **Scatter Chart** | Department-wise Placement |
| **Cards** | Employee status & EDUCATION LEVEL |
| **GAUGE** | Satisfaction Rating & Engagement Score |
| **Map Visual** | Geographic Sales Analysis by City |
| **Treemap** | Desired Salary Status |
| **KPI** | Divisions of Employee Units |
---

## 🧠 Key Insights
- Employee performance varied across product categories, with some exceeding targets consistently.  
- **Satisfaction Rating & Engagement Score** revealed strong performance in specific sub-categories.  
- The **“Geographic Sales Analysis by City”** field enabled regional analysis to identify top-performing cities and states.  
- **Divisions of Employee Units** were captured through monthly analysis using line charts.  
- **Divisions of Employee Units** and **Department-wise Placement** helped evaluate both national and regional performance.  

---

## 🪄 Summary
This project demonstrates a complete **end-to-end data analytics workflow**, covering:
- Data transformation  
- Data modeling  
- DAX calculations  
- Visual reporting using Power BI  

The analysis provided clear insights into **Employee performance**, **profitability**, and **regional variations**, enhancing business decision-making through interactive dashboards.

---

## ✅ Conclusion
The **HR EMPLOYEE ANALYSIS Project** showcases the combined power of **Power BI** and **Excel** for practical business analytics.  
By integrating clean data models, calculated measures, and visual storytelling, this project helps:
- Track EMPLOYEE TRAININGS vs performance  
- Identify high-performing segments  
- Enable data-driven decision-making  

---

## 👩‍💻 Author
**Project Title:** Mini Project – HR EMPLOYEE ANALYSIS  
**Author:** S.BHOOPATHIRAJA                                         
**Tools:** Excel | Power BI | DAX  
**Year:** 2025  
