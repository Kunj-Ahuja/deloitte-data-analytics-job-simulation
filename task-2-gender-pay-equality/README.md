# Task 2 — Gender Pay Equality Analysis

## Overview

As part of the **Deloitte Data Analytics Job Simulation**, this task focused on investigating potential gender inequality in employee compensation across Daikibo Industrials.

The Forensic Technology team had processed employee compensation data and generated an **Equality Score** for different job roles across company locations.

The objective was to classify these Equality Scores into three categories to make potential areas of pay inequality easier to identify and investigate.

## Objective

The provided **Equality Table** contained three columns:

- **Factory**
- **Job Role**
- **Equality Score**

The task was to create a fourth column named **Equality class**.

The Equality Score is an integer ranging from **-100 to +100**, where **0 represents ideal gender pay equality**.

The scores were classified into:

- **Fair**
- **Unfair**
- **Highly Discriminative**

## Equality Classification

The Equality Score was classified according to its distance from the ideal score of `0`.

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

```excel
=IF(ABS(C2)<=10,"Fair",IF(ABS(C2)<=20,"Unfair","Highly Discriminative"))
