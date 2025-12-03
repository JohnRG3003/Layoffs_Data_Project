# Global Layoffs Data Analysis (SQL)

## 📌 Project Overview
This project involves an end-to-end analysis of global workforce reduction trends in the technology sector (2020-2023). The goal was to clean a raw dataset of 2,300+ companies and perform Exploratory Data Analysis (EDA) to identify how economic conditions impacted different industries, funding stages, and geographic regions.

## 📂 File Structure
* `Data_Cleaning_Project.sql`: The script used to standardize data, remove duplicates using window functions, and handle null values.
* `Exploratory_Data_Analysis_Project.sql`: The script used for deriving insights, calculating rolling totals, and generating rankings.
* `layoffs.csv`: The raw dataset used for this analysis.

## 🛠️ Key SQL Techniques Used
* **Data Cleaning:** `ROW_NUMBER()` for de-duplication, `SELF JOINS` for populating missing data, `Standardization` of text strings.
* **Aggregations:** Grouping data by Industry, Year, and Company Stage.
* **Window Functions:** `SUM() OVER(ORDER BY date)` for Rolling Totals.
* **Ranking:** `DENSE_RANK()` to identify top companies with the most layoffs per year.
* **CTEs:** Used to structure complex queries for modular analysis.

## 📊 Key Insights & Findings
1.  **Hardest Hit Industries:** The **Consumer** and **Retail** sectors faced the highest volume of layoffs, significantly outpacing other traditional tech sectors.
2.  **Seasonal Trends:** Analysis of rolling totals revealed a sharp spike in layoffs beginning in **Q4 2022**, continuing through Q1 2023.
3.  **Stage Vulnerability:** **Post-IPO** companies accounted for the majority of workforce reductions compared to early-stage (Series A/B) startups.
4.  **Geographic Impact:** While the US had the highest volume, significant layoff clusters were identified in **India** and the **Netherlands**.

## 💻 How to Use
1.  Download the `layoffs.csv` file.
2.  Import into MySQL Workbench.
3.  Run the cleaning script first to create the staging table.
4.  Run the EDA script to generate the insights.
