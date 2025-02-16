# Cafe Sales Analysis

## Project Overview

This project focuses on cleaning, analyzing, and extracting valuable insights from café sales data to better understand customer behavior, product demand, and sales trends. The dataset contains transactional data, including product sales, payment methods, locations, and dates, which are processed and analyzed using Microsoft Excel.

The primary goal of this project is to transform raw sales data into a structured and insightful dataset that helps in making data-driven business decisions. This involves identifying missing values, correcting inconsistencies, standardizing formats, and creating interactive visualizations that allow stakeholders to easily interpret the data. Information about the dataset used can be seen [here](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)

## Objectives

- Clean and standardize the dataset by handling missing values, correcting inconsistencies, and formatting dates.
- Analyze sales performance by identifying top-selling products, preferred payment methods, and sales trends.
- Develop an interactive dashboard to visualize key insights and support data-driven decisions.

## Data Cleaning Process

1. Eliminated duplicate records to maintain data integrity and avoid skewed analysis.
2. Handle Missing Values (Quantity, Price Per Unit, Total Spent) by removing rows where at least two of these three columns were missing since the total cost could not be calculated.
3. Fill Missing Values in Sales Data:
    - Filled missing Quantity using **Quantity**: $\text{Quantity} = \frac{\text{Total Spent}}{\text{Price Per Unit}}$
    - Filled missing Price Per Unit using $$ Total Spent / Quantity $$
    - Filled missing Total Spent using $$ Quantity \times Price Per Unit $$
4. Matched missing Item values based on existing Price Per Unit data.
5. Used RANDBETWEEN in Payment Method clumn to assign a random value (Cash, Credit Card, or Digital Wallet) in a 1:1:1 ratio due to no significant distribution difference.
6. Used RANDBETWEEN in Location column to assign a random value (In-store or Takeaway) in a 1:1 ratio.
7. Dropped rows where Transaction Date was missing since it was a critical timestamp.
8. Extracted the month from Transaction Date to support time-based analysis in the dashboard.

## Data Visualization

## Conclusion
