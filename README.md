# Housing Affordability Analysis  
*SIADS 593 – Milestone 1 (University of Michigan Master of Applied Data Science)*


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
| **American Community Survey (ACS) 5-year – CHAS tables**<br>*(Comprehensive Housing Affordability Strategy)* | 2016 & 2020 • County level | Counts and HUD-calculated percentages of cost-burdened households, broken out by income band and by tenure |
| **ACS 5-year – Socio-Economic tables** | 2016 & 2020 • County level | Median household income, poverty metrics, employment context (to be integrated in Milestone 2) |
| **Freddie Mac Primary Mortgage Market Survey – 30-Year Fixed Rate** | 2016-2020 • Monthly | Captures financing-cost pressure on owner households |
| **Bureau of Labor Statistics Consumer Price Index, all urban consumers (CPI-U)** | 2016-2020 • Monthly | Used later to inflation-adjust incomes to real 2020 dollars |


## 5  Reproducing the Results
```bash
# 1. clone the repository
git clone https://github.com/dxliang001/SIADS593--Milestone-1.git
cd SIADS593--Milestone-1

# 2. create the Conda environment (Python 3.10)
conda env create -f environment.yml
conda activate siads593_affordability

# 3. launch JupyterLab
jupyter lab
