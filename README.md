# New york Citibike Data Exploration and Visualization
## by Alaa Alsaiery

### Dataset

[Citibike](https://www.citibikenyc.com/system-data) is Citi Bike is the US's largest bike share program. Mainly designed for quick trips.

The data used in this document includes all bike trips recorded from September,1st 2020 until October, 13th 2020. The dataset consists of 53754 trips, with the following features:

* Trip Duration (seconds)
* Start Time and Date
* Stop Time and Date
* Start Station Name
* End Station Name
* Station ID
* Station Lat/Long
* Bike ID
* User Type (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member)
* Gender (Zero=unknown; 1=male; 2=female)
* Year of Birth

*Note on data as shared by citibike: data has been processed to remove trips that are taken by staff as they service and inspect the system, trips that are taken to/from any of our “test” stations (which we were using more in June and July 2013), and any trips that were below 60 seconds in length (potentially false starts or users trying to re-dock a bike to ensure it's secure).*

### Data wrangling process:
- fix multiple fields that are not in the correct dtype, i.e. `start_time`, `end_time` should be datetime type, `user_type` and `member_gender` should be categorical data type, etc
- add new columns for age, trip duration in minute
- filter out outlier (ages and trip durations) from visual examination of the member age distribution and statistical percentile
- Change gender to categorical variable 
- Add column to count trips by station


### Exploration to Making Finding

Exploration analysis, allowed me to dig deep into the data and find further questions and queries. It also help assessing and cleaning data, learning more about distribution of some features. 

### Main Finding

* The hishest number of rides are actually fall into the (5-10 minutes tripduration) range. The average of citibike rides in New York is 14 Minutes.
* Almost 67% of bike riders are Male, while only 33% are Female, however Female riders have higher mean of tripduration. Another interesting finding, is that the third top age group of riders is 50 to 55 Years old riders
* The stations with the highest number of trips are actually not condensed in one area. There is one in midtown, two in lower manhattan, one in williamsburgh, one in Brooklyn, one in Queens, Two in Hrlem and Twon in The Bronx.