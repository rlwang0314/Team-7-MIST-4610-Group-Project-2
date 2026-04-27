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
We used four tables. The data from all four of these tables were provided by Star Schema and sourced from Sciensano.

1. The SCS_BE_DETAILED_PROVINCE_CASE_COUNTS table has approximately 236.6K rows. The columns used from this table are REGION (varchar), SEX (varchar), and NEW_CASES (number). 
2. The SCS_BE_DETAILED_MORTALITY table has approximately 11.4K rows. The column used from this table is DEATHS (number). 
3. The SCS_BE_DETAILED_TESTS table has approximately 13.9K rows. The column used from this table is TESTS (number). 
4. The SCS_BE_DETAILED_HOSPITALISATIONS table has approximately 12.6K rows. The column used from this table is TOTAL_IN_ICU (number). 

**What makes the data non-trivial and why is it interesting/meaningful?**

This dataset is non-trivial because both questions asked in this project combine multiple variables, perform calculations, and interpret patterns across different dimensions like region, gender, and time. For question 1, identifying which Belgian regions had the highest COVID-19 death rates requires comparing deaths to confirmed cases instead of using raw values. It also includes grouping the data by region and gender to compare mortality risk between males and females. This adds complexity because you can not just find the answer in the columns of data but requires aggregation and comparison across multiple categories. 

This analysis is meaningful because it shows insights into how COVID-19 impacts different populations and healthcare systems. For example, differences in death rates between males and females across regions show potential demographic disparities. These findings are important because they show how data can reveal differences in risk across populations and evaluate how effectively a country manages healthcare during a crisis. 


**Questions** 

Q1: Which Belgian regions had the highest COVID-19 death rate relative to confirmed cases, and did mortality risk differ between males and females? 

Question 1 is meaningful because it can help identify which regions should have more targeted public health messaging. Economically, regions with higher death rates also experience workforce loss and reduced productivity. Differences in mortality rates based on gender can affect labor markets, especially in areas dominated by one gender. This question can also help determine which regions need more medical resources and support decisions such as lockdowns and hospital expansion. 

Q2: As testing volume increased over time, did Belgium's ICU burden improve — suggesting better pandemic control? 

Question 2 is meaningful because it can indicate if the country is getting ahead of the virus (more testing means earlier detection and less severe cases). Economically, if there are fewer severe cases, there would be less disruption in the workforce, reducing the need for strict lockdowns and thus improving economic stability. This can also help provide insight on if the healthcare system is being overwhelmed. 


## Component 2: Snowsight Dashboard 

<img width="1546" height="835" alt="image" src="https://github.com/user-attachments/assets/c5adef7d-aa6a-433b-b97a-1aeb6a5ada48" />


**Question 1:**

<img width="692" height="461" alt="image" src="https://github.com/user-attachments/assets/465ad12b-4b07-4da7-a5c1-4c849726350d" />


<img width="969" height="212" alt="image" src="https://github.com/user-attachments/assets/17e4d0de-82c8-47b7-ba87-d00398b16b68" />


**What does this show and what does it mean?**

The bar chart compares COVID-19 death rates across three Belgian regions: Wallonia, Flanders, and Brussels. 

Wallonia has the highest COVID-19 death rate relative to confirmed cases, followed by Flanders, while Brussels has the lowest. In all three regions, males consistently show slightly higher death rates than females. This suggests both regional differences in outcomes and a gender gap in COVID-19 mortality risk.


**Question 2:**

<img width="695" height="477" alt="image" src="https://github.com/user-attachments/assets/da4538a6-1a4b-459b-8d38-0bf71fca0e4a" />

<img width="835" height="263" alt="image" src="https://github.com/user-attachments/assets/e28e08d9-23f2-4303-83f4-ac33b24f2d80" />

**What does this show and what does it mean?**

This chart shows the relationship between COVID-19 testing volume and new cases in Belgium over time. It shows how the pandemic evolved in the region. 

As testing increased over time, new cases still spiked during major waves, showing that more testing did not necessarily prevent surges. However, testing consistently outnumbered new cases, especially in later waves, suggesting Belgium was able to track the virus more effectively over time. This means that while testing improved visibility into the spread, it was not enough on its own to control it.

<img width="735" height="514" alt="image" src="https://github.com/user-attachments/assets/34cf1739-374f-4bf1-887b-766e530c0083" />

<img width="792" height="206" alt="image" src="https://github.com/user-attachments/assets/22678cc6-c363-4cf2-89ab-399198b8cdd5" />


**What does this show and what does it mean?**

This chart shows how overwhelmed the healthcare system was over time during COVID-19 in Belgium. It indicated how severe the pandemic was at certain times. 

ICU occupancy actually peaked higher in February 2021 than it did in the first wave of March 2020, meaning that even as testing expanded, the healthcare system was still being heavily strained. After that second wave though, ICU peaks dropped progressively with each subsequent wave, suggesting Belgium got better at managing severe cases over time. This partially answers our question, ICU burden did improve in the long run, but testing volume alone was likely not the main reason, as other factors like vaccination probably played a bigger role. 


## Component 3: Streamlit in Snowflake App 

Reproduction of Visualization Using AI 
<img width="1602" height="878" alt="image" src="https://github.com/user-attachments/assets/b1562219-c9f1-438a-b1e2-455a3ae0c066" />


The interactive elements are shown on the left side. The date range filter lets users select a specific time period for the data. This lets users analyze trends within specific phases of the pandemic, instead of looking at one big timeline. For example, users would be able to isolate peaks and declines in cases and ICU usage. When users only see the full timeline, they may miss how relationships change over time. 

The region filter (Brussels, Flanders, Wallonia) lets users select specific regions from the death-rate analysis. By adding this featuer, users would be able to compare regions directly (ex. Brussels vs. Flanders without Wallonia creating noise). Without the region filter, the chart makes users look at a full-country comparison and doesn't allow for focused regional insights. 


The sex filter (Male/Female/Both) lets users isolate mortality data by gender. This directly supports our research question about gender differences in mortality risk. Users can compare male vs. female death rates and see whether differencces are consistent across regions. 

All of these features combined provide analytical value by allowing users to explore the  data across time, geography, and demographics, rather than seeing only a fixed aggregate summary. 

**AI Use:** 

AI was used to improve the graphs and to add the interactive featuers. The code given by Streamlit was pasted into AI and asked what improvements it would make as well as what interactive features should be added to provide increased analytical insight. The suggestions were reviewed by the group and we decided which features should be added and what improvements we should let the AI make. 
