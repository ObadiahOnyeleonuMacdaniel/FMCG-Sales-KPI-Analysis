# FMCG-Sales-KPI-Analysis

### This repository contains an in-depth analysis of the FMCG sales team’s performance for February 2023. The analysis includes key performance indicators (KPIs) that provide insights into the achievements and effectiveness of each sales representative.

## PROBLEM STATEMENT
A table displaying the KPI achievements for all sales reps for February 2023, providing insights into the team's performance for the month.

Four files in the Excel CSV format containing all required data about the FMCG Sales Team were given.

These files were used to get all the insights regarding the performance of the team for the month of February 2023:

  (a) User Master;

  (b) Retailer Master;
  
  (c) Activities Report;
  
  (d) Sales Report

### Steps followed 

- Step 1 : Load and Read Dataset into Google colab (dataset is a csv file).
           
           Since am using Python for my Data Analysis, google colab or jupyter notebook are my favorite by default, while analyzing my dataset.
  
- Step 2 : Exploratory Data Analysis (EDA)
- Step 3 : Ensure consistent naming through FEATURE ENGINEERING and DATA CLEANING.
- Step 4 : Filter activities and sales data for February 2023
- Step 5 : Calculating for the Mandatory KPIs

  (a) Active Days

  (b) Retailer Universe, Coverage & Effective Coverage
  
  (c) Calls and Productive Calls
  
  (d) Sales metrics
  

## Calculating the percentages, the following expression were written;
       
        Calculate percentages for the KPI Summary Parameters 
        
        
                 kpi_summary['Coverage %'] = kpi_summary['Coverage'] / kpi_summary['Retailer Universe'] * 100
                 kpi_summary['Effective Coverage %'] = kpi_summary['Effective Coverage'] / kpi_summary['Retailer Universe'] * 100
                 kpi_summary['Productive Calls %'] = kpi_summary['Productive Calls'] / kpi_summary['Total Calls'] * 100
                 kpi_summary['Sales Value %'] = kpi_summary['Sales Actual (Value)'] / kpi_summary['Sales Target Value'] * 100
                 kpi_summary['Sales Volume %'] = kpi_summary['Sales Actual (Volume in Cartons)'] / kpi_summary['Sales Target Volume Cartons'] * 100
            


        
- Step 6 : Merge all KPIs into a Summary-KPI-Table
- Step 7 : Visualizing the KPI achievements. A card visual was used to represent count of customers.

  (a) Seat comfort
  
  (b) Departure & arrival time convenience

![Snap_1](https://user-images.githubusercontent.com/102996550/174089602-ab834a6b-62ce-4b62-8922-a1d241ec240e.jpg)

        
        Count of Customers = COUNT(airline_passenger_satisfaction[ID])
        



## INSIGHTS

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ## [4] SOME OTHER INSIGHTS
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
