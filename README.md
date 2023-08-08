# Project Description

Hello there :wave:
I hope this project finds you well!

In this project, I will identify patterns that determine whether a game can be considered successful or not. By doing so, you can discover the most promising games and plan advertising campaigns. Data related to user and expert reviews, genres, platforms (such as Xbox or PlayStation), and historical game sales data is available from open sources. The data is from the year 2016. Let's assume that it's now December 2016, and I am planning a campaign for the year 2017.

**Objective**
To perform user profiling for each region, in order to understand the platforms and genres with the highest sales and potential profitability. Additionally, to analyze how user and expert reviews influence sales on one of the popular platforms.

**Hypotheses**
1. The mean user rating for the Xbox One and PC platforms is the same.
2. The mean user rating for the Action and Sports genres is not the same.

# Steps

1. Data Overview
2. Data Preprocessing
3. Exploratory Data Analysis
4. Hypotheses Testing

## 1. Data Overview

**Data Description** 

The dataset contains the following columns:
- `Name` - name
- `Platform` - platform where the game is played
- `Genre` - game genre
- `NA_sales` - sales in North America in millions of USD
- `EU_sales` - sales in Europe in millions of USD
- `JP_sales` - sales in Japan in millions of USD
- `Other_sales` - sales in other regions in millions of USD
- `Critic_Score` - review score from critics, up to 100
- `User_Score` - review score from users, up to 10
- `Rating` - rating provided in ESRB format


## 2. Pre-Processing Data

The following are data preprocessing steps I did in this project:
1. Standardize Column Names
2. Working with Missing Values
3. Fixing Data Types
4. Adding New Columns


## 3. Exploratory Data Analysis:

  

1 (full dataset) How many games were released in different years? is the significant for each period? 
	
**Findings**

- Game sales in the year range 1980 - 1991 show a bullish trend.
- Game sales demonstrate an upward trend in the year range 1992 - 2008.
- Game sales show a declining trend in the year range 2010 - 2013.
- Game sales in the years 2014 - 2016 turn bullish again.
- Sales exhibit a significant increase from 2001 to 2002. In 2001, the number of released games was around 400, but in 2002, game sales doubled with a value of around 800.
- The peak of sales is observed in the years 2008 and 2009.

2. (full dataset) How does sales vary from one platform to another?

**Findings**

- From the distribution above, it can be inferred that sales vary across different platforms.
- The platform with the highest total sales is PS2.

3. (full dataset) Find platforms that were once popular but now have no sales at all. How long does it usually take for a new platform to emerge and for an old platform to fade in popularity?

**Findings**

- The average lifespan of a platform's popularity is around 2-5 years (based on the popularity data of NES, PS, PS2, DS, Wii, PS3, X360, and PS4).
- A platform typically takes about 2-3 years to become popular.
- PS2 had the highest level of sales, reaching 1227 units. PS2 entered the market in 2000 and had no sales by 2011.

4. (reference dataset) Which platforms have the highest sales? Which platforms are growing or shrinking? Select several platforms that have potential for profitability. Are the sales differences significant? What about the average sales on various platforms?

**Findings**

-   The platform with the highest sales is PS4.
- There are several significant differences in sales. Sales on platforms 3DS, PC, PSV, DS, and PSP have noticeable differences compared to platforms PS3, X360, PS4, XOne, WiiU, and Wii, which have higher sales.
- The average sales across various platforms also show diverse variations. However, the formed pattern indicates that the median is closer to the lower end (Q1), resulting in a positively skewed distribution.

5. (reference dataset) How does sales vary from one platform to another?

**Findings**
- The platform with the highest sales in the year range 2013-2016 is PS4.
- Based on the data from 2013 to 2016, all platforms experienced a downward trend.
- The growth of PS4 can be considered very rapid within a span of 1 year (2013 - 2014).
- A platform that has the potential for profitability is PS4, as its sales started to rise in 2014. Therefore, it is still in demand and has the potential for profitability based on the trend.

