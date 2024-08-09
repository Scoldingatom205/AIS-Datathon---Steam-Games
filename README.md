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
- Removed data prior to 2014 due to very little amount of games
- Cleaned estimated owners on the hyphen to have min and max owners to calculate revenue
- Flattened and counted every occasion for genre, language, and category - The most important transformation since genre, lanugage, and category were long lists of strings in string form so I made converted them into true lists, flattened into a single column, and counted every occasion.

## Insights Summary
Underperformance for our stakeholder can mean a number of things so we will use KPI's to answer a few quetions. Although we have historical data we will only be using the past 5 years to answer these questions and uncover trends using a Tableau dashboard.

- **Number of Games: Is there still is a market for gaming?**
  - Number of Games: The number of games.
    
- **Revenue: Is there still is money to be made in gaming**
  - Revenues: Multiplied estimated owners with price to get MIN and MAX revenues.
    
- **Ownership: Are gamers still buying games?**
  - Estimated Ownership: The number of people who owns/bought the game.
    
- **Concurrent Users: Are alot of gamers playing at the same time?**
  - User Concurrency: The highest number of users who are simultaneously playing.
    
- **Playtime: Are gamers investing a lot of time in gaming?**
  - Playtime: How long on average did users play the game.
    
- **Positive Reviews: How do people feel gaming?**
  - Positive Reviews: Indicates positive reception of game.
  -  
## Recommendations


## Final Dashboard
The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/rodrigo.suarez5210/viz/SteamGamingMarketAnalysis/FinalDash) This dashboard enables users to filter by KPIs, years, and game features.
![image](https://github.com/user-attachments/assets/9e48c4d1-3edc-4637-a5d7-da1d88342a02)




---------------------------------------------------------------------------------------------------------------------------------



# 🧠 What I learned
- By far my most important technical learning was the last point on cleaning the data. I discovered how to use ast.literal_eval by importing ast. This is what helped me parse the long list of strings and convert them into true lists to faciliate the counting.
- Learned how to properly clean and the value of exploring data to assertain what is necessary or relevant.
- Implemented my preexisting knowledge of the gaming industry to conduct a rich analysis of this dataset

# 🧠 How I can improve this project
- I want to learn APIs. I think being able to connect to the Steam gaming API would have made this project much stronger
- Using other data to strengthen this data set such as Twitch, streaming platform, data or gaming metrics such as users and revenue across platforms not limited to only PC. So a more in depth analysis of the gaming industry


Thank you for taking the time to read!
