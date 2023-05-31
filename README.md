# cyclistic-bike-share_analysis_capstone
This repository contains my capstone project for the Google Data Analytics Professional Certificate. 

The case study presents a scenario where you act as a junior data analyst working for the fictional company Cyclistic Bike-Share. The analyst will answer key business questions by following the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

The file cyclistic-bike-share-analysis-in-r_project.ipynb is a copy of the RMarkdown Notebook in .ipynb format which displays the code and output including visualization.

The index.html is the html version which can be viewed at the following github pages URL:  
https://jluera.github.io/cyclistic-bike-share_analysis_capstone/

I also have a version in Kaggle that is just slightly different as I used a similar but not 100% the same dataset and had to make a small amount of minor code changes due to Kaggle environment. This version can be seen here:
https://www.kaggle.com/code/jasonluera/cyclistic-bike-share-analysis-in-r-capstone

Verification of completion of the Google Data Analytics Professional Ceritificate can be seen here:
https://www.credly.com/badges/376995e4-efeb-41c0-aa6f-e78c847f04d6

## A summary of the relevant deliverables minus the actual code and output can be seen below.

## **ASK**
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.

Cyclistic currently provides three pricing plans:

* Single-ride-pass  
* Full-day-pass  
* Annual Membership  

The marketing director wants to create a campaign to convert Casual Riders (single-ride-pass or full-day-pass users) into Annual Members. The junior analyst is tasked with reviewing the prior year's trip data to gain insights into how Casual Riders and Annual Members use Cyclistic Bike-Share differently.

Three questions will guide the future marketing program:

* How do annual members and casual riders use Cyclistic bikes differently?  
* Why would casual riders buy Cyclistic annual memberships?  
* How can Cyclistic use digital media to influence casual riders to become members? 
 
You will produce a report with the following deliverables:  

* A clear statement of the business task  
* A description of all data sources used  
* Documentation of any cleaning or manipulation of data  
* A summary of your analysis  
* Supporting visualizations and key findings  
* Your top three recommendations based on your analysis  

### **Statement Of Business Task**
In order to design marketing strategies aimed at converting Casual Riders into Annual Members, the provided data shall be analyzed to better understand how Annual Members and Casual Riders differ, why Casual Riders would buy a membership, and how digital media could affect their marketing tactics.

### **Description Of All Data Sources Used**
Trip data representing Cyclistic's past year of trip records is sourced from real world data of the bike-share company Divvy. This data is provided by Lyft Bikes and Scooters, LLC which operates the City of Chicago's Divvy bike-share service. The data comes in the form of monthly CSV files. The CSV files can be downloaded here. The Data License Agreement can be found at the following link.

This data pulled for this analysis represents the past 12 months of trip data. There are 13 columns in each CSV file, each of which reprsents a single ride. The data has been sanitized so that there are no identifying records denoting a specific user. As such, we cannot use the data to determine how specific individuals use the service or to find trends in how they utilze multiple rides. However, we do have enough data to identify general differences between the two types of riders we are concerned with; Casual Riders and Annual Members.

### **Summary Of Changes**
So far during the pre-processing and cleaning phase we have made the following changes:

* Merged 12 dataframes into one called trips.  
* Renamed the rideable_type column values of "docked_bike" to "classic_bike" for consistency.  
* Added the following columns:    
&nbsp;&nbsp;&nbsp;&nbsp; - date  
&nbsp;&nbsp;&nbsp;&nbsp; - hour  
&nbsp;&nbsp;&nbsp;&nbsp; - day  
&nbsp;&nbsp;&nbsp;&nbsp; - month  
&nbsp;&nbsp;&nbsp;&nbsp; - year  
&nbsp;&nbsp;&nbsp;&nbsp; - day_of_week  
&nbsp;&nbsp;&nbsp;&nbsp; - ride_duration  
* Renamed the following columns:  
&nbsp;&nbsp;&nbsp;&nbsp; - Changed rideable_type to  ride_type  
&nbsp;&nbsp;&nbsp;&nbsp; - Changed started_at to start_time  
&nbsp;&nbsp;&nbsp;&nbsp; - Changed ended_at to end_time  
&nbsp;&nbsp;&nbsp;&nbsp; - Changed member_casual to customer_type   
* Filtered out rows where the ride_duration is less than 1, including many negative duration values.  


### **Summary Of Analysis**
**Rider Distribution:** Annual Members make up the majority of rides with 59.67% of the ride share compared to 40.33% from Casual Riders.  
**Ride Duration:** Casual Riders tend to take the longest rides on average, with an average ride duration of 29 minutes compared to 13 minutes for Annual Members.  
**Peak Weekly Traffic:** Traffic for Casual Riders tends to peak on the weekends whereas Annual Members tend to ride more during the week days.  
**Peak Daily Traffic:** On average, traffic for both Casual Riders and Annual Members peaks around 5:00pm every day, with the 4:00pm to 6:00pm range being significantly higher than the rest of the day.  
**Peak Seasonal Traffic:** The bike-share tends to be more popular in the summer months for both types of customers. However, the ride increase during the summer months is significantly higher with the Casual Riders compared to the Annual Members.  
**Bike Preference:** Casual Riders seem to prefer Electric Bikes whereas Annual Members seem to have a very slight preference for Classic Bikes.  
**Ride Locality:** Casual Riders tend to stick around the Lake Shore Drive region of Downtown Chicago, rarely going more than a few blocks from it.  Annual Members tend to spread their rides out more across the entire downtown Chicago area.

## **ACT**
Based on this analysis, my recommendations are as follows:  
1. **Consider adding an alternative membership or additional plans which are catered to Casual Riders.** Considering that Casual Riders tend to ride mainly during the summer months, take much longer rides compared to Annual Members, and stick to a smaller area of downtown Chicago near Shoreline Drive, it seems highly probable that a large segment of this group includes visitors to Chicago. A yearly membership may not be very appealing to this type of rider. However, you could offer additional packages which would suit them better. For example, adding a summertime membership with an allowance for longer rides may be a good way to entice Casual Riders to pay for a membership. Likewise, consider offering a weekend only membership or a week long pass option, which may go a long way towards enticing different segments of Casual Riders into paying more ahead of time. For those Casual Riders who do live in the downtown Chicago area, another option which may lead to more Annual Membership signups is increasing the allotted ride time for Annual Members, especially for users of Classic Bikes which are more affordable but would also take longer to reach their destination.

2. **Initiate a survey campaign for market research.** Obtain better data from actual Casual Riders to see why they use the bike-share service and why they have not signed up for an Annual Membership. Given the current data, all we can do is speculate on why Casual Riders are using the service the way that they do. I suggest we run a targeted survey campaign focused primarily on Casual Riders. We would offer discounts or an extended ride time to a randomized selection of Casual Riders in exchange for them answering a short survey. This would provide us which much better information regarding the target customer and we can hear from them directly on why they use the service and why they don't pay for the Annual Membership. That information could then be used to improve business decisions in the future.

3. **Initiate a campaign utilizing local "influencers" and social media to spread the word on the benefits of an Annual Membership.** Target some of the more popular "influencers" in town to help advertise the bike-share service to locals and visitors alike. Have those selected demonstrate how convenient the Cyclistic bike-share product is, and how easy it is to quickly get to various popular spots in downtown Chicago while using it. Likewise, run a social media campaign utilizing Annual Members and offer a discount or various perks if they make a social media post mentioning why they love using Cyclistic bike-share.

### **REFERENCES:**
* RDocumentation  
* R Charts  
* The R Graph Gallery  
* rstudio Community  
* Kaggle Community  
* Stack Overflow  
