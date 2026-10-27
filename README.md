# Healthcare-Operations-Billing-Analysis---Excel-EDA

#### Author: Dike Chinonso

## Project Overview

This project explores healthcare operations and billing patterns using a synthetic healthcare dataset from Kaggle. I used Excel to examine admission volumes, billing amounts, length of stay, patient demographics, insurance providers, hospitals, and physician encounter counts.

The aim was to identify patterns in the data, compare groups, and highlight areas that could be investigated further.

## Business Problem

Healthcare organisations need to understand how patient volumes and billing patterns vary across different groups. This analysis explores questions such as:

- How do admission volumes change over time?
- Does average billing vary across medical conditions, admission types, or insurance providers?
- How does billing per day relate to length of stay?
- Which age groups account for the largest share of encounters?
- Are there noticeable differences in average billing across selected hospitals?
- What can encounter counts tell us about physician workload?

## Dataset

- **Source:** [Healthcare Dataset on Kaggle](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)
- **Records:** 54,966 encounters
- **Date coverage:** May 2019 to May 2024
- **Data type:** Synthetic healthcare data

The dataset includes patient demographics, medical conditions, admission and discharge dates, admission types, hospitals, insurance providers, billing amounts, test results, and physician names.

The records represent encounters and should not be interpreted as 54,966 unique patients.

## Tools Used

- MySQL: Initial data cleaning and data-quality checks.
- Microsoft Excel: Exploratory data analysis, calculated columns, PivotTables, charts, and dashboard development.

## Methodology

### 1. Data Cleaning and Preparation

The dataset was cleaned using MySQL before being imported into Excel for analysis. Negative billing amounts were also identified and flagged during the SQL data-quality checks.

The Excel analysis therefore started with the prepared dataset rather than repeating the initial cleaning process. The negative billing values were documented as a data-quality limitation because their meaning could not be verified.

### 2. Calculated Columns

I added calculated columns in Excel to support the analysis:

- **Year:** Extracted from the relevant date field to examine admission volumes over time.
- **Age Group:** Grouped ages into 0–17, 18–34, 35–49, 50–65, and over 65.
- **Length of Stay Group:** Categorised encounters into short (1–3 days), moderate (4–7 days), long (8–15 days), and extended (over 15 days) stays.
- **Billing Per Day:** Calculated by dividing each encounter's billing amount by its length of stay.
- **Insurance Category:** Grouped insurance providers into private and government-backed categories for comparison.

These columns made it easier to summarise and compare the data across relevant groups.

### 3. Exploratory Data Analysis

I used Excel PivotTables to summarise encounter counts and average billing amounts across different categories. The analysis covered trends over time, admission types, medical conditions, insurance providers, age groups, hospitals, and physician encounter counts.

I also compared average and median daily billing across length-of-stay groups to check whether the observed pattern was also present in the median values.

### 4. Visualisation and Dashboard

I used charts to present the main comparisons and developed a dashboard to bring key metrics and findings together. The dashboard includes summary indicators and visual comparisons of admission volumes, billing patterns, patient demographics, and selected hospital results.

Slicers were used to allow interactive filtering of the dashboard.

## Scope of Analysis

The analysis covered:

- Overall encounter volume and key billing indicators.
- Admission volumes by year and admission type.
- Average billing by medical condition, admission type, and insurance provider.
- Private versus government-backed insurance comparisons.
- Average and median daily billing across length-of-stay groups.
- Patient age and gender distributions.
- Billing patterns across age groups.
- Encounter volumes and average billing for selected hospitals.
- Encounter counts for physicians with the highest recorded volumes.
- Distribution of clinical test results.

## Key Findings

- The dataset contains 54,966 encounters, with an average billing amount of $25,544.31 and an average length of stay of 15.5 days.
- Average total billing was similar across the four length-of-stay groups, while average daily billing decreased as length of stay increased.
- Average billing varied only slightly across medical conditions, admission types, and insurance providers.
- Medicare's average billing was close to that of the private insurance group, although Medicare was the only government-backed provider represented.
- Patients over 65 formed the largest age group, accounting for 30.8% of encounters.
- Admission volumes were relatively stable from 2021 to 2023. The 2019 and 2024 totals cover partial years and are not directly comparable with the full-year totals.
- Average billing differed across the selected hospitals, but the small number of encounters in each hospital's comparison limits interpretation.

These are descriptive findings from the available dataset and do not establish the causes of the observed patterns.

## Limitations

- The dataset is synthetic and may not reflect real hospital operations or billing.
- The records represent encounters rather than necessarily unique patients.
- The dataset contains negative billing amounts whose meaning could not be verified.
- The 2019 and 2024 figures cover partial years.
- Some comparisons, including those for children and selected hospitals, are based on relatively small numbers of encounters.
- Medicare was the only government-backed insurance provider represented, limiting the private-versus-government comparison.
- The analysis is descriptive and does not establish causation or statistical significance.
- Billing per day is derived from billing amount and length of stay, so its relationship with length of stay must be interpreted with this calculation in mind.

## Project Files

- Excel workbook: Contains the prepared data, calculated columns, PivotTables, charts, and dashboard.
- Project Insights: Provides a fuller discussion of the findings, their interpretation, and the limitations of the analysis.
