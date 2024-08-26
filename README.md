# Cyclistic Trip Data Case Study
## Overview
This project explores the Divvy bike trip data using BigQuery for exploratory analysis and Tableau for data visualization. The goal is to understand how casual riders and annual members use Cyclistic bikes differently in order to inform strategies aimed at increasing annual memberships.

## Scenario
As a junior data analyst working on the marketing analyst team at Cyclistic, a bike-share company in Chicago, I have been tasked with analyzing how casual riders and annual members use Cyclistic bikes differently. This analysis aims at designing a marketing strategy to convert casual riders into annual members, an effort supported by data-driven insights and visualizations. 

## About the company
In 2016, Cyclistic launched a successful bike-share program. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships.

Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members. Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a solid opportunity to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs. Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. 

In order to do that, however, the team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

## Business task
### Aim: Increase the Number of Annual Memberships

Towards this goal, three main questions were addressed:
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders consider buying Cyclistic annual memberships?
3. How can Cyclistic leverage digital media to influence casual riders to become members?

## Data Preparation
To answer the questions above, the Divvy datasets concerning Jan 2023 to Dec 2023 were used for the present analysis. Each dataset was downloaded as a .csv file from [here](https://divvy-tripdata.s3.amazonaws.com/index.html). 

Cyclistic is a fictional company. These datasets were made for the purpose of this case study. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement). This is public data that can be used to explore how different customer types are using Cyclistic bikes.

The datasets were loaded into BigQuery to perform data merging and cleaning. The combined dataset was then prepared for exploratory analysis.

## Data Cleaning & Transformation 
- Datasets: Confirmed that all 12 datasets had the same 13 columns, merged them into one dataset, and addressed potential duplicate rows and and missing values by dropping affected rows.  

- Columns: Created new columns for **trip length** (duration in minutes) and **trip distance** (calculated using latitude and longitude coordinates). Also added columns for **month** and **day of the week** to analyze monthly or weekly trends.

- Quality: Ensured there were no missing values or duplicate rows and confirmed data types were correct.


## Exploratory Analysis
Performed an exploratory analysis to compare bike usage between casual riders and members:
- Analyzed the average trip length (min) & distance (m), number of trips throughout the year, week, and day, and bike types used.
- Analyzed geographic preferences of the different bike riders.
- Saved cleaned dataset as a .csv file for Tableau visualization production.


## Visualization creation
Imported the cleaned dataset into Tableau, manually adjusting column structures, and setting the correct data types when needed. The visualizations highlight key findings, available at [Tableau] https://public.tableau.com/shared/4ZT3T2DHX?:display_count=n&:origin=viz_share_link)

## Recommendations
Based on the key findings, the following strategies are recommended:
1. **Seasonal campaigns**: Launch summer and/or weekend membership campaigns through email, to attract casual riders who may not want annual memberships

2. **exclusive access**: Offer members exclusive access to Cyclistic bikes during peak hours (early morning and late afternoon).

3. **Group discounts**: Offer membership **group discounts** to encourage group rides

4. **Preferred stations**: Ensure bike availability for members at frequently used departure stations. These locations could also provide a way to target new and existing customers for the marketing strategies mentioned above.
