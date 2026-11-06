<div align="center">

# -- ! Accenture India HR Analytics Dashboard ! --
### *Interactive Power BI Report for Workforce, Attrition, Compensation & Performance Insights*

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures%20%26%20Time%20Intelligence-4B0082?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-ETL%20from%20CSV-0078D4?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![Data Model](https://img.shields.io/badge/Data%20Model-Star%20Schema-9C27B0?style=for-the-badge&logo=databricks&logoColor=white)](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)


## Video Link-https://drive.google.com/file/d/1E7TiOqRlQmrFm0NxOIyv2__MGWHo-IFd/view?usp=sharing
<br/>

> *"Data tells you what happened — a good dashboard tells you what to do next."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🧱 Part A — Data Model & DAX](#-part-a--data-model--dax)
- [📊 Part B — Dashboard Pages](#-part-b--dashboard-pages)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Accenture India HR Analytics Dashboard** is a multi-page, interactive **Power BI** report that turns a large HR dataset (**50,000 employees**, **500,000 recruitment candidates**, 12 Indian cities and 15 departments) into clear, decision-ready insights. It demonstrates core business-intelligence concepts such as **star-schema data modeling**, **DAX measures**, **time-intelligence (vs Previous Year) comparisons**, **cross-page slicers** and **executive-style visual storytelling**.

This project is designed to:
- Build a clean **star-schema data model** from raw CSV files using Power Query
- Practice writing **DAX measures** for KPIs, YoY comparisons and dynamic text labels
- Design a consistent, branded **1920 × 1080 dashboard** with navigation, slicers and insight panels
- Give HR leaders one place to track **headcount, attrition, pay, performance, promotions and training**

---

## 🎯 Problem Statement

> **Objective:** Build an interactive HR analytics dashboard that helps leadership understand workforce health and act on attrition, compensation and performance trends.

You are building a reporting solution for an HR analytics team. The report must let users slice the workforce by **Year, City, Department, Job Level and Gender**, and answer questions such as *"Where are we losing people?"*, *"Are salaries competitive and fair?"* and *"Who are our high performers?"*

| 📂 Dashboard Page | 📄 Type | 🔍 Description |
|-------------------|---------|----------------|
| Workforce Overview | Descriptive | Headcount, new hires, gender mix, tenure and location spread |
| Attrition & Retention | Diagnostic | Attrition rate/count, retention, risk by department and city |
| Compensation Analytics | Analytical | Payroll, average/median/highest salary, pay by level and gender |
| Performance & Promotion | Analytical | Ratings, high performers, promotion rate, training completion |
| Executive Summary | Strategic | One-page view of the most important KPIs and risk signals |

The goal is to demonstrate **end-to-end Power BI skills** — from raw data to a polished, interactive executive report.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📑 **5 Report Pages** | Workforce Overview, Attrition & Retention, Compensation, Performance & Promotion, Executive Summary |
| 🧭 **Page Navigator** | Built-in navigation plus action buttons for smooth movement between pages |
| 🎛️ **5 Global Slicers** | Year, City, Department, Job Level and Gender filter every page |
| 📐 **Star Schema Model** | 5 dimension tables and 6 fact tables connected through ID keys |
| 🧮 **60+ DAX Measures** | KPIs, previous-year comparisons, growth %, ratios and dynamic labels |
| ▲▼ **Dynamic PY Labels** | Text measures like `vs PY: 16.0% ▼ 0.5 pp` update with the filter context |
| 🗺️ **Map Visuals** | City-level bubbles for headcount, attrition and average salary |
| 💡 **Key Insight Panels** | Narrative text boxes beside the charts summarising what the data says |
| 🎨 **Consistent Branding** | Purple Accenture-style theme on the Fluent 2 base theme, with custom icons |
| 🖥️ **Fit-to-Page Layout** | All pages designed at 1920 × 1080 for presentation-ready viewing |

---

## 🏗️ Project Structure

```
📦 accenture-hr-analytics/
│
├── 📄 accenture_Project.pbix    ← Power BI report (model + 5 report pages)
│
├── 📁 DATASET/                  ← Source CSV files loaded through Power Query
│   ├── DimDate.csv
│   ├── DimDepartment.csv
│   ├── DimEmployee.csv
│   ├── DimJobLevel.csv
│   ├── DimLocation.csv
│   ├── FactAttrition.csv
│   ├── FactCompensation.csv
│   ├── FactPerformance.csv
│   ├── FactRecruitment.csv
│   ├── FactTraining.csv
│   └── FactWorkforce.csv
│
└── 📄 README.md                 ← Project documentation
```

> ℹ️ The `.pbix` file points to a local `DATASET` folder. After downloading, update the file path in **Transform data → Data source settings**.

---

## 🔄 Project Workflow

```
Raw CSV Files (11 tables)
          │
          ▼
┌─────────────────────────────┐
│   Power Query (ETL)         │  ← Promote headers, set data types
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Data Model (Star Schema)  │  ← Relationships on Employee, Dept,
│                             │    Location, Job Level & Date keys
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   DAX Measures              │  ← KPIs, PY comparisons, dynamic text
└────────────┬────────────────┘
             │
     ┌───────┴────────┐
     ▼                ▼
┌─────────────┐   ┌──────────────────┐
│  Visuals    │   │ Slicers + Page   │
│  & Insights │   │ Navigation       │
└──────┬──────┘   └────────┬─────────┘
       │                   │
       ▼                   ▼
┌─────────────────────────────┐
│   5-Page Interactive Report │
└────────────┬────────────────┘
             │
             ▼
   Share / Publish to Power BI Service ✅
```

---

## 🧱 Part A — Data Model & DAX

### 📝 1. What is the Data Model?

The model follows a **star schema**: descriptive **dimension** tables (who, where, what level, when) sit around transactional **fact** tables (salary, attrition, performance, hiring, training). Slicers on a dimension filter every connected fact table.

---

### 🗺️ 2. Tables — Overview

| Table | Type | Key Columns | Rows (approx.) |
|-------|------|-------------|----------------|
| 🗓️ **DimDate** | Dimension | DateKey, Date, Year, Quarter, Month | 1,461 (2022–2025) |
| 🏢 **DimDepartment** | Dimension | DepartmentID, DepartmentName | 15 |
| 👤 **DimEmployee** | Dimension | EmployeeID, EmployeeName, Gender, DepartmentID, LocationID, JobLevelID | 50,000 |
| 🪜 **DimJobLevel** | Dimension | JobLevelID, JobLevel | 10 |
| 📍 **DimLocation** | Dimension | LocationID, City | 12 |
| 🚪 **FactAttrition** | Fact | EmployeeID, DepartmentID, LocationID, JobLevelID, AttritionReason | 8,000 |
| 💰 **FactCompensation** | Fact | EmployeeID, BaseSalary, Bonus, VariablePay | 50,000 |
| ⭐ **FactPerformance** | Fact | EmployeeID, PerformanceRating, PromotedFlag, HighPerformerFlag | 50,000 |
| 🧲 **FactRecruitment** | Fact | CandidateID, DateKey, DepartmentID, LocationID, Source, Stage | 500,000 |
| 🎓 **FactTraining** | Fact | EmployeeID, CourseCategory, CompletedFlag | 50,000 |
| 🧑‍💼 **FactWorkforce** | Fact | EmployeeID, CurrentSalary, TenureYears, YearsExperience, IsActive | 50,000 |

---

### 🔗 3. Relationships

```
                       DimDate
                          ▲
                          │ DateKey
                          │
DimDepartment ◄── FactRecruitment ──► DimLocation
      ▲                                    ▲
      │ DepartmentID                       │ LocationID
      │                                    │
      ├────────────── DimEmployee ─────────┤
      │              ▲   ▲   ▲   ▲         │
      │              │   │   │   │         │
DimJobLevel ─────────┘   │   │   └── FactWorkforce
 (JobLevelID)            │   └────── FactTraining
                         └────────── FactPerformance / FactCompensation

FactAttrition ──► DimDepartment, DimLocation, DimJobLevel
FactAttrition ──► DimEmployee   (inactive relationship)
```

---

### 🧮 4. Core DAX Measures

> Measures live in the `DimDate` table so they are easy to find and reuse.

**Headcount & Attrition**
```dax
Total Employees = DISTINCTCOUNT(DimEmployee[EmployeeID])

Attrition Count = DISTINCTCOUNT(FactAttrition[EmployeeID])

Attrition Rate  = DIVIDE([Attrition Count], DISTINCTCOUNT(DimEmployee[EmployeeID]))

Retention Rate  = 1 - [Attrition Rate]
```

**Compensation (values shown in LPA / Crore)**
```dax
Average Salary LPA =
DIVIDE(
    CALCULATE(AVERAGE(FactWorkforce[CurrentSalary]), FactWorkforce[IsActive] = 1),
    100000
)

Total Payroll Cr =
DIVIDE(
    CALCULATE(SUM(FactWorkforce[CurrentSalary]), FactWorkforce[IsActive] = 1),
    10000000
)
```

**Performance & Learning**
```dax
Promotion Rate =
DIVIDE(
    CALCULATE(DISTINCTCOUNT(FactPerformance[EmployeeID]), FactPerformance[PromotedFlag] = 1),
    DISTINCTCOUNT(FactPerformance[EmployeeID])
)

Training Completion % = DIVIDE(SUM(FactTraining[CompletedFlag]), COUNTROWS(FactTraining))
```

**Time Intelligence — Previous Year Comparison**
```dax
Attrition Rate PY =
CALCULATE([Attrition Rate], SAMEPERIODLASTYEAR(DimDate[Date]))

Line Attrition Rate =
VAR _cur = [Attrition Rate]
VAR _py  = [Attrition Rate PY]
VAR _d   = (_cur - _py) * 100
RETURN
IF(ISBLANK(_py), "vs PY: –",
   "vs PY: " & FORMAT(_py, "0.0%") & "   " &
   IF(_d >= 0, "▲ ", "▼ ") & FORMAT(ABS(_d), "0.0") & " pp")
```

**Key Concepts Used:**

| Concept | Detail |
|---------|--------|
| 🔁 `CALCULATE()` | Changes filter context (e.g., active employees only) |
| 🗓️ `SAMEPERIODLASTYEAR()` | Previous-year comparison for every KPI |
| ➗ `DIVIDE()` | Safe division that avoids divide-by-zero errors |
| 🧾 `VAR … RETURN` | Readable, reusable intermediate calculations |
| 🔤 `FORMAT()` | Builds dynamic "vs PY ▲▼" labels shown on KPI cards |

---

## 📊 Part B — Dashboard Pages

### 🗺️ 5. Pages — Overview

| # | Page | Main Visuals | Key Measures |
|---|------|--------------|--------------|
| 1️⃣ | **Workforce Overview** | KPI cards, department column chart, gender donut, new-hires line chart, city map, detail table | Total Employees, Active Employees, Average Tenure, Gender Ratio, New Hires |
| 2️⃣ | **Attrition & Retention** | KPI cards, attrition trend line, department bar, gender donut, recruitment-stage column chart, risk treemap, city map, table | Attrition Count/Rate, Retention Rate, High Risk Employees |
| 3️⃣ | **Compensation Analytics** | KPI cards, salary-by-level column chart, department bar, salary-band histogram, experience vs salary scatter, gender donut, city map, matrix | Average / Median / Highest Salary LPA, Total Payroll Cr |
| 4️⃣ | **Performance & Promotion** | KPI cards, rating distribution, promotion by department, training-completion donut, city map, matrix | Promotion Rate, High Performers, Avg Rating, Training Completion % |
| 5️⃣ | **Executive Summary** | KPI cards, headcount map, hiring funnel, payroll treemap, attrition-vs-salary scatter, summary table | Total Employees, Attrition Rate, Avg Salary, Promotion Rate |

---

### 👥 6. Workforce Overview

> Answers: *How big is the workforce and where is it located?*

- Headcount card with **vs-PY growth %**
- Active employees, average tenure and **Male : Female** ratio cards
- Employee count by department and by city (map)
- Monthly **New Hires** trend

### 🖼️ 1.Workforce Overview 

<img src="Assets/Screenshot 2026-11-06 085004.png">



---


---

### 🚪 7. Attrition & Retention

> Answers: *Who is leaving, where, and why does it matter?*

- Attrition rate, attrition count and retention rate with PY comparison
- Attrition by department, gender and city
- Treemap sized by headcount and coloured by attrition rate to surface **high-risk** departments
- Recruitment-stage view (Applied → Interviewed → Offered → Joined → Retained)

---

### 🖼️ 2.Attrition & Retention

<img src="Assets/Screenshot 2026-11-06 085207.png">


### 💰 8. Compensation Analytics

> Answers: *Is pay competitive, consistent and fair?*

- Total payroll (in ₹ Crore), average / median / highest salary (in LPA)
- Average salary by **job level**, **department** and **city**
- **Salary-band histogram** and **experience vs salary vs rating** scatter plot
- Gender pay comparison

---

### 🖼️ 3.Compensation Analytics
<img src="Assets/Screenshot 2026-11-06 085223.png">

### ⭐ 9. Performance & Promotion

> Answers: *Who performs well, who gets promoted, and is learning working?*

- Average rating (out of 5), high performers and promotion rate
- Rating distribution by department with promotion flags
- Training completion donut across the workforce

---

### 🖼️ 4.Performance & Promotion
<img src="Assets/Screenshot 2026-11-06 085253.png">

### 🧭 10. Executive Summary

> Answers: *What should leadership look at first?*

- Five headline KPIs: **Total Employees, Average Salary, Attrition Rate, Promotion Rate, High Performers**
- Department scatter of **attrition rate vs average salary**
- Payroll treemap, hiring funnel and a department-level summary table

---

### 🖼️ 5.Executive Summary

<img src="Assets/Screenshot 2026-11-06 085307.png">


## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 📊 **Power BI Desktop** | Latest | Report authoring and visualisation |
| 🧮 **DAX** | Built-in | Measures, KPIs and time intelligence |
| 🔧 **Power Query (M)** | Built-in | Loading CSV files and setting data types |
| 🗃️ **CSV Files** | — | Source data for dimensions and facts |
| 🎨 **Fluent 2 Theme** | CY26SU10 | Base theme, customised with a purple palette |
| 🖼️ **PNG Icons** | — | Custom KPI and navigation icons inside the report |

---

## 📈 Results & Insights

After exploring the dashboard (data as on **30 Apr 2025**), the following insights are produced:

- 👥 **Large Workforce** — **50,000 employees** across **12 cities** and **15 departments**, with **~61% male / ~39% female** split
- 📍 **Balanced Locations** — Bengaluru and Hyderabad lead headcount, but all 12 cities hold a similar share (~4,200 each)
- 🚪 **Attrition** — **8,000 employees (16%)** have left, giving an **84% retention rate**
- 🔎 **Attrition Reasons Are Evenly Spread** — Better Salary, Relocation, Career Growth, Personal Reasons and Work-Life Balance each account for roughly 19–20%
- 💰 **Compensation** — Average salary is about **₹31.5 LPA** with a median close to **₹31.4 LPA**, and the highest salary near **₹60 LPA**
- ⚖️ **Pay Parity** — Male and female average salaries are almost identical (~31.5 vs ~31.4 LPA)
- ⭐ **Performance** — Average rating is about **3.6 / 5**, indicating a generally strong workforce
- 🎓 **Learning** — Training completion is around **92%** of enrolled courses
- 🧲 **Hiring Funnel** — Candidates move through *Applied → Interviewed → Offered → Joined → Retained*, showing where talent drops off

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Portfolio Ready** | Covers modeling, DAX, visual design and storytelling in one project |
| 🔄 **Reusability** | Measures follow a repeatable *Value → PY → Growth → Label* pattern |
| 📚 **Educational** | Shows how star schema, relationships and filter context work together |
| 🧭 **Easy Navigation** | Page navigator and action buttons guide users across pages |
| 🎛️ **Fully Interactive** | Every slicer cross-filters visuals; maps and charts drill into detail |
| 📏 **Scalable** | Handles 500K+ recruitment rows and 50K employees smoothly |
| 🧪 **Extensible** | Easy to add new pages (Diversity, Learning, Forecasting) or measures |
| 🛡️ **Safe Calculations** | `DIVIDE()` and blank checks prevent errors in KPI labels |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Krinal Dholakiya

[![GitHub](https://img.shields.io/badge/GitHub-krinaldholakiya-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/krinaldholakiya)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/krinaldholakiya/)

> *"Every dashboard starts with a question — and the best ones answer it at a glance."*

**🎓 Role:** Data Analyst | Power BI Enthusiast \
**📍 Location:** India\
**🛠️ Skills:** Power BI · DAX · Power Query · Data Modeling · Dashboard Design

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📚 [Microsoft Power BI Docs](https://learn.microsoft.com/en-us/power-bi/) — Official Power BI reference
- 🧮 [DAX Guide](https://dax.guide/) — Complete DAX function reference
- 🔧 [Power Query M Docs](https://learn.microsoft.com/en-us/powerquery-m/) — M language reference
- ⭐ [Star Schema Guidance](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema) — Data modeling best practices
- 📖 [SQLBI](https://www.sqlbi.com/) — In-depth DAX and modeling articles
- 💬 [Power BI Community](https://community.fabric.microsoft.com/) — Problem-solving support
- 🎨 [Flaticon](https://www.flaticon.com/) — Icon inspiration

---

<div align="center">

---

*Made with ❤️ — Last updated: 6 November, 2026*

</div>
