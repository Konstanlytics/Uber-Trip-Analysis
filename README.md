# Uber-Trip-Analysis

## 📍 Project Summary

This project shows a simple and clear analysis of Uber trips over one month. The dashboard helps anyone—whether you're part of a ride-sharing team or just exploring data—understand when people take the most trips, what days are busiest, and how trip patterns change over time.

With this dashboard, you can:

- Spot the busiest times and days for Uber rides  
- See when demand is low and adjust schedules  
- Make smarter decisions about driver availability  
- Improve how the service runs overall

## 🌟 Key Features

- **Interactive Visuals** – Explore trips by time and day with slicers, filters, and hover-over tooltips  
- **Time-Based Insights** – Easily spot trends like peak hours and busiest days using heatmaps and charts  
- **Custom Date Table** – Allows flexible filtering and better handling of time-based calculations  
- **Clean & User-Friendly Layout** – Simple navigation with clear visuals that are easy to understand  
- **KPI Cards** – Quick stats on total trips, average duration, and overall distance at a glance

## 🧰 Tools and Data Source

**Tools Used** : Power BI, DAX (Data Analysis Expressions).

**Data Source**  
The data comes from one month of Uber trip records. It includes information such as:

- Date and time of each trip  
- Pickup and drop-off locations  
- Trip distance and duration  
- Fare amount  

This data was used to spot trends, understand ride patterns, and gain insights into how Uber is used throughout the month.


## 🧹 Data Preparation Process

To make the data easier to understand and analyze, it was cleaned and organized into separate tables in Power BI. Here's what was done:

### 🔄 Normalization  
The trip data was split into smaller tables to keep things neat and easy to work with:

- **Trip Details** – Has the main trip info like fare amount, pickup time, number of passengers, and location IDs  
- **Location Table** – Lists all the pickup and drop-off locations, along with the city names  
- **Date Table** – A custom calendar table with days, weekdays, and more to help filter by time  
- **Measure Table** – Holds calculated values like average trip distance, trip duration, and booking value  
- **Dynamic Parameter Table** – Helps make the visuals more interactive (like letting users switch between different views)

### 🔗 Data Modeling 
- The **Trip Details** table was linked to the **Date Table** using the trip date, so we can break things down by day or week  
- It also connects to the **Location Table** twice — once for the pickup location and once for the drop-off. Since Power BI only allows one connection to be active at a time, we used a DAX formula called `USERELATIONSHIP` to activate the second one when needed  
- These connections make it easy to filter and explore the data from different angles

![Modelling](https://github.com/Konstanlytics/Uber-Trip-Analysis/blob/main/Modelling.JPG)

## 📅 Date Table Setup

To support time-based analysis for this one-month dataset, a custom Date table was created using DAX in Power BI. The date range is fixed from June 1 to June 30, 2024, and includes useful columns such as:

Day, Month, and Year

Day Name and Day of Week

Month Name (full and short)

Week of Year

Weekend Indicator

This table enables flexible filtering and breakdowns in visuals like trends, comparisons by weekday, and calendar-based insights.

![Date table](https://github.com/Konstanlytics/Uber-Trip-Analysis/blob/main/Date%20table.JPG)



## Data Analysis

![Overview Analysis](https://github.com/Konstanlytics/Uber-Trip-Analysis/blob/main/Overview%20Analysis.JPG)

### 🔍 Key Metrics

- Total Bookings: 103.7K

- Total Booking Value: $1.6M

- Average Booking Value: $15.00

- Total Trip Distance: 349K miles

- Average Trip Distance: 3 miles

- Average Trip Duration: 16 minute

### 📈 Trip Trend Analysis
The daily trip chart shows that people booked rides fairly steadily all month, but there were some busy days, especially around the middle and end of the month.

This could mean more people needed rides during weekends, special events, or maybe when Uber ran promos.

This kind of chart helps the team know when demand is high, so they can make sure enough drivers are available and maybe even run special deals or adjust prices smartly.


### 💳 Payment & Time of Day Breakdown

**Total Booking Values Info :**

- *Payment Type:*

Uber Pay: 70.47% of total booking value

Cash: 28.45%

Other (Amazon Pay, Google Pay): Less than 1%

- *Trip Time:*

Day Trips: 86.72%

Night Trips: 13.28%

These numbers show that most people prefer paying through the app instead of using cash. Also, most rides happen during the day — which likely means people are using Uber for things like work, errands, or appointments, rather than late-night outings.


### 🚗 Vehicle Type Performance  
- **UberX** had the highest number of trips (**38.7K**) and brought in around **$584K**, making it the most popular option for riders  
- **UberXL** and **Uber Black** followed closely, often used for bigger or more luxurious rides  
- **Uber Green** had the fewest trips, which could mean fewer eco-friendly cars are available or not many riders choose them

### 📍 Location Insights  
- **Most Frequent Pickup Point:** Penn Station / Madison Square West  
- **Most Frequent Dropoff Point:** Upper East Side North  
- **Longest Trip:** Lower East Side to Crown Heights North — about **144.1 miles**

These popular spots help highlight where people commonly start or end their trips. This kind of info can help Uber place more drivers in busy areas and possibly adjust pricing during peak times.

### 🚘 Preferred Vehicle by Location  
- **UberX** is the top choice at the busiest pickup and drop-off locations  
- This shows it's a favorite because it's likely affordable, easy to find, and gets the job done for most riders
