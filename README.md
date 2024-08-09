# Steam Games Analysis - Project Overview
1 of 10 teams to compete in the Inauguraul Spring 2023 Association of Information Systems (AIS) @ CSULB Datathon in April 2024.
My team took 1st place!!

## Background
Teams were assigned randomly based on skillset information given to AIS through a survey before the datathon. The challenge was to come up with a business problem and deliver strategic recommendations in front of a panel of judges. 

My team approach was to become a hypothetical analytics and consulting firm, BARS, and offer solutions to a struggling game development company who is seeking to reverse a trend of underperforming titles. More specifically the founder of the company is a passionate gamer and is tasking us with using extensive data to identify their next successful game project according to financial success but more important, a well loved game by the gaming community.

## Dataset Structure
Each row in the data set was a one of the 85k titles with 38 columns. After preprocessing (see below) I finished with 63k and 21 columns. 

### Preprocessing
- Removed 17 uniformative columns (urls, images, age, median, operating systems, etc.)
- Excluded zero reviewed games
- Filtered out 10k+ games 0 owners
- Eliminated outliers with high pricing (above $150) - 0.001% had games priced that high
- Removed anomaly of a game with future release date
- Removed data prior to 2010 due to very little amount of games
- Cleaned estimated owners on the hyphen to have min and max owners to calculate revenue
- Flattened and counted every occasion for genre, language, and category - Turned long lists of strings in individual string form hashed to AppID.
  
## Insights Summary
Underperformance for our stakeholder can mean a number of things so we will use KPI's to answer a 6 key quetions about the gaming market. Although we have historical data we will only be using the past 5 years to answer these questions and uncover trends using a Tableau dashboard. We believe using the past 5 years would be more relevant to analyze than using all-time data for the launch of a new game.

- **Number of Games: Is there still is a market for gaming?**
  - 2010-2017: There was a robust and nearly double increase in the number of new games released each year, reflecting a thriving and expanding market.
  - 2018-2023: While the total number of games released has doubled, there has been a noticeable decline since 2022, with about a 15% decrease in new (since 2021) releases. This suggests a possible saturation or market adjustment.
    
- **Revenue: Is there still is money to be made in gaming?**
  - Revenues = Estimated owners multiplied with price
  - 2010-2017: Revenue grew significantly at an average annual rate of 35%, despite a 7% annual decrease in average game prices. This indicates strong market demand and value.
  - 2018-2023: Revenue more than doubled initially, but there has been a sharp 40% decline since 2022, despite rising prices by roughly 10% yearly. The decline could be due to the rise of free-to-play models, subscriptions, and in-game purchases, which are not reflected in this revenue calculation.

- **Positive Reviews: How do people feel gaming?**
  - 2010-2017: Positive reviews increased by about 28% YoY, reaching a total of 46 million, suggesting a generally favorable reception to games.
  - 2018-2023: There has been a concerning 35% decrease in positive reviews, dropping to 30 million. This decline may indicate growing dissatisfaction or changing expectations among gamers.
  
- **Ownership: Are gamers still buying games?**
  - Estimated Ownership: The number of people who owns/bought the game.
  - 2010-2017: The number of owners grew at an average annual rate of 31%, totaling 5.17 billion. This shows strong market penetration and consumer engagement.
  - 2018-2023: Ownership totaled 4.03 billion, representing a 20% decrease. The rate of increase has slowed dramatically, from 56% annually in the from 2018-2020 to just 9% after 2021, indicating potential challenges in maintaining growth. 

- **Playtime: Are gamers investing a lot of time in gaming?**
  - 2010-2017: Playtime increased by a robust 46% YoY, demonstrating high engagement and investment from gamers.
  - 2018-2023: While the YoY increase remained strong in the first few years (53%), it slowed to an average of 7% after 2021. This suggests a decline in the intensity of engagement or shifting interests.

#### To Summarize
The gaming market appears to be experiencing a period of transition. While there was a period of rapid growth and strong engagement from 2010 to 2017, recent years show signs of a market adjusting to new realities. The decline in the number of new games and positive reviews, coupled with a significant drop in revenue, suggests that gamers are becoming more discerning and may be looking for higher-quality or more engaging gaming experiences. The slowdown in ownership growth and playtime further reinforces the need for the industry to adapt and innovate to meet evolving consumer expectations or in other words, its look for its **next Good Game**

   
## Recommendations
To recommend we must look at genres, categories, and supported languages. The genre Action led in almost all KPI's but most importantly led in Most Concurrent Users, Owners, Positive Reviews, Revenue and trailed in Playtime. For supported languages it was consistently English, German, French, Spanish-Spain, and Simplified Chinese in the top 5 across all KPI's. For categories, Single-player and Multi-player were T1 and T2 for all the KPIs but we also noticed that it was important for gamers to have full controller support and online PvP/Co-Op. 

The next game should be Action genre and be produced in at least English, German, and French. The defining factor in a game is the category. Instinctively we should go for the consistently highest rated which is Single Player but if we compare it to the second highest rated, MultiPlayer we see some interesting things.
![image](https://github.com/user-attachments/assets/1f9c213b-40ba-4ded-a907-30e282e59c7b)

Action Multiplayer games have more Concurrent Users (15% more), Positive Reviews(13% more) and sold at a higher price (20% more). The biggest difference is the Number of Games. Action Multiplayer games have 70% fewer games meaning that revenue per game, ownership per game, and playtime per game is higher.

#### KPIs per Action Multiplayer game:
- **Conccurent Users** = 795 (vs 210) **276%** higher than Action Single-player
- **Positive Reviews** = 5191 (vs 1407) **268%** higher than Action Single-player
- **Playtime** = 255 hours (vs 105) **143%** higher than Action Single-player
- **Owners** = 525K (vs 162k) **224%** higher than Action Single-player 
- **Revenue** = 6,8M (vs 2,5M) **172%** higher than Action Single-player

**Therefore my final recommendation is to definitely create an Action genre and Multiplayer category game that is supported in English, German, and French languages.**



## Final Dashboard
The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/rodrigo.suarez5210/viz/SteamGamingMarketAnalysis/FinalDash) This dashboard enables users to filter by KPIs, years, and game features.
![image](https://github.com/user-attachments/assets/9e48c4d1-3edc-4637-a5d7-da1d88342a02)




---------------------------------------------------------------------------------------------------------------------------------

# 🧠 How I can improve this project
- Using other data to strengthen this data set such as Twitch, streaming platform, data or gaming metrics such as users and revenue across platforms not limited to only PC. So a more in depth analysis of the gaming industry


Thank you for taking the time to read!
