# 🎮 AIS-Datathon -- Steam-Games -- Brief Description
My team and I competed in a datathon. The challenge was to come up with a business problem and deliver strategic recommendations. My team decided to work for a hypothetical analytics and consulting firm and offer solutions to a struggling game development company. Here is a brief introduction:

"We are BARS, an analytical and consulting firm, contracted by a game development company seeking to reverse a trend of underperforming titles. We were tasked with a comprehensive industry analysis using a dataset of 85,000 titles from the Steam gaming platform. Our stakeholder, the Head of Development and a passionate gamer, has tasked us with using extensive data to identify their next successful game project!

Financial success is obvious but our stakeholder’s mission is to deliver a game that resonates with gamers–ensuring many people play, many people like it, and significant playtime. BARS will showcase a Tableau dashboard that leverages KPIs such as revenues, positive reviews, estimated ownership, playtime, game count, and user concurrency to optimally identify genre, category, language support, pricing strategy, and potential publisher to ensure commercial and mission success."

My role in the team was Data Analyst. I was in charge of the Python code for initial EDA and then ETL to facilitate building of an interactive Tableau Dashbaord.

# 📦 Technologies:
- Python on Juypter Notebook
- pandas
- Matplotlib
- Numpy
- Counter from collections
- Tableau Dashboard

# 👨‍💻 Methodologies
1. Select KPIs
2. Clean the Data
3. Visualize
4. Make Recommendations

## Select KPIs
Our stakeholder obviously wants financial success but they are more concerned with making a game that "that resonates with gamers–ensuring many people play, many people like it, and significant playtime". Therefore we will be using:
- Number of Games: we want to see if there still is a market for gaming
- Revenue: we want to see if there still is money to be made in gaming
- Ownership: are gamers buying games?
- Concurrent Users: is it a popular game? are alot of gamers playing at the same time?
- Playtime: are gamers investing a lot of time gaming?
- Positive Reviews: how do people feel about gaming?
These KPIs get a macro and micro analysis of the market to determine whether underperformance is because of our stakeholder's game or because the industry is struggling.

## Cleaning the Data
Each row in the data set was a one of the 85k titles. You can see the detailed version of my code uploaded above but to summarize this is what I did:
- Removed 14 unnecessary columns (urls, images, age, median, etc.) that would be useless for industry analysis
- Excluded zero positive & negative reviewed games - games without any reviews does not contribute to our analysis
- Filtered out 10k+ games with estimated ownership ranging from 0 - If games had no owners then game was an utter failure which is not very useful to analyze
- Eliminated outliers with unusually high pricing (above $150) - A hundreth of a percent had games priced that high so it was unecessary to include them
- Removed anomaly of a title with future release date - A future release dated game has no metric to go off of
- Delimited estimated owners on the ‘-’ to have min and max owners - This was crucial in calculating revenue since estimated owners has a range (EX: 0 - 20000)
- Flattened and counted every occasion for genre, language, and category - The most important transformation since genre, lanugage, and category were long lists of strings in string form so I made converted them into true lists, flattened into a single column, and counted every occasion. It was instrumental to our analysis.

## Visualize & Recommendations
If you are interested on the rest of the project here is a link to the Tableau Public Dashboard:
https://public.tableau.com/app/profile/rodrigo.suarez5210/viz/SteamGamingMarketAnalysis/Dashboard1

# 🧠 What I learned
- By far my most important technical learning was the last point on cleaning the data. I discovered how to use ast.literal_eval by importing ast. This is what helped me parse the long list of strings and convert them into true lists to faciliate the counting.
- Learned how to properly clean and the value of exploring data to assertain what is necessary or relevant.
- Implemented my preexisting knowledge of the gaming industry to conduct a rich analysis of this dataset

# 🧠 How I can improve this project
- I want to learn APIs. I think being able to connect to the Steam gaming API would have made this project much stronger
- Using other data to strengthen this data set such as Twitch, streaming platform, data or gaming metrics such as users and revenue across platforms not limited to only PC. So a more in depth analysis of the gaming industry


Thank you for taking the time to read!
