# Steam Games Analysis - Project Overview
1 of 10 teams to compete in the Inauguraul Spring 2023 Association of Information Systems (AIS) @ CSULB Datathon in April 2024.
My team took 1st place!!

## Background
Teams were assigned randomly based on skillset information given to AIS through a survey before the datathon. The challenge was to come up with a business problem and deliver strategic recommendations in front of a panel of judges. 

My team approach was to become a hypothetical analytics and consulting firm, BARS, and offer solutions to a struggling game development company who is seeking to reverse a trend of underperforming titles. More specifically the founder of the company is a passionate gamer and is tasking us with using extensive data to identify their next successful game project according to financial success but more important, a well loved game by the gaming community.

## Dataset Structure

## Insights Summary
BARS will showcase a Tableau dashboard that leverages KPIs:
- **Revenues**
- **Positive Reviews**
- **Estimated Ownership:**
- **Playtime**
- **Game Count**
- **User Concurrency**

- - Number of Games: we want to see if there still is a market for gaming
- Revenue: we want to see if there still is money to be made in gaming
- Ownership: are gamers buying games?
- Concurrent Users: is it a popular game? are alot of gamers playing at the same time?
- Playtime: are gamers investing a lot of time gaming?
- Positive Reviews: how do people feel about gaming?

## Recommendations


## Final Dashboard
The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/rodrigo.suarez5210/viz/SteamGamingMarketAnalysis/Dashboard1). This dashboard enables users to filter by KPIs, years, and game features.



---------------------------------------------------------------------------------------------------------------------------------
# 👨‍💻 Methodologies
1. Select KPIs
2. Clean the Data
3. Visualize
4. Make Recommendations

## Cleaning the Data
Each row in the data set was a one of the 85k titles. You can see the detailed version of my code uploaded above but to summarize this is what I did:
- Removed 14 unnecessary columns (urls, images, age, median, etc.) that would be useless for industry analysis
- Excluded zero positive & negative reviewed games - games without any reviews does not contribute to our analysis
- Filtered out 10k+ games with estimated ownership ranging from 0 - If games had no owners then game was an utter failure which is not very useful to analyze
- Eliminated outliers with unusually high pricing (above $150) - A hundreth of a percent had games priced that high so it was unecessary to include them
- Removed anomaly of a title with future release date - A future release dated game has no metric to go off of
- Delimited estimated owners on the ‘-’ to have min and max owners - This was crucial in calculating revenue since estimated owners has a range (EX: 0 - 20000)
- Flattened and counted every occasion for genre, language, and category - The most important transformation since genre, lanugage, and category were long lists of strings in string form so I made converted them into true lists, flattened into a single column, and counted every occasion. It was instrumental to our analysis.

# 📦 Technologies:
- Python on Juypter Notebook
- pandas
- Matplotlib
- Numpy
- Counter from collections
- Tableau Dashboard


# 🧠 What I learned
- By far my most important technical learning was the last point on cleaning the data. I discovered how to use ast.literal_eval by importing ast. This is what helped me parse the long list of strings and convert them into true lists to faciliate the counting.
- Learned how to properly clean and the value of exploring data to assertain what is necessary or relevant.
- Implemented my preexisting knowledge of the gaming industry to conduct a rich analysis of this dataset

# 🧠 How I can improve this project
- I want to learn APIs. I think being able to connect to the Steam gaming API would have made this project much stronger
- Using other data to strengthen this data set such as Twitch, streaming platform, data or gaming metrics such as users and revenue across platforms not limited to only PC. So a more in depth analysis of the gaming industry


Thank you for taking the time to read!
