# Deloitte Data Analytics Job Simulation

![Deloitte](https://img.shields.io/badge/Deloitte-Data%20Analytics-black)
![Tableau](https://img.shields.io/badge/Tableau-Visualization-blue)
![Excel](https://img.shields.io/badge/Excel-Data%20Analysis-green)
![Forage](https://img.shields.io/badge/Forage-Job%20Simulation-orange)

## 📌 Overview

This repository contains my completed work from the **Deloitte Data Analytics Job Simulation**, completed through **Forage** in August 2026.

The simulation involved practical tasks covering:

- Data analysis
- Data visualization
- Tableau dashboard development
- Operational analytics
- Forensic technology
- Gender pay equality analysis

The project consisted of two major analytical tasks, each demonstrating a different application of data analysis in a business context.

---

# 📊 Task 1 — Daikibo Telemetry Downtime Analysis

## Objective

Analyze Daikibo Industrials' machine telemetry data to identify patterns in machine downtime across factories and device types.

The objective was to build an interactive Tableau dashboard that allows users to:

1. Compare downtime across factories.
2. Identify the factory with the highest downtime.
3. Analyze downtime by device type.
4. Drill down from factory-level performance to device-level performance.

## Tools Used

- Tableau
- JSON telemetry data
- Calculated fields
- Interactive dashboards

## Data Preparation

A calculated measure called `Unhealthy` was created.

```text
IF [Status] = "unhealthy" THEN 10 ELSE 0 END
