# Bike-Share Marketing Analytics Dashboard

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiMzVmZDhlNjAtY2NiNy00YjY4LTg5MzYtMGM5MDI4NTExOGQzIiwidCI6IjhjYTA1MzkxLWJlNjYtNDk5Zi1iMTg1LTZkYjI4YTJlNmMwYiJ9&pageName=ReportSection

## Problem Statement

This dashboard helps the bike-sharing company understand their riders better. It helps the bike-sharing company know if their riders are preferring casual rides or member rides. Through different number of rides analysis, they get to know their marketing strategies and plans. It also lets them know the number of rides by month & bike type, thus since by using this dashboard they have identified that marketing of cyclistic annual membership can be done on weekends from 4-6 pm at the most popular locations.

Since, number of member riders (almost 61 %) are more than casual riders (around 39 %), thus in all they must keep this thing in mind while working on the marketing campaign.

Also since total number of rides in winters are less than the total number of rides in summers, thus they must keep this thing in mind while working on the marketing campaign.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 : For calculating total number of rides by rider type, null values were not taken into account as around 8% values are null in total.
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various rides, thus in order to represent total rides by months, a new visual was added. 
- Step 8 : Visual filters (Slicers) were added for the rider type which are "Casual" & "Members".
- Step 9 : Calculated date columns were created named "Date", "Month", "MonthNum", "Weekday" & "WeekdayNum".

For creating new columns following DAX expression was written;
       
        Dates = CALENDAR(DATE(2023, 05, 01), DATE(2023, 10, 31))
        
        MonthNum = MONTH(Dates[Date])
        
        Month = FORMAT(Dates[Date], "mmm")
        
        WeekdayNum = WEEKDAY(Dates[Date])

        Weekday = FORMAT(Dates[Date], "ddd")
        
Snap of new calculated columns,

![Snap_1](https://github.com/Sid-Gogia-007/Bike-Share-Marketing-Analytics-Report/assets/155529593/46568eba-24f7-415e-bf4b-29eca05fcb48)
- Step 10 : Two chart visuals were added to the dashboard, pie chart representing number of rides by rider type & donut chart representing number of rides by bike type.
           
           Although, by default, while calculating average, total & month rides blank values are ignored.
- Step 11 : Two column charts were also added to the report design area representing the number of rides by month and number of rides by weekday. While creating this visual, field named "Rider Type" was also added to the Legends bucket, thus number of customers are also seggregated according the Rider type. 
- Step 12 : A line chart was also added to the dashboard representing the number of rides by ride hours in the day.
- Step 13 : In the report view, under the insert tab, two text boxes were added to the canvas, in one of them name of the bike-share company was mentioned & in the other one company's brief description was written.
- Step 14 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area.
- Step 15 : A matrix and map visual were used to represent start and end stations.

Snap of matrix and map,

![Snap_Count](https://github.com/Sid-Gogia-007/Bike-Share-Marketing-Analytics-Report/assets/155529593/fa7c5972-8e58-4533-a8bb-15e9d3e48bd9)
        
 - Step 16 : The report was then published to Power BI Service.

# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://github.com/Sid-Gogia-007/Bike-Share-Marketing-Analytics-Report/assets/155529593/85bf718d-7c6b-4d43-9f97-03857eb77d44)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://github.com/Sid-Gogia-007/Bike-Share-Marketing-Analytics-Report/assets/155529593/a173eb51-113b-4f02-80f0-b946d00b886c)

![Dashboard_upload](https://github.com/Sid-Gogia-007/Bike-Share-Marketing-Analytics-Report/assets/155529593/61f2f09e-e72f-4370-98a1-8387f2804c99)

![Dashboard_upload](https://github.com/Sid-Gogia-007/Bike-Share-Marketing-Analytics-Report/assets/155529593/4e9aa224-e4fd-4a48-82b1-a60157d3551b)

# Insights

A three page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard:

(1) We can clearly see that there are more member riders than the casual riders type in all the months, as the total number of rides is approximately 3 million, in which around 60.8% are members and 39.2% are casual riders.

(2) The number of rides are maximum on the weekends in comparison to the weekdays for the casual riders. 

(3) By seeing the charts in the dashboard, we can also say that it is clearly evident that only casual riders have used the docked bikes.

(4) After analysing the line chart we can identify that there is a decline in terms of the riders during the winter months.


           Marketing of Cyclistic Annual Membership can be done for casual riders on weekends from 4 pm to 6 pm at the most popular locations like Streeter Dr & Grand Ave, Dusable Lake Shore Dr & Monroe St/North Blvd , Michigan Ave & Oak St and Millennium Park.
