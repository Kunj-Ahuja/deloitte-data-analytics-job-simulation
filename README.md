# Deloitte Data Analytics Job Simulation

## Overview

This repository contains my completed work from the **Deloitte Data Analytics Job Simulation** through **Forage**, completed in August 2026.

The simulation involved practical tasks covering **Data Analysis** and **Forensic Technology**.

The project consists of two analytical tasks:

1. **Daikibo Telemetry Downtime Analysis** — Tableau
2. **Gender Pay Equality Analysis** — Microsoft Excel

Together, these tasks demonstrate the application of data analysis, data visualization, classification, and business-focused problem-solving to realistic organizational scenarios.

---

# 📊 Task 1 — Daikibo Telemetry Downtime Analysis

## Overview

The first task involved analyzing telemetry data collected from machines across Daikibo Industrials' factories.

The objective was to use **Tableau** to identify patterns in machine downtime and create an interactive dashboard that allows factory-level performance to be compared with device-level downtime.

## Objective

The analysis focused on:

- Comparing downtime across Daikibo factories.
- Identifying the factory with the highest downtime.
- Analyzing downtime by device type.
- Creating an interactive factory filter.
- Allowing users to drill down from factory-level downtime to device-level downtime.

## Data Preparation

A calculated measure called `Unhealthy` was created in Tableau.

`IF [Status] = "unhealthy" THEN 10 ELSE 0 END`

Each unhealthy telemetry message was treated as representing **10 minutes of potential downtime**.

The resulting measure was then aggregated to calculate total potential downtime across factories and device types.

## Dashboard

The Tableau dashboard contains two visualizations:

### Down Time per Factory

| Factory | Potential Downtime |
|---|---:|
| daikibo-factory-seiko | 480 minutes |
| daikibo-shenzhen | 420 minutes |
| daikibo-factory-meiyo | 110 minutes |
| daikibo-berlin | 20 minutes |

### Down Time per Device Type

| Device Type | Potential Downtime |
|---|---:|
| LaserWelder | 480 minutes |
| LaserCutter | 430 minutes |
| HeavyDutyDrill | 70 minutes |
| Furnace | 20 minutes |
| SpotWelder | 10 minutes |
| ConveyorBelt | 10 minutes |
| CNC | 10 minutes |
| MetalPress | 0 minutes |
| AirWrench | 0 minutes |

## Key Insight

**daikibo-factory-seiko** recorded the highest potential downtime at **480 minutes**.

The dashboard was configured so that selecting a factory in the **Down Time per Factory** chart filters the **Down Time per Device Type** chart.

This provides an interactive drill-down from factory performance to the equipment contributing to downtime.

## Tools Used

- Tableau
- JSON telemetry data
- Calculated fields
- Bar charts
- Interactive dashboard filters
- Data visualization
- Operational analytics

---

# ⚖️ Task 2 — Gender Pay Equality Analysis

## Overview

The second task focused on investigating potential gender inequality in employee compensation across Daikibo Industrials.

The Forensic Technology team had processed employee compensation data and generated an **Equality Score** for different job roles across company locations.

The objective was to classify the Equality Scores into meaningful categories using **Microsoft Excel**.

## Objective

The provided Equality Table contained:

- Factory
- Job Role
- Equality Score

A fourth column called **Equality class** was added to classify each Equality Score.

The Equality Score ranges from **-100 to +100**, with **0 representing ideal equality**.

## Equality Classification

| Equality Score | Equality Class |
|---|---|
| -10 to +10 | Fair |
| -20 to -11 / +11 to +20 | Unfair |
| Below -20 / Above +20 | Highly Discriminative |

### Examples

| Equality Score | Equality Class |
|---:|---|
| 10 | Fair |
| -9 | Fair |
| 15 | Unfair |
| -20 | Unfair |
| 20 | Unfair |
| -30 | Highly Discriminative |
| 30 | Highly Discriminative |

## Excel Implementation

The classification was implemented using an Excel `IF` formula:

`=IF(ABS(C2)<=10,"Fair",IF(ABS(C2)<=20,"Unfair","Highly Discriminative"))`

The formula evaluates the absolute value of the Equality Score and assigns the appropriate Equality Class.

The formula was then applied across the complete dataset.

## Analysis Process

1. Opened the provided Equality Table in Microsoft Excel.
2. Reviewed the Factory, Job Role, and Equality Score fields.
3. Added a fourth column named **Equality class**.
4. Applied conditional logic to classify each Equality Score.
5. Filled the classification formula across the complete dataset.
6. Saved the completed Excel spreadsheet.

## Business Context

The classification converts numerical equality scores into easily interpretable categories.

This can help organizations:

- Identify potentially unequal compensation patterns.
- Highlight job roles or locations requiring further investigation.
- Prioritize areas that may warrant additional forensic analysis.
- Communicate compensation equality findings more effectively.

The classification is an analytical indicator and does not, by itself, establish the cause of a pay disparity or prove discrimination. Further investigation would be required to understand the underlying factors.

## Tools Used

- Microsoft Excel
- IF functions
- Conditional logic
- Data classification
- Spreadsheet analysis
- Forensic technology

---

# 🔍 Key Takeaways

The simulation provided experience applying data analytics to two different business problems.

### Operational Analytics

The telemetry analysis demonstrated how machine data can be transformed into an interactive Tableau dashboard to identify factories and equipment associated with potential downtime.

The analysis identified **daikibo-factory-seiko** as the factory with the highest potential downtime at **480 minutes**, while **LaserWelder** was the largest contributor to overall device-level downtime at **480 minutes**.

### Forensic Analytics

The gender pay equality analysis demonstrated how compensation equality scores can be classified into meaningful categories to highlight areas requiring further investigation.

Together, the tasks provided practical experience in transforming structured data into insights that can support business decision-making and investigation.

---

# 🛠️ Skills Demonstrated

### Data Analysis

- Data preparation
- Data interpretation
- Data classification
- Business-focused analysis
- Operational analytics

### Data Visualization

- Tableau
- Bar charts
- Interactive dashboards
- Dashboard filtering
- Drill-down analysis

### Microsoft Excel

- IF functions
- Conditional logic
- Data classification
- Spreadsheet analysis

### Business & Forensic Analytics

- Manufacturing telemetry analysis
- Downtime analysis
- Compensation equality analysis
- Forensic data interpretation
- Business insight generation

---

# 📁 Repository Structure

    deloitte-data-analytics-job-simulation/
    │
    ├── README.md
    │
    ├── task-1-telemetry-analysis/
    │   ├── README.md
    │   ├── dashboard-overview
    │   ├── dashboard-seiko-filtered
    │   └── daikibo-telemetry-analysis.twbx
    │
    └── task-2-gender-pay-equality/
        ├── README.md
        └── Equality-Table-Completed.xlsx

---

# 🎯 Project Context

This project was completed as part of the **Deloitte Data Analytics Job Simulation** through **Forage**.

The simulation provided practical experience working with real-world business scenarios involving **Data Analysis** and **Forensic Technology**.

The two tasks demonstrate the ability to apply analytical techniques across different business contexts, from manufacturing operations and machine downtime to employee compensation and gender pay equality.

---

# 👤 Author

**Kunj Ahuja**

B.Com (Hons.) — University of Delhi

Interested in:

- Data Analytics
- Business Intelligence
- Data Visualization
- Business & Digital Analytics
