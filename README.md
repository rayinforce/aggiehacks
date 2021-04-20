# aggiehacks-team xianghenaicha

CONTENTS OF THIS FILE
---------------------

## Introduction
This project explores the covid’s impact on the house price growth in the USA using the regression analysis, built from R. 

## Data Gathering and Storage
All data are collected from publicly available sources such as Zillow open reseach housing data, state population data, US Cencus Bureau Housing Security data collected after April 2020, etc. 

Links to data sources:

US Census Bureau	https://www.census.gov/data/experimental-data-products/household-pulse-survey.html
Our World in Data	https://github.com/owid
CDC	https://data.cdc.gov/Case-Surveillance/United-States-COVID-19-Cases-and-Deaths-by-State-o/9mfq-cb36
NYTIMES covid data	https://github.com/nytimes/covid-19-data
US Census Bureau	https://www.census.gov/housing/hvs/data/index.html
US Census Bureau	https://www.census.gov/data/datasets/time-series/demo/popest/2010s-state-total.html
Freddie Mac (2021-04-11). 15-Year Fixed Mortgage Rate: 15-Year Fixed Mortgage Rate | , 08/30/1991 - 04/08/2021. Data Planet? Statistical Datasets: A SAGE Publishing Resource. (Dataset). Dataset-ID:  021-001-002

All data used can be found in the zipped file from the shared link to google drive:
https://drive.google.com/drive/folders/1o-ESU5pSACs9DIm_vwE4_aw0OTZG7E2b?usp=sharing

## Modules
*zillow_house_process.Rmd:*
	This file processes the housing data obtained from Zillow research and output country level, state level and county level home value time series data and growth rate over time.

*housing_security_data_processing.Rmd:*
	This file processes the housing security survey statistics from the US Census Bureau. I take in all the weekly files in raw Excel format, then cleans the data and consolidate them to one in country level and the other in state level.

*visualization_and_clustering.Rmd:*
	This file contains a part of further data cleaning for the housing security data and conduct k-means clustering on selected data.
  
*Modeling_xianghenaicha.RMD:* 
Run this model to launch the modeling including time series analysis (optional) and regression analysis.

## Simple Graphs of Model performace
linear model:
					Estimate	Pr(>|t|)
Intercept				0.1822		6.19E-02
num_listing_sfr_growth_rate		-0.003748	2.09E-05
in_covid				0.129		3.20E-15
people_fully_vaccinated_per_hundred_diff0.03228		< 2e-16
mortgage_rate				-0.3211		< 2e-16
house_completion			9.366E-07	< 2e-16




Clustering:
![image](https://user-images.githubusercontent.com/60135226/115432329-d5934980-a238-11eb-9a98-78fe0d07e543.png)

![image](https://user-images.githubusercontent.com/60135226/115432368-daf09400-a238-11eb-8d3d-b38b52207bb5.png)

![image](https://user-images.githubusercontent.com/60135226/115432562-18edb800-a239-11eb-861c-6b0a25d1c254.png)







## Maintainers
Rosie Wang (roselainewang@gmail.com)
Rui Zheng (raywithoute@gmail.com)
