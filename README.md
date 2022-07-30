# Ford-GoBike-Data-Exploration-and-Visualization-of-insights

## 1. Investigation Overview

> This project has two parts that illustrates the importance and value of data visualization techniques in the data analysis process which is as Capstone project part of the Udacity Data Analysis Nanodegree course.

> In this part (1/2) I will use Python visualization libraries to systematically wrangle and explore a `201902-fordgobike-tripdata.csv` datafile, starting from plots of single variables and building up to plots of multiple variables.

> In the following second part of the project (2/2), I produced a short presentation that illustrates interesting properties, trends, and relationships that I discovered in the selected (cleaned) dataset.


## 2. Dataset Overview

Bay Wheels is the first regional and large-scale bicycle sharing system deployed in California and on the West Coast of the United States. It was established as Bay Area Bike Share in August 2013. 

This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area during 1`February 2019`. The dataset can be downloaded [here](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv)s


## 3. Wrangle/Clean to create cleaned datafile `fordgobike-tridata_clean.csv` (part 1)

After opening the data (CSV) into the worksheet, I cleaned the data based on the issues I found when assessing the data. I did the following:
- I found out that starttime and endtime have wrong datatypes `string` (in stead of datetime), I changed the datatype yo datetime.

- I also found out that user_type has wrong datatype `string` (in stead of categorical)

- Also, there were null Values in some rows, the rows were dropped.

- There was an odd year for a row in member_birth_year as one row was very odd, this would affect my analysis, I then dropped the row also.

- I created a column for duration_min, start day this was done because I would be needing this in my analysis to see days of the week that had some events and the minutes to help make meaning out of what I have from seconds.

After all this, I exported the file into `201902-fordgobike-tripdata_clean.csv`



## 4. Summary of Findings of Data Exploration (part 1)

After exploring the data and visualizing my findings, I saw that:

- The graphs reinforces the idea that people tend to use bikes as a means of transportation on week days and the peak times are when they go to work and leave work, the use of bikes drastically reduces by weekends.

- Subscribers mainly hire a bike during weekdays (more than double the level of weekdays), while for Customers, they hire relatively the same number of trips all week round.

- It is very interesting to note that the duration of trips in the weekdays is significantly lower than on weekends in both the subscribers and Customers.

- The average bike trip duration of Customers is about the double of Subscribers(21 to 10 mis).

- Males subscribers spend more time on the road than other genders (other and females) but averagely, they spend less time on the road. This shows that most of the males durations fall in the lower spectrum.

>Note: The Data Exploration has been done in notebook `Part I Dataset Exploration - Ford Go-Bikes.ipynb`.


## 5. Key Insights for Presentation slides (part 2)

In this presentation, I focused my attention on the relationship between user_type, gender and duration.

I began with a barchat showing the two user types and their number od occurrences showing that the subscribers are more than the customers.

I then followed my presentation with the genders and the number. I also visualized this with a barchat showing that the males are more than the female and other gender.

Then, I presented a boxplot of the user type and duration showing that majority of customers spend more time on the road than subscribers.

I finished my visualization with a striplot showing the relationship between the three variables, showing that the although males spend subscribers spend more time on the road (in total), they averagely spend lesser time with other and females spending more time on the road on an average.
