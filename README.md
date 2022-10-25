# Che_Math
This repository was created to collect all the coded-related homework and projects developed within the course $Mathematical$ $Methods$ $in$ $Chemical$ $Engineering$ from the Chemical and Petroleum Engineering Department at the University of Pittsburgh. The programming languages used for this purpose are Julia and Python.

## Project 1:
Regression tools are used to analyze COVID-19 data in the US at the County level for the states of California, Florida, and New York. The two factors (independent variables) considered in the analyses are (1) the total population 25 years and over with a Bachelor's degree or higher and (2) the household income. The measurement (independent variable) is the mortality rate per 100K population up to the end of 2021. The study is performed through 4 Jupyter notebooks organized as follows:

0. Preliminary data analysis: A preliminary data analysis is performed to select the US States of interest on which the study will be conducted. Some of this data is visualized at the country and state levels. 
1. Data pre-processing: Raw data is collected, filtered, and consolidated in DataFrames for further analysis. Also, some scattered plots are used to display the qualitative correlation between the independent and dependent variables.
2. Dataframe_grouping: The consolidated DataFrames are grouped by defined criteria. The selected states and county-level data are displayed using Histograms to see the frequency distribution of each factor and measurement.
3. Model fitting: The data is fitted using linear regression tools for two simple comparisons (2 factors) and one complex comparison (3 parameters) that includes interactions.
