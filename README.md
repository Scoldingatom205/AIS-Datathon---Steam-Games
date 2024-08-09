# Steam Games Analysis - Project Overview
1 of 10 teams to compete in the Inauguraul Spring 2023 Association of Information Systems (AIS) @ CSULB Datathon in April 2024.
My team took 1st place!!

## Background
Teams were assigned randomly based on a survey before the datathon. The challenge was to identify a business problem and provide strategic recommendations. My team, BARS, acted as an analytics and consulting firm to help a game development company find their next successful title, focusing on both financial success and gaming community approval.

## Dataset Structure
The dataset initially had 85k titles (one per row) with 38 columns, which was reduced to 63k titles with 21 columns after preprocessing. 

### Preprocessing
- Removed 17 uninformative columns (e.g., URLs, images)
- Excluded games with zero reviews or zero owners
- Filtered out games with outlier pricing (above $150) - 0.001% had games priced that high
- Removed future release dates and data prior to 2010 due to low amount of games
- Cleaned estimated owners on the hyphen to have min and max owners to calculate revenue
- Flattened and counted every occasion for genre, language, and category - Turned long lists of strings in individual string form hashed to AppID.
  
## Insights Summary
Underperformance for our stakeholder can mean a number of things so we will use KPI's to answer  6 key quetions about the gaming market. We believe using the past 5 years for recommendations would be more than using all-time data for the launch of a new game.

- **Number of Games: Is there still is a market for gaming?**
  - 2010-2017: Nearly doubled annually, showing market expansion.
  - 2018-2023: Total number doubled, but saw a 15% decrease in new releases since 2022, indicating possible market saturation.
    
- **Revenue: Is there still is money to be made in gaming?**
  - Revenues = Estimated owners multiplied with price
  - 2010-2017: Grew at an average annual rate of 35% despite a 7% annual decrease in game prices. This indicates strong market demand.
  - 2018-2023: Initially more than doubled but dropped 40% since 2022, likely due to the rise of free-to-play models, subscriptions, and in-game purchases.

- **Positive Reviews: How do people feel gaming?**
  - 2010-2017: Positive reviews increased by about 28% YoY, reaching a total of 46 million, suggesting a generally favorable reception to games.
  - 2018-2023: A concerning decreased by 35% to 30 million, indicating potential dissatisfaction.
  
- **Ownership: Are gamers still buying games?**
  - Estimated Ownership: The number of people who owns/bought the game.
  - 2010-2017: Grew 31% annually, reaching 5.17 billion.
  - 2018-2023: Dropped to 4.03 billion (20% decrease) with a slowed growth rate from 56% to 9% after 2021.
    
- **Playtime: Are gamers investing a lot of time in gaming?**
  - 2010-2017: Playtime increased by a robust 46% YoY, demonstrating high engagement and investment from gamers.
  - 2018-2023: While the YoY increase remained strong in the first few years (53%), it slowed to an average of 7% after 2021. This suggests a decline in the intensity of engagement or shifting interests.

#### To Summarize
The gaming market is shifting. The rapid growth from 2010 to 2017 has slowed, with declines in new games, positive reviews, and revenue. Gamers appear to be seeking higher-quality experiences, which suggests gamers are looking for its **Next Good Game**

   
## Recommendations
The genre Action led in most KPI's most importantly in Concurrent Users, Owners, Positive Reviews, Revenue. For supported languages it was consistently English, German, French, top 3 across all KPI's. For categories, Single-player and Multi-player were T1 and T2 for all the KPIs.

An interesting obvservation was found that yes the next game should be Action genre and be produced in at least English, German, and French. bust should it be Single Player which led every time or another category. If we compare it to the second highest rated category, MultiPlayer we see that it has 70% fewer games meaning that KPIs per game are higher. 

![image](https://github.com/user-attachments/assets/1f9c213b-40ba-4ded-a907-30e282e59c7b)

#### KPIs per Action Multiplayer game vs Action Single Player:
- **Conccurent Users**: 795 (276% higher)
- **Positive Reviews:**: 5,191 (268% higher)
- **Playtime:**: 255 hours (143% higher)
- **Owners:**: 525K (224% higher)
- **Revenue:**: 6.8M (172% higher)

**Final recommendation: Develop an Action genre, Multiplayer game, supported in English, German, and French.**

## Supplementary Insights from Secondary Data
-  **Leverage Esports and Twitch Popularity:** The top games in the Esports scene and on Twitch are predominantly multiplayer action games. This popularity underscores the potential for high engagement and visibility. Sources: [Backlinko](https://backlinko.com/twitch-users#most-popular-games), [ESCharts](https://escharts.com/top-games?order=peak).
- **Expand Language Support:** Supporting multiple languages such as English, French, German, and Spanish aligns with the major demographics of Twitch users in the USA, Germany, and France. This broader language support will enhance the game's accessibility and appeal. [Source: Statista.](https://www.statista.com/statistics/511558/twitch-traffic-by-country/)
- **Adopt a Freemium Revenue Model:**  Implementing a 'freemium' model can drive substantial revenue, as evidenced by Fortnite’s $20 billion success. This model offers the game for free while generating income through in-game purchases. [Source: Game World Observer](https://gameworldobserver.com/2023/11/21/fortnite-revenue-20-billion-epic-games-donald-mustard).

## Final Dashboard
The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/rodrigo.suarez5210/viz/SteamGamingMarketAnalysis/FinalDash) This dashboard enables users to filter by KPIs, years, and game features. Also look through the tooltips as they have a bunch of information on them!

![image](https://github.com/user-attachments/assets/9e48c4d1-3edc-4637-a5d7-da1d88342a02)



Thank you for taking the time to read!
