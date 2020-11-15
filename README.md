# Kickstarting with Excel

## Overview of Project


The project is focused on kickstarter campaigns in the entertainment sector. Our clients project is the kickstart of a play named Fever. I started with an initial data analysis on several thousand crowdfunding projects to uncover hidden trends and provided more specific details with filters and pivot tables and graphs. The data analysis was performed on kickstarter data to uncover trends to show results and trends on successful and failed kickstarted campaigns in several countries. Data was filtered for the US, GB and examples from the theater category. Categories vary in success as shown in the graph. 

![Parent Category Outcomes](https://user-images.githubusercontent.com/60243906/99124385-26c25180-25a6-11eb-87ca-3de3793b2bd4.jpg)


### Purpose

The purpose of this analysis is to inform a clients decision rgearding the launch, budgeting and development of a play kickstarter campaign. In a first step, I provided global and national examples and trends to show kickstartes with the best potential, outline challenges and suggest the most feasable funding goal. The purpose of the project was to provide the client with visual information around campaign outcomes based on their launch dates and their funding goals to further advance their kickstarter campaign.

## Analysis and Challenges

#### Descriptive Data Theater Category

Data suggests that out of 912 theater plays, 525 were successful and 349 failed. To understand the reason behind the failure an analysis was conducted on project goals and pledged amounts. 

![Theater outcome](https://user-images.githubusercontent.com/60243906/99125097-810fe200-25a7-11eb-8925-df29442d6ac9.jpg)

Descriptive statistics for goals and pledged amounts, average donations and numbers of backers show that the mean goal for successful theater plays was $5,048 while failed plays aimed for almost double ($10,554). The mean pledge of successful plays was $5,601 while only $558 for failed projects. 

The data shows that, in addition to the needed funding, the launch date seems to be significant, since especially launching in the second quarter seems to be promissing for successful plays. 


![Picture1](https://user-images.githubusercontent.com/60243906/99124545-7a349f80-25a6-11eb-821b-0ac94a1e0e46.jpg) 

From the plot chart below, we can see that the mean campaign goal is around £4,000. This is outside of the range of outliers for amount pledged, we can recommend to produce the play for less than £4,000. Half of the campaign goals are less than £2,000, which is just over the 3rd quartile for amounts pledged.


![plot chart](https://user-images.githubusercontent.com/60243906/99124649-a9e3a780-25a6-11eb-9cdf-fc9e71040ded.jpg)


### Analysis of Outcomes Based on Launch Date

I conducted my analysis in several steps. I started with the Theater Outcomes by Launch Date task. To complete this task, I had to create a new collumn in the Kickstarter spredsheet for "Years", using the YEARS formula. Afterwards, I created a pivot table with year and parent category as filters, outcomes in columns, date created in rowns and count of outcomes as values. This table shows how the success and faliure of plays show a seasonal trend. The table visualizes the data. 

<img width="362" alt="Theater Outcomes Based on Launch Date" src="https://user-images.githubusercontent.com/60243906/99160754-77ad7500-268e-11eb-874f-c62c33438a61.png">

### Analysis of Outcomes Based on Goals

To conduct this part of the analysis, I created a new sheet with the funding goals as 12 different categories. I worked with the formula =COUNTIFS to determine the number of campaigns in each of the goal ranges, and differentiated between successful, failue and canceled projects. The formula I used to determine the amount of successful kickstartes e.g. with a goal below 1000$ Goal is as follows.  =COUNTIFS('Goal Success'!A:A, "<1000")
I did the same for every other goal range and each of the three categories. Afterwards, I added the amount of projects for each goal range and calculated the percentage of success, failed and canceled projects for each of the 12 goal ranges. I then created a pivot table to create a pivot graph. 


<img width="761" alt="Outcomes_vs_Goals" src="https://user-images.githubusercontent.com/60243906/99160753-75e3b180-268e-11eb-87c2-aea1cb55924e.png">



### Challenges and Difficulties Encountered

One challenge I faced was the order of the funding ranges when creating the pivot graph in the last part of the analysis. Excel sorted the categories in a way that wasn't ascending but seemed arbitrarily. Consequently, the graph didn't display the information in a way that made sense. It took me some time to solve the issue but finally found a function to move the rows in a pivot table manually. Another challenge I faced was that excel slowed down noticeably with added sheets and more information. I'm not sure why since I have a MacBook Pro 2020. A last challenge I encountered was in the analysis of outcomes based on goals. When working with the formula  =COUNTIFS, excel crashed whenever I filtered the outcomes collumn. To get around this problem, I c/p the filtered collums successful, failed, cancelled and created new sheets for each so excel didn't have to draw information for the formula from the biggest data sheet in the file. It seemed to work this way. 



## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

Most theater outcomes are successful if they are launched in May (111/839) and June (100/839). Most theater outcomes fail if they are launched in July and October. There seems to be the tendecy of theater kickstartes to be more successful when they are launched in the second quarter of the year while the distribution of failed kickstartes is way more balanced throughout the year. Succesful kickstarter have a mean of 69.92 and median of 68, while failed kickstartes have a mean of 41.1 and median of 39.5 with a total of 839 and 493 respectively. In conclusion, the launhcing date only seems to affect a positive outcome but negative outcomes seem to have different reasons than the date. 

- What can you conclude about the Outcomes based on Goals?

This part of the analysis gives us more insight into reasons for kickstarters to fail. Kickstartes have the tendency to become less successful the bigger the funding goal gets. As long as the funding goal is below 1000$, the sucess rate is 75%, if between 1000-4999, 72.25% and then almost exponentially declines with another slighlty higher success rate in the 35k - 45k range (66%). However, the data is small for this funding goal and might not be significant. A trens is that the higher the funding goal is, the more likely a kickstarter is to fail. Peaking at 45k-50k with a 1000% fail rate. 

- What are some limitations of this dataset?

The data set might be incomplete and 

- What are some other possible tables and/or graphs that we could create?

We could correlate outcomes based on launch date and outcomes baded on goals to see if the goal is correlated with the date for failed kickstarters. 
