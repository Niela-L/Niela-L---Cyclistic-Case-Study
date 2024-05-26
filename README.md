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
To answer the questions above, the Divvy datasets concerning Jan 2023 to Dec 2023 were used for further analysis. Each dataset was downloaded as a .csv file from [here](https://divvy-tripdata.s3.amazonaws.com/index.html). Cyclistic is a fictional company. These datasets were made for the purpose of this case study. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement). This is public data that you can use to explore
how different customer types are using Cyclistic bikes.

The datasets were loaded into BigQuery for exploratory analysis and to be able to join all datasets into one dataframe that could then be used to produce data visualizations in Tableau. 

# Cleaning data + exploratory analysis in BigQuery (SQL) 
At this stage, I confirmed that all 12 datasets had the same 13 columns. Then, I joined all datasets into one dataframe. I checked for missing values and for duplicate rows (0 duplicates rows). I decided to keep the rows with missing values as I could just not consider these when doing my analysis or visualization of the data. 

I checked for datatype for each column and observed that the data types were correct.

Next, a new column was created to display **trip length** (in minutes) to be able to assess differences between casual customers and members. I also created additional columns to contain the **month**, and the **day of the week** to be easier to make exploratory analysis regarding bike use throughout the year and week.

# Analysis
At this stage, I analyzed the previously cleaned combined dataset to assess for differences in bike usage between casuals and members.

I compared the average trip length, numbers of trips throughout the year and week, and the types of bikes used between casuals and members. This process showed key differences in how casuals and members used Cyclistic bikes differently.

After this analysis, I saved my cleaned dataset as a .csv file.

# Visualization creation
After an initial exploratory analysis in BigQuery, the cleaned combined dataset was loaded into Tableau. When doing this, I noticed that I had to separate the columns manually to ensure the correct structure of the data. I also noticed that some columns had the wrong data type.

To be continued












