# Simple-Global-Covid-19-and-GDP-Analysis.
Examines a simple relationship between national GDP-per capita and covid statistics using public datasets. Free for viewing and commentary.

# Lets get started!
This starter data analysis project is structured based on Absent Data's video demonstration: https://www.youtube.com/watch?v=iwUli5gIcU0&list=WL&index=2&t=2076s
# 1-5
In addition to the four packages he makes use of- Pandas, Seaborn, Matplotlib, and Sklearn- I also include Numpy for the purpose of splicing the public datasets I utilize into a single usable format. The three datasets I use summarize data on world country populations, country GDP per capita, and by-country Covid-19 reported cases and deaths. Links will be provided at the end of the readme.
Cell 2 prepares the raw data for processing, mainly by limiting each dataset to the latest year (2021 for GDP, 2022 for population, and 2023 for Covid data) and setting up any NA values that might exist to be removed. Cells 3-5 provide heads for each cleaned dataset.
# 6-12
Cells 6-12 splice consistent data from the three dataframes into a single dataframe with columns on a list of countries and their respective continents, cumulative deaths and cases in 2023, 2021 GDP-per-capita in USD, population in 2022, and derived rates of deaths per-thousand cases, cases per million people, and deaths per million people. Several notes on the splicing process:
  - Each column is entered into the final dataset assuming that the countries the data cells are assigned to are always arranged in alphabetical order, and that the countries that make it in exist in all three of the base datasets. This should assure that all statistics match their respective countries. The length of each column is confirmed in cell 9. 
  - The rates are derived from the quotients of the statistics in the separate dataframes, rather than official statistics, since the goal of this project is to see how these datasets of different sources interact.
# 13-15
The following three cells conduct univariate visual analysis on the single dataframe (the "percountry" dataframe). Distribution plots on most of the statistics show a distribution significantly skewed to the left, but this is largely due to outliers on the high end. The following kernel density estimate plots raise further questions on the data by showing an unusually low case and death rate per million people in Africa. The apparent "sparing" of Africa from the expected effects of Covid-19 (in WHO data) has puzzled experts, but whatever the reason, these observations are enough to exclude these statistics from any further analysis due to their inonclusivity. In contrast, the death rate per thousand cases 
