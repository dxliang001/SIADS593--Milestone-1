# Housing Affordability Analysis  
*SIADS 593 – Milestone 1 (University of Michigan Master of Applied Data Science)*
##Team members 
Please list your team members (2-3 max).

Sahana Sundar (sahanasu)
Dongxin Liang (dxliang)
Naiwen Duan (nduan) 


## 1  Project Overview
With inflation and mortgage rates rising, it’s increasingly challenging for prospective homeowners to purchase a home. We will investigate how housing affordability has evolved over time. 

By using geospatial housing-cost data from Zillow and Redfin, we can analyze how affordability has evolved over time, and what role interest rates and inflation play in driving those trends.



## 2 Questions to Answer: 
1. How has the average price of a home changed from 2016-2020? 
2. How does home price vary across counties in the United States? 
3. How do year-over-year Consumer Price Index changes and mortgage rate movements correlate with county-level cost burden shifts?
Cost burden: % of income spent on housing
4. Does inflation or interest rate changes tend to lead or lag changes in affordability?
5. Are certain age or household groups shifting away from traditional homeownership due to affordability?


## 3  Data Sources (all public)
| Data set | Time span | Purpose |
|----------|-----------|---------|
| **American Community Survey (ACS) 5-year – CHAS tables**<br>*(Comprehensive Housing Affordability Strategy)* | 2016 - 2020 • County level | Counts and HUD-calculated percentages of cost-burdened households, broken out by income band and by tenure |
| **ACS 5-year – Socio-Economic tables** | 2016 - 2020 • County level | Median household income, poverty metrics, employment context  |
| **Redfin County Market Tracker** | 2016-2020 • County level |  The Redfin Data Center provides publicly accessible information on the housing market. We will use a dataset that shows home prices listed on the Redfin website by county.   |
| **Freddie Mac Primary Mortgage Market Survey – 30-Year Fixed Rate** | 2016-2020 • Monthly | Captures financing-cost pressure on owner households |
| **Bureau of Labor Statistics Consumer Price Index, all urban consumers (CPI-U)** | 2016-2020 • Monthly | Used later to inflation-adjust incomes to real 2020 dollars |


## 4  Reproducing the Results
```bash
# 1. clone the repository
git clone https://github.com/dxliang001/SIADS593--Milestone-1.git
cd SIADS593--Milestone-1

# 2. launch JupyterLab
jupyter lab
```

## 5 Analysis

Analysis 1: Find the distributions of housing cost burden (% of income spending on mortgage/rent), income, home values, and rent across counties. We expect to learn if there are specific geographic concentrations where housing is more/less affordable. 

Analysis 2: Calculate pearson correlation coefficients between housing cost burden and each variable in the ACS data (ex: employment status, education level) and visualize the results using a heatmap. We expect to learn which variables are most correlated with having a high housing cost burden.

Analysis 3: At the national level (for all of the US), see if there’s any correlation between annual CPI and mortgage rate changes and housing cost burden (% of income spending on mortgage/rent) to detect whether changes in inflation or mortgage rates tend to precede or lag shifts in housing affordability. We expect to learn if changes in home prices can be attributed to inflation alone, or if there are other factors at play. 
Analysis 4: We want to learn whether certain demographic and socioeconomic groups (e.g., renters, young families, low-income households) are disproportionately experiencing housing cost burdens compared to others. To do this, we will:
Calculate cost-burden indicators (e.g., % of income spent on housing) using ACS and HUD CHAS data, segmented by household income brackets, age groups, tenure status, and household structure.
Compare the level and severity of cost burden (e.g., moderately burdened vs. severely burdened) across these groups.
We want to answer whether household type or economic status significantly affects vulnerability to affordability pressures, and whether the burden is increasing faster among specific groups over time. 

## 6 Visualizations 

Choropleth Map:
We will plot the average home price by state or county, with a drop down for the user to filter on a year and month between January 2016 and December 2020. 

Line Plot: 
We will plot the annual inflation rate change and the year over year change in the housing cost burden from 2016 to 2020 to understand how these two trends relate to each other.

Heatmap: 
We will plot the Pearson correlation coefficient between cost-burden and each predictor variable (income, poverty, unemployment, inflation, mortgage rate).

Grouped Bar Chart: 
We will plot the % of households that are cost-burdened (spending 30% or more of their income on housing) for various income levels to show how housing affordability has shifted over time. 


