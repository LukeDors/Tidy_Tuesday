# House and Mortgage data

Data comes from the Freddie Mac House Price Index at both the State and National level. The original source can be found [here](http://www.freddiemac.com/research/indices/house-price-index.html).

The House Price Index (HPI) is a broad measure of the movement of single-family house prices. The HPI is a weighted, repeat-sales index, meaning that it measures average price changes in repeat sales or refinancings on the same properties. This information is obtained by reviewing repeat mortgage transactions on single-family properties whose mortgages have been purchased or securitized by Fannie Mae or Freddie Mac since January 1975. - Quote from [Federal Housing Finance Agency](https://www.fhfa.gov/DataTools/Downloads/Pages/House-Price-Index.aspx)

Included are some recession dates in the US - the Great Recession (2007) had some major effects across many industries and markets. You can read more about some of the recent changes [here](http://bit.ly/2019-week6) from Fortune.

# Data Dictionary

### state_hpi.csv

|variable    |class     |description |
|:---|:---|:-----------|
|year        |date - integer   |      Year      |
|month       |date - integer   |    Month        |
|state       |character |   US State         |
|price_index |double    |   Calculated House Price Index - average price changes in repeat sales or refinancings at state level         |
|us_avg      |double    |   Calculated House Price Index - averaged at national level         |

### mortgage.csv

* Please notice that 30 year fixed rate data goes back to 1971, while the 15 year data begins in 1991 and the adjustable 5-1 Hybrid begins in 2005.

|variable                              |class  |description |
|:-----------|:---|:-----------|
|date                                  |date |     Date       |
|fixed_rate_30_yr                      |double |     Fixed rate 30 year mortgage (percent)       |
|fees_and_pts_30_yr                    |double |      Fees and percentage points of the loan amount      |
|fixed_rate_15_yr                      |double |     Fixed rate 15 year mortgage (percent)       |
|fees_and_pts_15_yr                    |double |      Fees and percentage points of the loan amount      |
|adjustable_rate_5_1_hybrid            |double |      5-1 Hybrid Adjustable rate mortgage (5 year fixed, then annual adjustable rate)     |
|fees_and_pts_5_1_hybrid               |double |     Fees and percentage points of the loan amount       |
|adjustable_margin_5_1_hybrid          |double |      A fixed amount added to the underlying index to establish the fully indexed rate for an ARM.|
|spread_30_yr_fixed_and_5_1_adjustable |double |      Difference in rate between 30 year fixed and 5-1 adjustable      |


### Recessions

* You should probably just go to the [Wikipedia article](https://en.wikipedia.org/wiki/List_of_recessions_in_the_United_States) - but this is a small list of recessions in the USA.

|variable                             |class     |description |
|:-----------|:---|:-----------|
|name                                 |character |    Recession Name        |
|period_range                         |character |        Time period range of the recession    |
|duration_months                      |character |      How long the recession lasted      |
|time_since_previous_recession_months |character |    Time since previous recession in months        |
|peak_unemploy_ment                   |character |  Peak unemployment (percent)          |
|gdp_decline_peak_to_trough           |character |     GDP decline from peak to trough       |
|characteristics                      |character |  Paragraph description of the recession          |