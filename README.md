# PWC-Diversity-and-inclusion

## Table of Contents:
+ Problem statement
+ Data Source
+ Data Preparation
+ Data Visualization
+ Insights


## Problem Statement:
Define relevant KPIs in hiring, promotion, performance and turnover, and create a visualisation.

### Calculating the following measures could help to define proper KPIs:

+ of men
+ of women
+ of leavers
+ employees promoted (FY21)
+ of women promoted
+ of hires men
+ of hires women
+ turnover 
+ Average performance rating: men
+ Average Performance rating: women

## Data Source: [diversity and inclusion dataset](https://github.com/Ananya-Foujdar05/PWC-Diversity-and-inclusion/blob/main/03%20Diversity-Inclusion-Dataset.xlsx)


## Data Preparation:
+ Data transformation was done in power query and loaded into power bi desktop
+ Created some measures using DAX that are:
   - Total Employees = `COUNT('Pharma Group AG'[Employee ID])`
   - Men = `COUNTX(FILTER('Pharma Group AG' , 'Pharma Group AG'[Gender] = "Male") , 'Pharma Group AG'[Employee ID])`
   - Women = `COUNTX(FILTER('Pharma Group AG' , 'Pharma Group AG'[Gender] = "Female") , 'Pharma Group AG'[Employee ID])`
   - Leavers = `COUNTX(FILTER('Pharma Group AG' , 'Pharma Group AG'[FY20 leaver?] = "Yes") , 'Pharma Group AG'[Employee ID])`
   - Total Hiring = `COUNTX(FILTER('Pharma Group AG' , 'Pharma Group AG'[New hire FY20?] = "Y") , 'Pharma Group AG'[Employee ID])`
   - Total promotion = `COUNTX(FILTER('Pharma Group AG' , 'Pharma Group AG'[Promotion in FY21?] = "Yes") , 'Pharma Group AG'[Employee ID])`
   - Promotion in FY21 = `'Pharma Group AG'[Total promotion]/'Pharma Group AG'[Total Employees]`
   - Total Turnover = `COUNTX(FILTER('Pharma Group AG' , 'Pharma Group AG'[In base group for turnover FY20] = "Y") , 'Pharma Group AG'[Employee ID])`
   - Turnover in FY20 = `'Pharma Group AG'[Total Turnover]/'Pharma Group AG'[Total Employees]`
 

## Data Visualization:

![Diversity and inclusion](https://github.com/Ananya-Foujdar05/PWC-Diversity-and-inclusion/assets/140806083/cb01625a-2da4-46fe-a523-e7a339d8283e)

  
## Insights:
As we can conclude
+ Total employee are 500 in which 295 are men and 205 are women.
+ In FY20 new hires are 66 and leavers are 47.
+ There is  86% turnover in FY20 and avg. performance rating of men's and women's in FY20 are 2.41 and 2.42 respectively.
+ There is 10.20% promotion in FY21 in which 8.78% women are promoted.
+ 223 employees are from 20-29 age group which is the highest followed by 174 that are from 30-39 age group.
+ Number of employee working in operation department are highest followed by sales and marketing department.
+ Most employee working are from switzerland followed by europe.
