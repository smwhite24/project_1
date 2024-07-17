Project Description: 
  Our group compared mortgage rates against real estate prices. Our assumption was that increasing mortgage prices have a negative effect on real estate prices, because as mortgage rates increase and it becomes more difficult to borrow and afford to purchase a home, prices will follow and decrease. 

Installation instructions: 
  Please download the files in the github and ensure you have the following dependencies in your environment: Panadas, Numpy, MatPlotLib, SciPy. The raw data files are included in Resources folder. The visual outputs are in the Outputs folder. This was run in VS Code or can be ran in Jupyter Notebook. 

Data Sources: 
  Zillow Data was sourced on 7/9/2024. Zillow data is monthly median sales prices per metro area that is smoothed and seasonally adjusted. We use data for all home types (single-family home rentals and condos) as well as exclusively single-family rentals (SFR).
[(https://www.zillow.com/research/data/)]

  Mortgage Data was sourced on 7/15/2024 from Freddie Mac. It includes weekly interest rates for different types of mortgages. Merging with the Zillow data, so we have Nashville median prices for all and for single-family rentals in one place. 
[(https://www.freddiemac.com/pmms)]


We imported and read data from Zillow.


We only want to look at Nashville data so we dropped other locations. We have 68 time points for median sales prices in Nashville starting in 2018 and ending in 2024. Data is collected at the end of each month.


We shape real estate data, transposing, renaming columns and adjusting data types so that we can merge using it later.

We then imported and read mortgage data from FreddieMac. We drop all NA values and values that aren't mortgage or date data. We rename the column names and drop irrelevant columns. We then changed the data types for analysis later.

We keep the last data from each month to match with median sales prices.

We then can merge the data mortgage and median sales data on month/year, and again ensure the data is the right type for analysis.

We then plotted both all median sales prices and single family rental median sales prices against time and saw that they were remarkably similar so we ran a t-test to ensure that they weren't statistically significantly different.

We did the same with mortgage rates but ran an anova test instead because there were three series.

We then plotted median sales prices for all against 30yr fixed mortgage rates over time.

Lastly, we calculated the correlation coefficients and produced two regressions. We produced one for 30yr FRM and one for 5/1 ARM because ARM seemed to deviate from both 30 and 15 year FRM. #Real estate prices below 300000 seem to have a negative relationship with mortgage rates while real estate median prices over 300k looks like to have an exponential relationship with mortgage rates.

In the future we’d like to incorporate census data (demographic data like education, race, or income) to help explain changes in real estate prices. Additionally, we would like to explore what effect the pandemic had on median prices. In the future we could also look at the frequency of homes being put up for sale or being taken off the market. Mortgage rates affect buyers borrowing power and may have a greater effect on frequency of sales rather than price. 
Our data was limited to median sales prices for only single family rentals and condos. We if had more time we would have explored the differences across commercial and residential prices and across different types of homes (1br, 2br, 3br). 

Throughout this project we used Xpert Learning Assistant to trouble shoot code and visualizations. 
