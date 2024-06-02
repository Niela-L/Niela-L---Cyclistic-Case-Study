# Cyclistic-Trip-Data-Case-Study
This is my approach to the Cyclistic case study, using BigQuery for exploratory analysis of Divvy trip data, and Tableau for data visualization production.

# Scenario
I am a junior data analyst working on the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success
depends on maximizing the number of annual memberships. Therefore, my team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, my team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve my recommendations, so they must be backed up with compelling data insights and professional data visualizations.

# About the company
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships.

Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members. Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a solid opportunity to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs. Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. 

In order to do that, however, the team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

# Business task
### Aim: Increase the number of annual memberships

Towards this goal, three main questions are asked:
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

# Prepare the data
To answer the questions above, the Divvy datasets concerning Jan 2023 to Dec 2023 were used for further analysis. Each dataset was downloaded as a .csv file from [here](https://divvy-tripdata.s3.amazonaws.com/index.html). Cyclistic is a fictional company. These datasets were made for the purpose of this case study. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement). This is public data that can be used to explore
how different customer types are using Cyclistic bikes.

The datasets were loaded into BigQuery to be merged into one dataset. The combined dataset was then cleaned, and an exploratory analysis was performed to assess for differences between casual riders and members.

# Data Cleaning & Trasnformation 
At this stage, I confirmed that all 12 datasets had the same 13 columns. Then, I joined all datasets into one dataset. I checked for duplicate rows (0 duplicates rows), and for missing values (the columns start_station_name, start_station_id, end_station_name, end_station_id, end_lat & end_lng, had missing values). I decided to later in my data cleaning & transformation process to drop the rows with missing values. 

I checked for datatype for each column and observed that the data types were all correct.

Next, new columns were created to display **trip length** (=trip duration,in minutes) and trip_distance (using a built-in Bigquery function to calculate distance from the latitude and longitude coordinates; in meters). I also created additional columns to contain the **month**, and the **day of the week** to be easier assess for trends in bike usage throughout the year, and week.

The cleaned dataset was free of missing values & duplicates rows. Data types were correct and necessary columns were added. This dataset was ready for further analysis.

# Exploratory Analysis
At this stage, I analyzed the previously cleaned combined dataset to assess for differences in bike usage between casuals and members.

I compared the average trip length (min) & distance (m), number of trips throughout the year, week, and day, and the types of bikes used between casuals and members. I also looked at geographic localizations most preferred by the different riders. This process showed key differences in how casuals and members used Cyclistic bikes differently.

After this analysis, I saved my cleaned dataset as a .csv file to upload it to Tableau.

# Visualization creation
After an initial exploratory analysis in BigQuery, the combined dataset was loaded into Tableau. When doing this, I noticed that I had to separate the columns manually to ensure the correct structure of the data. I then attributed the correct data type to each column. 

The key findings can be found in [Tableau](https://public.tableau.com/shared/4ZT3T2DHX?:display_count=n&:origin=viz_share_link)


# Top three recomendations based on key findings:
1. **Seasonal campaigns**: Launch summer and/or weekend membership campaigns through email, to attract casual riders who may not want annual memberships

2. Offer members **exclusive access** to Cyclistic bikes during peak hours (early morning and late afternoon)

3. Offer membership **group discounts** to encourage group rides

4. **Target preferred departure stations**: ensure bike availability for members at those stations. Most frequented departure stations could also provide a way to target specific places for the previously recommended marketing strategies
