# FMCG SALES (Fast Moving Cosumers Goods) KPI ANALYSIS

This repository contains an in-depth analysis of an FMCG (Fast Moving Cosumers Goods) sales team’s performance for February 2023. 

The analysis includes key performance indicators (KPIs) that provide insights into the achievements and effectiveness of each sales representative.

## PROBLEM STATEMENT
We seek to generate a table displaying the KPI achievements for all sales reps for February 2023, providing insights into the team's performance for the month.

Four files in the Excel CSV format containing all required data about the FMCG Sales Team were given.

  (a) User Master;

  (b) Retailer Master;
  
  (c) Activities Report;
  
  (d) Sales Report

These files were used to get all the insights regarding the performance of the team for the month of February 2023:

### Steps followed 

- Step 1 : Load and Read Dataset into Google colab (dataset is a csv file).
           
               Since am using Python for my Data Analysis, google colab or jupyter notebook are my favorite by default while analyzing my dataset.

- Step 2 : Exploratory Data Analysis (EDA)
- Step 3 : DATA CLEANING and also Ensuring consistent naming through FEATURE ENGINEERING.
- Step 4 : Filter activities and sales data for February 2023 only.

     ![actv](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/0a270594-5fa6-44fd-95e1-b8a5cc4480dc)     

 ![sfb](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/dbadfeee-58e9-44ab-8d70-4306cb9d8438)
- Step 5 : Calculating for the Mandatory KPIs

  (a) Active Days

  (b) Retailer Universe, Coverage & Effective Coverage
  
  (c) Calls and Productive Calls
  
  (d) Sales metrics
       
- Step 6 : Merge all KPIs into a Summary-KPI-Table
- Step 7 : Visualizing the KPI achievements. A boxplot was used



## CALCULATING THE MANDATORY KPIs 
- Loading the dataset    
          
               #Load and Read Dataset
               user_master = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/EURO ATLANTIS ANALYSIS/User Master.csv')
               retailer_master = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/EURO ATLANTIS ANALYSIS/Retailer Master.csv')
               activities_report = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/EURO ATLANTIS ANALYSIS/Activities Report.csv', parse_dates=['Visit Date'])
               sales_report = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/EURO ATLANTIS ANALYSIS/Sales Report.csv')


- Filtering activities and sales data for February 2023


- Checking the unique number of features in the sales_feb dataframe

- Get the number of unique values for each column

- Checking the unique number of features in the sales_feb dataframe

- Checking the unique number of features in the sales_feb dataframe

- Checking the unique number of features in the sales_feb dataframe


- ## Calculating for the Mandatory KPIs
  ### (a) Active Days
  - Target Work Days: Number of days sales reps are expected to work in a month, where a working week is Monday – Saturday
  - Work Days: Actual number of work days worked (Visible in the activities report).
  
           
           Top-10 Sales_rep with the highest Active days
  ![activedayszz](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/2e26ffb4-f20a-4d04-9802-b0cf31cc7cb1)      

 ### (b) Retailer Universe, Coverage & Effective Coverage.

   KPIs to show the relationship between the unique number of retailers each sales rep is expected to have, cover and sell into.
- Retailer Count Target

          
           Top-10 Sales_rep with the highest retailer_universe
  ![retatt](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/58b22adc-0653-46c2-88ba-66f16ee054d1)      

- Retailer Count
- Retailer Universe %
- Covered Retailers: Unique count of retailers visited in the month by each sales rep (Visible in the activities report for each sales rep).

            Top-10 Sales_rep with the highest Coverage
  ![covr](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/8abd9919-661a-47d8-842c-00b710450679)
- Coverage % (Against Retailer Count)
- Productive Retailers: Unique count of retailers sold to in the month by each sales rep (Visible in the sales report for each sales rep).
- Productive Coverage % (Against Retailer Count)
- Productive Coverage % (Against Covered Retailers)
- Effective Coverage
  
              Top-10 Sales_rep with the highest Effective Coverage
  ![ecb](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/16f6384c-8340-4e4f-bba7-a4b308b16984)


  
 ### (c) Calls and Productive Calls
  KPIs to show the number of expected retailer visits (calls), actual visits and productive visits.
Calls Target: Target number of unique retailers to be visited on each work day by each sales rep multiplied by the target work days in a month for each sales rep.
Calls Actual: Total number of unique retailers visited on each work day in a month for each sales rep (Visible in the activities report for each sales rep).
Calls %


           Top-10 Sales_rep with the highest total calls
  ![bb](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/d3f7c12b-2827-40c8-a9e2-d9ac9d1744ff)
  
Productive Calls: Total number of unique retailers sold to on each work day in a month for each sales rep (Visible in the sales report for each sales rep).

Productive Calls % (Against Calls Target)

Productive Calls % (Against Calls Target)

           Top-10 Sales_rep with the highest Productive Calls
  ![spc](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/7b422359-9f00-448c-be06-8ffb1ef3369b)


 ### (d) Sales metrics
Sales Target (Value)

Sales Actual (Value)

Sales Target (Volume in Cartons)

Sales Actual (Volume in Cartons)

Sales Value %

Sales Volume %


### Calculating the percentages, the following expression were written;
       
        Calculate percentages for the KPI Summary Parameters 
        
        
                 kpi_summary['Coverage %'] = kpi_summary['Coverage'] / kpi_summary['Retailer Universe'] * 100
                 kpi_summary['Effective Coverage %'] = kpi_summary['Effective Coverage'] / kpi_summary['Retailer Universe'] * 100
                 kpi_summary['Productive Calls %'] = kpi_summary['Productive Calls'] / kpi_summary['Total Calls'] * 100
                 kpi_summary['Sales Value %'] = kpi_summary['Sales Actual (Value)'] / kpi_summary['Sales Target Value'] * 100
                 kpi_summary['Sales Volume %'] = kpi_summary['Sales Actual (Volume in Cartons)'] / kpi_summary['Sales Target Volume Cartons'] * 100
            

## DATA ANALYSIS & VISUALIZATION REQUIREMENTS
A table showing the KPI achievements for all sales rep for the month.

A table showing the summary of all KPI achievements by ASM & ZSM for the month.

A presentation telling a story about all KPI achievements by the team for the month of February as well as additional insights that can be drawn from the data.

![spx](https://github.com/ObadiahOnyeleonuMacdaniel/FMCG-Sales-KPI-Analysis/assets/156518788/075d70e0-da2c-4725-a140-3b69fcdaf112)


## INSIGHTS


