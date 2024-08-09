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
Underperformance for our stakeholder can mean a number of things so we will use KPI's to answer a few quetions. Although we have historical data we will only be using the past 5 years to answer these questions and uncover trends using a Tableau dashboard.

- **Number of Games: Is there still is a market for gaming?**
  - Since 2018 however, there is a small decline but there was a resurgence at the end of 2023. 
    
- **Revenue: Is there still is money to be made in gaming**
  - Revenues = Estimated owners multiplied with price
  - Since 2018, there is a considerable decline in revenue.
    - However games that are free will therefore have zero revenue leaving out data to be inconclusive in answering this question due to games (priced and free) that make hundreds of millions on subscription models, microtransactions, and in-game currency.

- **Positive Reviews: How do people feel gaming?**
  - Since 2018, people seem to hate games more and more YoY with a noticeable dip in 2022. That tells us that people are unsatisfied with recent games.
  - T5 Genres: Action, Indie, Adventure, RPG, Simulations
  - T5 Categories: Single Player, Multiplayer, Steam Cloud, Steam Trading Cards, Full Controller Support
  - T5 Languages: English, French, German, Simplified Chinese, Russian
  
- **Ownership: Are gamers still buying games?**
  - Estimated Ownership: The number of people who owns/bought the game.
  - Steep decline again! Due to unsatisfaction of games gathered from positive reviews, it seems gamers are not buying new games as much.
  - T5 Genres: Action, Indie, Adventure, RPG, Casual
  - T5 Categories: Single Player, Multiplayer, Steam Cloud, PvP, Online PvP
  - T5 Languages: English, French, German, Simplified Chinese, Spanish-Spain

- **Playtime: Are gamers investing a lot of time in gaming?**
  - Yes but there is a sharp decline.
  - T5 Genres: Indie, Adventure, Action, Simulation, RPG
  - T5 Categories: Single Player, Steam Cloud,, Multiplayer, Steam Trading Cards, Full Controller Support
  - T5 Languages: English, Simplified Chinese, German, French, Spanish-Spain

**To Summarize**
Games are experiencing a decline is positive reviews, number of owerns, number of games released, and average playtime. A telling KPI is average playtime as we can analyze where users are spending their time. It seems like Indie Genre, Single-Player category, and games in English and German. In other words, due to a decline in max owners  in----------
    

   
## Recommendations


## Final Dashboard
The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/rodrigo.suarez5210/viz/SteamGamingMarketAnalysis/FinalDash) This dashboard enables users to filter by KPIs, years, and game features.
![image](https://github.com/user-attachments/assets/9e48c4d1-3edc-4637-a5d7-da1d88342a02)




---------------------------------------------------------------------------------------------------------------------------------

# 🧠 How I can improve this project
- Using other data to strengthen this data set such as Twitch, streaming platform, data or gaming metrics such as users and revenue across platforms not limited to only PC. So a more in depth analysis of the gaming industry


Thank you for taking the time to read!
