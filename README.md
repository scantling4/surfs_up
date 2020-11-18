# surfs_up


## Overview of the Analysis:

## Purpose

The purpose of this analysis was to look at temperature trends during the months of June and December in Oahu, Hawaii in order to determine if the surf and ice cream shop business is sustainable year-round. This was done using SQLite and SQLAlchemy. 

## Results:

-	The mean temperature is higher in June than it is in December.
-	There are about 150 more data points for the temperatures collected in June which is shown in the “count” row. 
-	The mean temperatures, however, do not vary by very much. In June the mean temperature is 74.94 degree, while in December the mean temperature is 71.04. 
-	The standard deviations of temperatures for both months are relatively similar. For June, it is 3.257 while for December it is 3.746.

![June Temperature Summary](/june_temp_summary.png)
![December Temperature Summary](/december_temp_summary.png)

## Summary: 

The results for this analysis are quite informative. As shown in the summary statistics, the mean temperature does not vary by much (three degrees) within six months. This supports the proposal that an ice-cream and surf shop would be a sustainable business all year round. More analysis should be done on the other months as well to look at the temperature trends for each month over the years. The relatively small standard deviation (about three degrees) for each month suggests that the weather does not vary much during those months. 

- Performing these two additional queries will gather the precipitation data from Oahu for the months of June and December. This will allow for a more informative analysis and thus influence the decision to open a surf shop or not. 

- june_precipitation = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
- december_precipitation = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
