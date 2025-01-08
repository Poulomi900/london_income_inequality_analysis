# Objective of the Project

The primary objective of this project is to build an end-to-end data pipeline on AWS to analyze income inequality trends in the UK. The analysis focuses on understanding the impact of housing costs on disposable income and identifying regional disparities in income distribution. By leveraging AWS services such as S3, Glue, and Athena, this project demonstrates the process of ingesting, transforming, and analyzing data efficiently, with insights that can support financial institutions and policymakers.

## Key Goals
#### 1. Analyze Income Inequality:
  Use the 90:10 income ratio, which compares the income of the top 10% of households (90th percentile) to the bottom 10% (10th percentile), to measure income inequality.
  Examine how inequality varies across regions (London, UK Overall, Rest of the UK) and over time.

#### 2. Assess Housing Costs Impact:
 Compare income levels Before Housing Costs (BHC) and After Housing Costs (AHC).
 Calculate the reduction in disposable income due to housing costs and identify regions where housing affordability is a significant challenge.

#### 3. Provide Actionable Insights:

Derive insights on regional disparities in income inequality to help financial institutions design policies and products targeting areas with high inequality or housing cost burdens.
Identify trends that could guide affordable housing investments or policy interventions.

## Derived Insights
#### 1.Housing cost impact by region:
- London has the highest housing cost impact, with an absolute difference of 4.48, indicating significant financial stress from housing expenses.
- Rest of UK has the least impact, with a housing cost impact of 1.15, reflecting better housing affordability.
- Financial institutions should prioritize affordable housing initiatives in London to mitigate the high housing cost burden.

#### 2.Trends in Income Inequality Over Time:
- AHC is consistently higher than BHC, indicating significant post-housing disposable income due to subsidies or benefits.
- Both BHC and AHC gradually increased from 2008/09 to 2018/19, peaking in 2018/19-2020/21.
- AHC declined after 2018/19, dropping to 6.33 in 2020/21-2022/23, suggesting rising housing costs or reduced subsidies impacting disposable income.

#### 3. Regional Ranking by Income Inequality (AHC):
- London has the highest income inequality (AHC) with an average of 9.81, significantly higher than other regions.
- UK overall has moderate inequality (5.47), while the Rest of UK has the lowest inequality (5.07).
- The stark disparity suggests that London faces severe income inequality challenges compared to the rest of the UK, warranting targeted financial and policy interventions.

#### 4. Housing Cost Impact Percentage by Region:
- London has the highest housing cost impact, with a significant reduction of -83.98% in disposable income due to housing costs.
- The UK overall shows a housing cost impact of -33.90%, while the Rest of UK has the lowest impact at -29.22%, indicating better housing affordability outside London.
- The stark difference in London highlights the severe burden of housing costs, making it a critical focus area for affordable housing policies and financial support programs.

#### 5. Trends in Regional Income Inequality Over Time (AHC):
- London shows the highest income inequality over time, peaking at 11.0 in 2018/19-2020/21 before declining to 9.0 in 2020/21-2022/23.
- The Rest of UK maintains consistently low inequality, hovering around 5.1 for most years, with a slight decrease to 4.8 in 2020/21-2022/23.
- UK overall remains steady, averaging 5.5 across years, indicating minimal variation in national inequality trends outside of London.
