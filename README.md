# LITA-CLASS-DOCUMENTATION-PROFIT-ANALYSIS

## Project Overview
The project analyzes the profit of International Breweries in differerent counntries.

## Data Sources
---
The dataset was sourced from the Sales Records of International Breweries. The dataset includes information about the following:
- Sales ID
- Sales Rep
- Emails
- Brands
- Plant Cost
- Unit Price
- Quantity
- Cost
- Profit
- Countries
- Region
- Month
- Years

  

## Data Tools Used
---
- Microsoft Excel [Download Here](https://wwww.microsoft.com)
  1. For Data Cleaning
  2. For Analysis
  3. For Visualization- Pivot tables, PieChart and Cloumn chart were used to visually represent key insights
- Structured Query Language(SQL) for Quering of Data

## Data Cleaning and Preparations
---
In the initial phase of the Data Cleaning and preparations,the following actions were performed;
1. Data loading and Inspection
2. Handling missing variables
3. Data Cleaning and formating

## Exploratory Data Analysis
---
EDA invoved the exploring of Data to answer some questions about the Data which are as follows;
- Calculate the Total Profits
- Calculate the Total Profit for senegal
- Calculate the Total Profit for Nigeria in 2019
- Calculate the Total Profit for Nigeria in 2017
- Calculate the Total Profit for Nigeria
- Calculate the Total Profit for Hero brands
  
### SQL Query Used
- **Calculate the Total Profits**
```SQL
select sum(profit) as TotalProfit from International_Breweries
```
![Screenshot (226)](https://github.com/user-attachments/assets/668b969e-bd8c-4cf3-bac3-0b8ee349eebc)

- **Calculate the Total Profit for senegal**
```SQL
select sum(profit) as TotalProfit from International_Breweries
where countries = 'Senegal'
```
![Screenshot (227)](https://github.com/user-attachments/assets/f6ce974b-02d1-4977-86e0-f3fcd7659662)

- **Calculate the Total Profit for Nigeria in 2019**
```SQL
select sum(profit) as TotalProfit from International_Breweries
where countries = 'Nigeria' and YEARs = '2019'
```
![Screenshot (228)](https://github.com/user-attachments/assets/31cebb4e-7144-46a1-9fbc-b7485c63764f)

- **Calculate the Total Profit for Nigeria in 2017**
```SQL
select Brands, sum(profit) as TotalProfit 
from International_Breweries
where countries = 'Nigeria' and years = '2017'
Group by Brands
order by 2 desc
```
![Screenshot (229)](https://github.com/user-attachments/assets/31535ec9-dd9d-472b-9da8-4aa0a0392bbe)

- **Calculate the Total Profit for Nigeria**
```SQL
select Brands, sum(profit) as TotalProfit 
from International_Breweries
where countries = 'Nigeria' 
Group by Brands
order by 2 desc
```
![Screenshot (230)](https://github.com/user-attachments/assets/0938c991-a47b-488b-8b15-8b0ba113672c)

- **Calculate the Total Profit for Hero brands**
```SQL
select  sum(profit) as TotalProfitHero from International_Breweries
where countries = 'Nigeria' and years = '2017' and brands ='Hero'
--Group by Brands
--order by 2 desc
```
![Screenshot (231)](https://github.com/user-attachments/assets/7016eb5e-794c-4e34-ab09-f974b96b82d0)

- **Categorize the 5 countries into their language**
```SQL
SELECT countries,
      CASE
	     WHEN COUNTRIES IN ('Nigeria', 'Ghana') then 'Anglophone'
		 Else 'Francophone'
End as CountriesGroup,
sum(Profit) as TotalProfit from international_breweries
where years in ('2017', '2018', '2019')
Group by Countries
order by 3 desc
```
![Screenshot (232)](https://github.com/user-attachments/assets/f6d76697-0b37-4001-a550-92a10e15e4e2)

## Data Visualization
### Pivot Table
![Screenshot (224)](https://github.com/user-attachments/assets/30ebf30d-9f92-411c-9b6b-543d0c45249c)

### Filtered Column Chart for Year 2017
![Screenshot (221)](https://github.com/user-attachments/assets/189d3d1c-825c-40bf-a502-45355ae5f34a)

### Filtered Column Chart for Year 2018
![Screenshot (222)](https://github.com/user-attachments/assets/3d3b3614-ba0a-413e-b923-dd96323ee525)

### Filtered Column Chart for Year 2019
![Screenshot (223)](https://github.com/user-attachments/assets/bb0c7024-5932-45d5-b408-741350115da9)

### 1. Overall Profit Overview
- Profits generated decreased in 2018 and 2019 as compaired to 2017 as seen in the Column Charts above.
  

