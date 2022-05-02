# TCMFINAL2022

### Project Overview
Our final project uses Pandas and Jupyter Notebook to analyze past data and predict future golfer performance on specific courses. Specifically, we focused on projecting the leaderboard for the 2022 Wells Fargo Championship, which begins on May 5th. To start, we looked at the 2022 strokes gained thus far for four different strokes: off the tee, approaching the green, around the green, and putting. Looking at each stroke separately, we sorted the players from best score to worst score, and then used min-max scaling to get each score on a scale from zero (worst) to one (best). We compiled these weighted and adjusted scores for the four statistics into one master table. We then repeated that process for the 2021 statistics. Next, we were interested in finding the contributions of each statistic in final performance at a specific course. To do this, we ran a linear regression to get the coefficients for each stroke. It was important to keep in mine that those coefficients with the lowest number (most negative) would lead to the highest contribution because better golf scores are lower. From there, we put each coefficient over the total to get the contributions of each stroke. Finally, to get a final score, we calculated a weighted average for each player using their scores and the contributions for each stroke. We then sorted the players by this final score, creating a predictive leaderboard. 

**How to interpret our code**
1) Start by viewing "Strokes Gained 2021" and "Strokes Gained 2022." These files weight and min/max scale (between 0-1) all 4 of the major statistics we used for every player on the PGA tour in 2021 and 2022.
2) Then view "Finding Most Informative Course Statistics"(Wells Fargo) or "Masters 21 finding most informative statistic"(Masters) depending on which tournment you are looking for. These files use the previous tournament at the specific course for the file you select to find the statistics that most contribute to success at that course. 
3) Then view "Accessing Course Fit and Projecting Success based on 2021 informative statistics and 2021 play" or "Projecting 2022 Masters Leaderboard" to see who we predict will win each tournament. We do this by computing a weighted average for each player. This is done by using the 4 statistics for the player in the current year as well as last years significance of each statistic at that course. 

**Back testing**
We also ran a back test on the 2022 Masters tournament using the same process. Our results show significant predictive accuracy even while not accounting for course history for specific players. Thus, we have confidence that our model is a strong predictor for the Wells Fargo Championship on May 5th.


**Our models projected Masters 2022 top 20:**
Russell Henley,
Justin Thomas,
Taylor Gooch,
Will Zalatoris,
Daniel Berger,
Joaquin Niemann,
Luke List,
Cameron Smith,
Matt Fitzpatrick,
Hideki Matsuyama,
Sam Burns,
Tome Hoge,
Scottie Scheffler,
Sungjae Im,
Shane Lowry,
Xander Schauffele,
Jordan Spieth,
Patrick Cantlay,
Harold Varner III,
Tommy Fleetwood

**Actual 2022 Masters top 20**
Scottie Scheffler,
Rory Mcilroy,
Shane Lowry,
Cameron Smith,
Colin Morikawa,
Will Zalatoris,
Corey Conners,
Justin Thomas,
Sungjae Im,
Cameron Champ,
Charles Schwartzel,
Dustin Johnson,
Danny Willet,
Kevin Na,
Matthew Fitzpatrick,
M.W. Lee,
Harry Higgs,
Lee Westwood,
Taylor Gooch,
Hideki Matsuyama,
Tommy Fleetwood,
Jason Kokrak,
*22 names to include ties

**Correct 2022 Masters Top 20 Predictions**,
**10/22**,
**45% predictive accuracy**
