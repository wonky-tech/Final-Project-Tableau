# Final-Project-Tableau

## Project/Goals
The goal of this project is to demonstrate ability with Tableau by completing visualizations for a given dataset. I chose to work on the dataset of house prices, indices and other economic indicators.

The set questions/tasks for the housing and economic data are given in the `assignment.md` file available from this repository:

- Show the trend of house prices across Canada in the last 40 years (table `housing_price_index`).
- Compare the trend after 2005 with actual benchmark prices in table `real_estate_prices` to see if there are any differences.
- Compare this trend with the trend of office prices. Which one is getting more expensive, faster?
- Create a heatmap of Canada with current house prices for each available district.
- Are the price differences between different districts increasing?
- Compare the trend of house prices with earnings.
- Did people spend more of their earnings in 2014 than they did in 2001?
- There were several economic crises in the world in the last 40 years, including these four: Black Monday (1987), Recession (early 1990s), dot com bubble (2000 - 2002), Financial crisis (2007 - 2009). Show the effect of these crises on:
	- Earnings
	- House prices
	- Office prices
	- House constructions
	- Consumer index
- Plot `consumer_index` together with `housing_price_index` and fit the regression line between them. Can we predict `consumer_index` from the `housing_price_index`?
- Try to find an interesting pattern, trend, outlier, etc. from the data used in the above questions.


## Process
I worked through each question/task in turn, using the appropriate data file for each. There were notable points in the process:
1. Generally, I displayed trends on a line graph.
2. I chose to use a table with heatmap shading for regional house price trends. 
	1. Tableau could only show province on a geographical map; showing regions does not appear to be part of the software, or would require extra location data for Tableau to display. 
	2. I cleaned up region names, removing unhelpful characters where necessary. I added a province indicator to each region line. 
	3. I combine multiple sheets for each region into a single CSV file of all regions using Python to make it easier to display in Tableau.
3. I displayed changes in the housing price index over time with coloured lines for each region. This highlighted trends in two subgroups.
4. To compare changes in house prices with earnings changes, I displayed house prices as a multiple of average earnings.
5. To display earnings, I used Python to convert a wide table with many columns (for each region) into a long table with only three columns: Date, Earnings and Region.
6. To highlight the effect of financial crises on economic indicators, I used the Tableau annotate region feature on line graphs.
7. I used Tableau dashboards to add 

## Results
I chose to work on option 1, with housing data and economic indices like earnings and housebuilding data. 


## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
