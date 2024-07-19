# Evaluating Players' performance using Understat
## by Anthony Verdesca

The code helps to evaluate which players are the most influential for a team during the calendar year webscraping data from Understat.com.  

Using Bayer Leverkusen - We will answer the following questions:

1) Who are the 5 most influential players for Goal Events? (Goals + Assists)
2) How is the performance of the 5 most influential players during the season (Month by month and by minutes played)
3) From the player that scores the most: Where does he prefers to shoot and also where does he score the most goals?
4) Who is the best "duo" (Goals and assisted the most)

# Executive Summary
1. [Introduction](https://github.com/DatafromtheBleachers/Understat/new/main?filename=README.md#introduction)
2. [Methodology](https://github.com/DatafromtheBleachers/Understat/new/main?filename=README.md#methodology)
3. Results
4. Upgrates

# Introduction
Understat.com is a website that provides detailed Expected Goals (xG) statistics for teams and players from the top European football leagues.
The goal of Understat.com was to create the most precise method for shot quality evaluation. For this case, they trained neural network prediction algorithms with a large dataset.
On Understat.com, you will find detailed xG statistics for the top European leagues, including the English Premier League, La Liga, Bundesliga, Serie A, and others.

![understat](https://github.com/user-attachments/assets/ee79eb93-3026-466d-9d33-33542fe33d18)
![understat](https://github.com/user-attachments/assets/98fad07f-26ce-4f3f-805c-8f69c02f8ac8)

Data is extracted as a collection of shooting events by teams and by players. 

# Methodology

The process consisted in 3 stages:
1) Webscraping understat using MyBeautifulSoup
2) Data Cleaning 
3) Data Visualization using barplots, histograms, mplsoccer and heatmaps

First, lets have a look in the format of the data once is scrapped:
![image](https://github.com/user-attachments/assets/9d4b7817-98af-4101-a04d-328861636a37)

## A brief explanation of each column: ##

**date**: The date of the shot event.
**minute**: The minute of the game where the shot event happened.
**MatchID**: ID of the match that was played.
**x**: x coordinate on the soccer field.
**y**: y coordinate on the soccer field.
**xG**: Goal Expectation - A value of the odds of a shoot to end up as a goal.
**result**: Whether the shot event ended up as a Goal, Missed, Blocked, Saved or Own Goal.
**team**: Team that is generating the shot event.
**Home_Away**: If **team** was playing at home or was a visitor.
**player**: Player generating the shot event.
**player_assisted**: Player that provided the assist. If **player** generate its own shot event, then this will be "NaN".
**Shottype**: Type of shot: Left foot, Right foot or a header.
