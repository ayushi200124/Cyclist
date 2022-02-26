# Cyclistic
<img src="https://user-images.githubusercontent.com/79920441/155269317-7ba5e33e-b731-44ba-a9c3-d787bf8756ac.gif" width="300" height="200">

You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director
of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore,
your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights,
your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives
must approve your recommendations, so they must be backed up with compelling data insights and professional data
visualizations.

**Contents**
1. [Characters and Team](#chr)
2. [ About the company ](#comp)
3. [Ask](#ask)
4. [Prepare](#prep)
5. [Process](#pro)
6. [Analyze](#ana)
7. [Share](#sh)
8. [Act](#act)
9. [Wrap Up](#wrap)
<a name="chr"></a>
## 1. Characters and Team

- **Cyclistic:** A bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself
apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with
disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about
8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to
commute to work each day.
- **Lily Moreno:** The director of marketing and your manager. Moreno is responsible for the development of campaigns
and initiatives to promote the bike-share program. These may include email, social media, and other channels.
- **Cyclistic marketing analytics team:** A team of data analysts who are responsible for collecting, analyzing, and
reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy
learning about Cyclistic’s mission and business goals — as well as how you, as a junior data analyst, can help Cyclistic
achieve them.
- **Cyclistic executive team:** The notoriously detail-oriented executive team will decide whether to approve the
recommended marketing program.

<a name="comp"></a>
## 2. About the company

In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that
are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and
returned to any other station in the system anytime.
Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments.
One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes,
and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers
who purchase annual memberships are Cyclistic members.
Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the
pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will
be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a
very good chance to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic
program and have chosen Cyclistic for their mobility needs.
Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to
do that, however, the marketing analyst team needs to better understand how annual members and casual riders differ, why
casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are
interested in analyzing the Cyclistic historical bike trip data to identify trends.

**Guidelines- Three questions will guide the future marketing program:**
- How do annual members and casual riders use Cyclistic bikes differently?
- Why would casual riders buy Cyclistic annual memberships?
- How can Cyclistic use digital media to influence casual riders to become members?

Moreno has assigned you the first question to answer: How do annual members and casual riders use Cyclistic bikes
differently?
You will produce a report with the following deliverables:
- A clear statement of the business task
- A description of all data sources used
- Documentation of any cleaning or manipulation of data
- A summary of your analysis
- Supporting visualizations and key findings
- Your top three recommendations based on your analysis

<a name="ask"></a>
## 3. Ask
**Guiding questions**
- What is the problem you are trying to solve?
- How can your insights drive business decisions?
 
**Key tasks**
1. Identify the business task
2. Consider key stakeholders

**Deliverable**
A clear statement of the business task

### My Approach-
- Task 1: The problem statement clearly states two important facts.
i. The marketing team has recognized that the revenue can increase when we convert our part-time customers into our full-time customers, i.e., make them take our annual subscription
ii. The data we have also states that 30% of our users have annual subscription but a large proportion of 70% has not used our premium membership but has used our services at least once.We will analyze user behaviours on how annual members and casual riders use Cyclistic bikes differently to make recommendations on how to convert casual riders into annual members
- Task2: The secondary stakeholder here is the Cyclistic Marketing Executive Team and my primary stakeholder should be Lily Moreno. Right now I would be recommending Moreno and team, on what makes casual drivers not to take our annual subscription and what drives our annual customers to avail our services. This whill make us understand how both the sections of the customers are using our services and what are their expectations.

<a name="prep"></a>
## 4. Prepare
**Guiding questions**
- Where is your data located?
- How is the data organized?
- Are there issues with bias or credibility in this data? Does your data ROCCC?
- How are you addressing licensing, privacy, security, and accessibility?
- How did you verify the data’s integrity?
- How does it help you answer your question?
- Are there any problems with the data?
 
**Key tasks**
1. Download data and store it appropriately.
2. Identify how it’s organized.
3. Sort and filter the data.
4. Determine the credibility of the data

**Deliverable**
A description of all data sources used

### My Approach-
1. The dataset is made available in [12 Months Cyclistic Data](https://divvy-tripdata.s3.amazonaws.com/index.html) and the naming convention of the files are: YYYYMM-divvy-tripdata.csv . I have downloaded the data from 202102-divvy-tripdata.csv to 202201-divvy-tripdata.csv as the most recent 12-months analysis. Each dataset contains almost 100k to 400k rows and 13 columns. 
    - ride_id : Unique id of each ride trip
    - rideable_type : type of bicycle ridden, split between 3 categories - classic, docked and electric
    - started_at : date and time of the start of the trip
    - ended_at : date and time of the end of the trip
    - start_station_name : Start station name
    - start_station_id : Start station id
    - end_station_name : End station name
    - end_station_id : End station id
    - start_lat : latitude of the start location
    - start_lng : longitude of the start location
    - end_lat : latitude of the end location
    - end_lng : longitude of the end location
    - member_casual : type of membership, either casual or member
2. Additional data limitation that I have spotted from the above metadata is, due to no personal information available, I am unable to tell how often the same user uses the bike in the month and how frequently, and from which stations. Hence, I can only make the assumption that each ride id corresponds to a unique rider spread across the days of the month.
3. The data given has a consistency since the data types match with the kind of data stored and is well formatted under correct names. Further I will check for outliers in the analysis process. 
4. I have taken a random sample of each dataset in order to reduce the complexity of the data and ease of using the spreadsheet. I reduced the population sample to 10k-10.5k rows (randon group n= total no. of cell/10k). Steps to execute random sampling:

`select a cell -> =RANDBETWEEN(1,n) -> fill the entire column -> copy the column -> follow the link` -> [watch next steps](https://www.youtube.com/watch?v=bNUAQsThmAc)


<a name="pro"></a>
## 5. Process
**Guiding questions**
- What tools are you choosing and why?
- Have you ensured your data’s integrity?
- What steps have you taken to ensure that your data is clean?
- How can you verify that your data is clean and ready to analyze?
- Have you documented your cleaning process so you can review and share those results?
 
 **Key tasks**
1. Check the data for errors.
2. Choose your tools.
3. Transform the data so you can work with it effectively.
4. Document the cleaning process.

**Deliverable**
Documentation of any cleaning or manipulation of data

### My Approach-
In excel I performed some tasks-
- Made a new column= month `ctrl+c -> write the column name -> ctrl+enter`
- Made a new column= day_of_week `=WEEKDAY((start_time_cell),1)`
- Made a new column= ride_length `=(started_at)-(ended_at)`
- Made a new column= exact_start_time `copy started_at column -> paste -> format cells -> hh-mm AM\PM`
- Made a new column= season `ctrl+c -> write the column name -> ctrl+enter`
    - December,January, February= Winter
    - March, April, May= Spring
    - June, July, August= Summer
    - September, October, November= Autumn
- Removed duplicates if any `select the sheet -> data -> remove duplicate rows`
<a name="ana"></a>
## 6. Analyze
**Guiding questions**
- How should you organize your data to perform analysis on it?
- Has your data been properly formatted?
- What surprises did you discover in the data?
- What trends or relationships did you find in the data?
- How will these insights help answer your business questions?
 
 **Key tasks**
1. Aggregate your data so it’s useful and accessible.
2. Organize and format your data.
3. Perform calculations.
4. Identify trends and relationships.

**Deliverable**
A summary of your analysis

### My Approach-
Uploaded dataset to kaggle and started a new kernal to analyze the statistical informations in R. I have performed the following steps-
- 
<a name="sh"></a>
## 7. Share
**Guiding questions**
- Were you able to answer the question of how annual members and casual riders use Cyclistic bikes differently?
- What story does your data tell?
- How do your findings relate to your original question?
- Who is your audience? What is the best way to communicate with them?
- Can data visualization help you share your findings?
- Is your presentation accessible to your audience?
 
 **Key tasks**
1. Determine the best way to share your findings.
2. Create effective data visualizations.
3. Present your findings.
4. Ensure your work is accessible.

**Deliverable**
Supporting visualizations and key findings

### My Approach-

<a name="act"></a>
## 8. Act
**Guiding questions**
- What is your final conclusion based on your analysis?
- How could your team and business apply your insights?
- What next steps would you or your stakeholders take based on your findings?
- Is there additional data you could use to expand on your findings?
 
 **Key tasks**
1. Create your portfolio.
2. Add your case study.
3. Practice presenting your case study to a friend or family member

**Deliverable**
Your top three recommendations based on your analysis

### My Approach-


<a name="wrap"></a>
## 9. Wrap Up

