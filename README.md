# Team-7-MIST-4610-Group-Project-2

## Team Name: 
Sp26_71552_Group 7

## Team Members:
1. Nandini Chinthapanti [@nandinichr](https://github.com/nandinichr)
2. Sara Gebreyohannes [@saragebree](https://github.com/saragebree)
3. Rajan Malik [@RKMalik-1](https://github.com/RKMalik-1)
4. Landon Tabor [@lptabor63](https://github.com/lptabor63)
5. Reina Wang [@rlwang0314](https://github.com/rlwang0314)

## Component 1: Dataset and Questions
**The dataset we selected and why:**

We selected the COVID-19 Epidemiological Dataset because it contains detailed information like confirmed cases and geographic breakdowns, allowing for analysis across countries. It also has time-series data and variables that can be aggregated and compared in different ways, making it possible to answer more complex questions. 

**A brief description: number of tables, approximate row counts, key columns and data types, and which columns are relevent:**
We used four tables. 

1. The SCS_BE_DETAILED_PROVINCE_CASE_COUNTS table has approximately 236.6K rows. The columns used from this table are REGION (varchar), SEX (varchar), and NEW_CASES (number). 
2. The SCS_BE_DETAILED_MORTALITY table has approximately 11.4K rows. The column used from this table is DEATHS (number).
3. The SCS_BE_DETAILED_TESTS table has approximately 13.9K rows. The columns used from this table are TESTS (number).
4. The SCS_BE_DETAILED_HOSPITALISATIONS table has approximately 12.6K rows. The columns used from this table is TOTAL_IN_ICU (number). 

**What makes the data non-trivial and why is it interesting/meaningful?**

This dataset is non-trivial because both questions asked in this project combine multiple variables, perform calculations, and interpret patterns across different dimensions like region, gender, and time. For question 1, identifying which Belgian regions had the highest COVID-19 death rates requires comparing deaths to confirmed cases instead of using raw values. It also includes grouping the data by region and gender to compare mortality risk between males and females. This adds complexity because you can not just find the answer in the columns of data but requires aggregation and comparison across multiple categories. 

This analysis is meaningful because it shows insights into how COVID-19 impacts different populations and healthcare systems. For example, differences in death rates between males and females across regions show potential demographic disparities. These findings are important because they show how data can reveal differences in risk across populations and evaluate how effectively a country manages healthcare during a crisis. 


**Questions** 

Q1: Which Belgian regions had the highest COVID-19 death rate relative to confirmed cases, and did mortality risk differ between males and females? 

Q2: As testing volume increased over time, did Belgium's ICU burden improve — suggesting better pandemic control? 



## Component 2: Snowsight Dashboard 



## Component 3: Streamlit in Snowflake App 
