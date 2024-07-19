# Evaluating Players' performance in their local leagues using Understat
## by Anthony Verdesca

The code helps to evaluate which players are the most influential for a team in their local leagues during the calendar year webscraping data from Understat.com.  

Using Bayer Leverkusen - We will answer the following questions:

1) Who are the 5 most influential players for Goal Events? (Goals + Assists)
2) How is the performance of the 5 most influential players during the season (Month by month and by minutes played)
3) From the player that scores the most: Where does he prefers to shoot and also where does he score the most goals?
4) Who is the best "duo" (Goals and assisted the most)

# Executive Summary
1. [Introduction](https://github.com/DatafromtheBleachers/Understat/new/main?filename=README.md#introduction)
2. [Methodology](https://github.com/DatafromtheBleachers/Understat/new/main?filename=README.md#methodology)
3. [Results](https://github.com/DatafromtheBleachers/Understat/new/main?filename=README.md#results)
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
1) [Webscraping understat using MyBeautifulSoup](https://github.com/DatafromtheBleachers/Understat/blob/main/Codes/Project-Understat-Webscraping.ipynb)
2) [Data Cleaning](https://github.com/DatafromtheBleachers/Understat/blob/main/Codes/Project-Understat-Data-Cleaning.ipynb) 
3) [Data Visualization using barplots, histograms, mplsoccer and heatmaps](https://github.com/DatafromtheBleachers/Understat/blob/main/Project-Understat.ipynb)

First, lets have a look in the format of the data once is scrapped:
![image](https://github.com/user-attachments/assets/9d4b7817-98af-4101-a04d-328861636a37)

# Results

## 1) Who are the 5 most influential players for Goal Events? (Goals + Assists) ##

Leverkusen could not have gotten where they are if it was not due to the contributions of these players. It is interesting to see how accurate Álex Grimaldo was on the scoring ocassions he had, as his Goal Expectations seemed to be around ~6 Goals at most, while he outperformed generating 10! 

![image](https://github.com/user-attachments/assets/1ebb173f-c54f-445d-a3e1-171945490623)

## 2) How is the performance of the 5 most influential players during the season (Month by month and by minutes played) ##

### Month by Month ###

- Boniface was having a very prolific start of the season, but it took him a while to get back into the scoreboard after the winter break.
- Álex Grimaldo provided Assists or Goals during at least once a year. Clearly a strong and dangerous player for the rivals.

![image](https://github.com/user-attachments/assets/a204861d-cc40-4405-baa6-51275fb4fc1b)

## By Minutes Played ##
- Álex Grimaldo is a complete threat during the whole game - He is able to assist or score at any point in the match, same as Florian Wirtz.
- Special attention to the block of time between the 50th and the 70th minute, where a higher number of Boniface and Wirtz's goals/assist came up.

![image](https://github.com/user-attachments/assets/32ca2367-48c3-4da4-85b5-bae564adc1c0)

# 3) From the player that scores the most: Where does he prefers to shoot and also where does he score the most goals? #

## Shot Heatmap ##

- Boniface looks to place himself in areas with near the penalty spot.
![image](https://github.com/user-attachments/assets/1248c285-241f-42c2-a7bd-209082c19640)

## Goal Heatmap ##
- Once again, although more faded, the higher amount of goals is located near the penalty spot. 
![image](https://github.com/user-attachments/assets/05ce126a-ae3e-4fbe-bb15-03d1339c9999)

# 4) Who is the best "duo" (Goals and assisted the most) #
- Victor Boniface(Goals) + Floriant Wirtz(Assists) generated the most goals.
- Second Best: Floriant Wirtz (Assists) + Victor Boniface (Assists). The pair seems to work really well together. 
- This shows that Álex Grimaldo does not assist as much as the other players in the top 5 besides Florian Wirtz.    

![image](https://github.com/user-attachments/assets/525dd60c-9fe1-474f-a57a-ca71981c06cc)