6. (reference dataset) Examine how user and professional reviews influence sales on the most popular platform (PS 4 - based on my analysis in point 3.5)

**Findings**

- From the correlation heatmap and scatter matrix graphs above, conclusions can be drawn regarding interrelated variables:

- total_sales and critic score exhibit a moderate weak positive relationship. As total_sales increases, there is a higher likelihood of a higher critic_score.

- critic_score and user_score show a moderate to high positive relationship. As user_score increases, there is a higher likelihood of a higher critic_score.

7. (reference dataset) Distribution of User and Professional Reviews and whether reviews influence sales on the second popular platform (PS3). Additionally, the comparison between the most popular platform (PS4) and the second popular platform (PS3)

**Findings**

- Analysis of the Comparison between Game Sales on Platforms 'PS4' and 'PS3:

	The results indicate consistency, with a strong enough relationship existing only between critic score and user score, while the correlation between total_sales and critic score shows a weak positive correlation.

8. (reference dataset) Observe the overall distribution of games based on genre. What can we conclude about the most profitable genres? Can you make generalizations about genres with high and low sales?

**Findings**

- From the distribution above, it can be observed that sales vary across different genres.
- The genre with the highest total sales is action.

9. (reference dataset) User Profiling by Region

**Findings**

- The detailed order of game sales based on ratings in the EU, NA, and JP regions can be seen below:

	1. EU: M, E, E10+, T

	2. NA: M, E, E10+, T

	3. JP: T, E, M, E10+

- Variations in sales for each rating:

	1. Games with the M rating (Mature - 17 and up) have the highest sales in the EU and NA, and rank third in JP.

	2. Games with the E rating (Everyone - All ages) rank second in the EU and NA, and second in JP as well.

	3. Games with the E10+ rating (Everyone 10+ - Ages 10 and up) rank third in the EU and NA, and fourth in JP.

	4. Games with the T rating (Teen - Ages 13 and up) rank last in the EU and NA, but have the highest sales in JP.

**Insight:**

ESRB ratings do influence sales in each region, as they reflect the market conditions in the three regions. 

# Hypotheses Testing

#### Hypothesis 1: The mean user rating for the Xbox One and PC platforms is the same.


**Verdict**
The average user rating on the Xbox and PC platforms is not the same.
Meaning: Users on the Xbox and PC platforms have different impressions/rating values.

**Insight**
These two platforms provide different experiences. It might be worthwhile to delve deeper into the experiences for each platform.

#### Hypothesis 2: The mean user rating for the Action and Sports genres is not the same.

**Verdict**
The average user rating for the Action and Sports genres is not the same.
Meaning: Users in the Action and Sports genres have different impressions/rating values.

**Insight**
These two genres provide different experiences. It might be worthwhile to delve deeper into the experiences when playing games in both of these genres.

# General Conclusion

1. The profiles in the EU and NA regions show similarities in terms of platforms, genres, and ESRB ratings. Japan stands out as the region with the most distinct profile.

2. Strategies to increase profits can be based on the specific profiles of each region. For EU and NA regions, similar strategies could be employed with some modifications tailored to the unique aspects of each region, such as popular gaming platforms.

3. The correlation between variables in the reference dataset for the year 2017 is as follows:

	- Total sales and critic score have a moderate weak correlation (0.41). Higher total_sales are associated with higher critic_scores.

	- User_score and critic_score have a moderate high correlation (0.56). Higher user_scores correspond to higher critic_scores.

	- Total sales and user_score do not have a significant relationship (-0.034).

4. The concluded hypotheses are:

	- The average user rating for the XBox and PC platforms is not the same.

	- The average user rating for the Action and Sports genres is not the same.

5. The platform with potential for development in the year 2017 is the PS4.

6. The genre with potential for development in the year 2017 is the action.
