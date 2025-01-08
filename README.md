
# SQL Queries for Housing Costs and Income Inequality Analysis

This document outlines key SQL queries designed to analyze the impact of housing costs on income inequality, track trends over time, and identify regions facing financial challenges.

---

## 1. Housing Cost Impact by Region
**Objective**: Calculate the average impact of housing costs (difference between BHC and AHC) by region. This helps identify regions where housing costs have the greatest effect on income inequality.

```sql
SELECT 
    geo AS region,
    AVG(CASE WHEN type = 'bhc' THEN income END) AS avg_bhc,
    AVG(CASE WHEN type = 'ahc' THEN income END) AS avg_ahc,
    ABS(AVG(CASE WHEN type = 'bhc' THEN income END) - AVG(CASE WHEN type = 'ahc' THEN income END)) AS abs_housing_cost_impact
FROM cleaned_data
GROUP BY geo
ORDER BY abs_housing_cost_impact DESC;
```

---

## 2. Trends in Income Inequality Over Time
**Objective**: Track how income inequality changes over time for both AHC and BHC, helping assess the long-term effectiveness of housing-related subsidies or policies.

```sql
SELECT 
    year,
    AVG(CASE WHEN type = 'bhc' THEN income END) AS avg_bhc,
    AVG(CASE WHEN type = 'ahc' THEN income END) AS avg_ahc
FROM cleaned_data
GROUP BY year
ORDER BY year ASC;
```

---

## 3. Regional Ranking by Income Inequality
**Objective**: Identify regions with the highest average income inequality (AHC) to pinpoint areas experiencing the most financial stress.

```sql
SELECT 
    geo AS region,
    AVG(CASE WHEN type = 'ahc' THEN income END) AS avg_income_inequality_ahc
FROM cleaned_data
GROUP BY geo
ORDER BY avg_income_inequality_ahc DESC;
```

---

## 4. Housing Cost Impact Percentage by Region
**Objective**: Compute the percentage difference between BHC and AHC to understand how housing costs affect income inequality relative to the baseline (BHC).

```sql
SELECT 
    geo AS region,
    (AVG(CASE WHEN type = 'bhc' THEN income END) - AVG(CASE WHEN type = 'ahc' THEN income END)) /
    AVG(CASE WHEN type = 'bhc' THEN income END) * 100 AS housing_cost_impact_percentage
FROM cleaned_data
GROUP BY geo
ORDER BY housing_cost_impact_percentage DESC;
```

---

## 5. Identify Regions with Rising Inequality
**Objective**: Detect regions where income inequality (AHC) is increasing over time, signaling potential financial challenges for households.

```sql
SELECT 
    geo AS region,
    year,
    AVG(CASE WHEN type = 'ahc' THEN income END) AS avg_income_inequality_ahc
FROM cleaned_data
GROUP BY geo, year
ORDER BY region, year ASC;
```
