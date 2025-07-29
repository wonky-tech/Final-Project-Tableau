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
5. To display earnings, I used Python to convert a wide table with many columns (for each region) into a long table with only three columns: Date, Earnings and Region. I converted weekly earnings to average monthly earnings.
6. To highlight the effect of financial crises on economic indicators, I used the Tableau "annotate region" feature on line graphs.
7. For the Consumer Price Index, it was necessary to filter for percentage as CPI percentages with combined in the same file with index figures.
8. I used Tableau dashboards to add captions to each graph and combined them into a Tableau story to be saved on Tableau public for conversion to PDF and PPT files.

## Results
I chose to work on option 1, with housing data and economic indices like earnings and housebuilding data. Combined into a Tableau story, the final presentation was 12 slides with the following graphs and conclusions:
1. **National HPI trend: **The trend in national House Price Index has been increasing gradually since the end of the 2007-2009 financial crisis, and increasing rapidly in recent years since the start of the pandemic in 2020.
2. **House Price Index trend vs benchmark prices**: The trend in national House Price Index is compared with benchmark house prices for the same period. It shows both increasing gradually, with an increase in growth of the benchmark prices in recent years.
3. **Office Price Index trend vs House Price Index**: The trend in the national House Price Index is similar to the Office Price Index.
4. **Canada house price heatmap showing benchmark prices**: The heatmap of benchmark house prices shows relative differences between regions and over the years. Darker shading shows the gap between metropolitan centres and other areas is growing.
5. **HPI trends by region shows two main groups**: Regional trends in house prices shows a difference between some regions (Regina, Saskatoon, Winnipeg, St Johns and the rest of NL) and mostly GTA, Ontario, BC and major metropolises. The former group, group 1 on the lower left, increases dramatically 2009-2013, then drops off in recent years. In contrast, the latter group 2, on the lower right, shows slower growth for the same time period and a rapid increase starting around 2015.
6. **Canadian earnings track HPI**: Average earnings track the House Price Index surprisingly closely, apart from a slowing in  HPI growth during the financial crisis around 2008.
7. **Housing costs taking from earnings**: The benchmark cost of a house is shown as a multiple of average earnings. There was a steep increase in housing as a multiple of earnings from 2005-2008, dropping dramatically around the financial crisis. The trend steepens again from 2011-2016.
8. **Canadian average monthly earnings**: I only have data for two of the financial crises mentioned, but they seem to have little effect on average earnings. Later slides show a contrasting larger effect on other economic indicators.
9. **Housing Price Index vs Office Price Index**: The impact of finacial crises on housing and office market price indexes is similar. Both are affected by the 90's recession and the 2008-2009 financial crises. They are less affected by Black Monday in 1987 and the dot com bubble 2000-2002.
10. **Housing Starts**: The impact of crises on house construction appears to be the most dramatic, compared to other economic indicators.
11. Consumer Price Index: Major financial crises have a measurable impact on the Consumer Price Index, a measure of inflation that excludes housing costs.
12. **CPI vs HPI**: There is a relationship between the Housing Price Index and the Consumer Price Index, with an r-value of 0.47.

**A Notable feature of the CPI graph**: The apparently high inflation at the start of the graph is not an error. Canada experienced high inflation in the seventies and early eighties. Anti-inflationary measures, like interest rate increases, controlled inflation but also triggered a recession.

## Challenges 
Making some of the mentioned file transformations using Python on Excel sheets was a stretch for me. I'd previously mostly worked on CSV files. It was also a challenge ensuring that the graphs were giving sensible images to reflect the data. For instance, I didn't realise at first that CPI data needed to be filtered for percentage or index, because the two were on the same sheet.

## Future Goals
Given more time, my main goal would be to add interactivity to the charts where it makes sense to improve comprehension.

[Link to Tableau Public](https://public.tableau.com/views/FinalProjectTableau17534797159890/CostsandTrendsinCanadianHomeOwnership?:language=en-US&publish=yes&:sid=&:redirect=auth&:displaycount=n&:origin=vizsharelink)
