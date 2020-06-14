# PyBer Analysis

### Assignment Details and Analysis

  The goal of this assignment was to take the data from both the city_data.csv and the ride_data.csv to create a joint data frame that summarizes the key metrics for the ride-sharing data by city type. The analysis was performed by calculating total fares, total drivers, total rides, average fare per driver, and average fare per ride from the each data sources onto a new joint data frame then grouping by city types. To get this information the functions used to create these calculations were sum(), count(), and groupby(). After creating the first table a separate pivot table was created using a merged data frame of the two CSV files to show the total fares by date per city type. Functions use to perform this technical analysis were groupby(), pd.to_datetime(), set_index(), reset_index(), rename(), sum(), pivot(), and loc(). A multi-line chart was then created using Matplotlib (see Fig. 8).
#### Results

  Based on the multi-line chart (Fig. 8) we can conclude that the Urban city areas have the highest fares, Suburban areas have the second highest, and Rural city areas have the lowest fares. Each city type appear to have a peak in their fare prices in late February.
  
  ![alt_text](https://github.com/clefemine/PyBer_Analysis/blob/master/Analysis/Fig8.png)
  Fig. 8
  
### Challenges
 
  Challenges that were encountered when analyzing the data included creating a pivot table where the index remains the date. This can be solved by using the reset_index() object and then the pivot() object to create a properly formed table. Another challenge was grouping the fare amount per city type by weeks. This can be solved using the resample() method and knowing that "W" will group by week. Sizing the chart image was also a challenge, but by running different dimensions it's possible to find the proper size needed.
  
### Discussion

  Based on the analysis, the different city types vary greatly. It would benefit the analysis to look into this trend with a variety of technical approaches using the data provided. I recommend comparing the total ride and driver counts based on city types. This would show if the city types show a difference in demand in rides compared to the amount of drivers available. This can be done with two bar graphs with city types in the x-axis and the y-axis containing either total driver or total rides. I would also recommend analyzing whether there is a particular time of the day that rides are more desire based on city types. This process would be similar to the analysis that created Fig. 8, this would not take into account the day of the year, only the time of the day. Using the DateTimeIndex() method the time of the day can be extracted. Comparing the number of ride counts and fares throughout the day can give insight on when a driver can expect to make more money based on higher ride demand and city types will show variation. 
