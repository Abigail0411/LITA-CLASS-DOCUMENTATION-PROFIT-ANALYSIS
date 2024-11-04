# LITA-CLASS-DOCUMENTATION-PROFIT-ANALYSIS
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
