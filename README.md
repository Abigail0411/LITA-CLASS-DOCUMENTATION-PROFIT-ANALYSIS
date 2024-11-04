# LITA-CLASS-DOCUMENTATION-PROFIT-ANALYSIS

### Data Sources
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

  

### Tools Used
---
- Microsoft Excel [Download Here](https://wwww.microsoft.com)
  1. For Data Cleaning
  2. For Analysis
  3. For Visualization- Pivot tables, PieChart and Cloumn chart were used to visually represent key insights
- Structured Query Language(SQL) for Quering of Data

### Data Cleaning and Preparations
---
In the initial phase of the Data Cleaning and preparations,the following actions were performed;
1. Data loading and Inspection
2. Handling missing variables
3. Data Cleaning and formating

### Exploratory Data Analysis
---
EDA invoved the exploring of Data to answer some questions about the Data which are as follows;
- Calculate the Total Profits
- Calculate the Total Profit for senegal
- Calculate the Total Profit for Nigeria in 2019
- Calculate the Total Profit for Nigeria in 2017
- Calculate the Total Profit for Nigeria

---to get total profit----
select sum(profit) as TotalProfit from International_Breweries
---to get totalprofit for senegal------
select sum(profit) as TotalProfit from International_Breweries
where countries = 'Senegal'
--to get total for Nigeria in 2019---
select sum(profit) as TotalProfit from International_Breweries
where countries = 'Nigeria' and YEARs = '2019'
----
select Brands, sum(profit) as TotalProfit 
from International_Breweries
where countries = 'Nigeria' and years = '2017'
Group by Brands
order by 2 desc

select Brands, sum(profit) as TotalProfit 
from International_Breweries
where countries = 'Nigeria' 
Group by Brands
order by 2 desc


----to get totalprofit for Hero brands-----
select  sum(profit) as TotalProfitHero from International_Breweries
where countries = 'Nigeria' and years = '2017' and brands ='Hero'
--Group by Brands
--order by 2 desc
Categorise the 5 countries into their language
SELECT countries,
      CASE
	     WHEN COUNTRIES IN ('Nigeria', 'Ghana') then 'Anglophone'
		 Else 'Francophone'
End as CountriesGroup,
sum(Profit) as TotalProfit from international_breweries
where years in ('2017', '2018', '2019')
Group by Countries
order by 3 desc
s
