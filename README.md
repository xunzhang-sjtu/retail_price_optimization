# RETAIL PRICE OPTIMIZATION
Price optimization using price elasticity
* Merged and standardized the data from the differents data sources.
* Explored the data to gain information about it and to discover insights.
* Transformed the variables to a better fit of the model.
* Developed and optimized a linear regression model to obtain and understand the price elasticity.
* Predicted the quantity sold for a set of prices for a given day (parameterized) to obtain the optimal price that maximizes revenue.

## Objective
The objective is to set, for a specific day, the optimal price of a product, maximizing profits.

## Code and Resources Used 
**Python Version:** 3.8.5 

**Packages:** pandas, numpy, sklearn, matplotlib, seaborn

**Burger Cafe CSV:** https://onedrive.live.com/?authkey=%21AHDkRFUvt4FI8Wc&id=7BA8848FE0992BD8%21278810&cid=7BA8848FE0992BD8&parId=root&parQt=sharedby&o=OneUp

## Data Wrangling
There are 3 CSV that have different information about the transactions made in the Burger Cafe. In this phase, I merged and cleaned them in order to have the data ready to work with.
 *  Make a first approach to the Cafe Burger´s Data.
 * 	Identify keys from all data sources and combine them.
 
## EDA & Modeling
 *  EDA using pandas profiling to get a first intuition about the data. Here I discovered the distribution of the numerical variables, correlations, the existence of null and duplicated values.
 *  Solved the existence of null values problems by studying the feature that contained them.
 *  Cleaned the duplicated values identifying those that were the real ones using the d+1 and d-1 mean for the duplicated values.
 *  Feature engineering to create more relevant features.
 *  Univariate and multivariate analysis to understand the data. Here I discovered that each sell id can have 1 or more products (combos) and that the sell id 1070 quantity and price differs a lot from the rest.
 *  Splitted the dataset by sell id.
 *	Used the box cox transformation for all numerical since they had a bimodal distribution and I wanted to make them more symmetrical.
 *  Used the z-score transformation for all the numerical features to scale down the values.
 *	Developed an OLS model using the most relevant features (p-value < 0.05).
 * 	Set for a specific day (based on the data features used to fit the model) a range of different prices and use the model to obtain the one that maximizes the revenue.