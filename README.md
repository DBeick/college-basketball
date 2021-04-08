# college-basketball
Home project for analysis of men's basketball performance in 2013-19 seasons

#### Table of Contents

1. [Installation](#installation)
2. [Purpose](#purpose)
    1. [Questions](#questions)
    2. [Other Questions outside this Analysis](#out_of_scope)
3. [Notebooks](#notebooks)
4. [Data](#data)
5. [Results](#results)
6. [Liscensing, Authors, and Acknowledgments](#liscensing)
    1. [Acknowledgments](#acknowledgments)
    2. [Adjustments](#adjustments)

## Installation<a name="installation"></a>

## Purpose<a name="purpose"></a>
Data analysis in sports has become commonplace in the 21st century, with people ranging from casual fans to franchise executives digging into numbers to better understand team performance. The goal of this analysis is to perform a rough look at offensive and defensive performance and their relation to team success in a personal favorite sport of mine, collegiate basketball.

### Questions<a name="questions"></a>
1. Does a team's superiority in its conference correlate to postseason success?
Superiority is determined by how many standard deviations the team's rating is above the mean of its conference in these categories:
    * Win rate
    * Offensive efficiency
    * Defensive efficiency
    * Net field goal percentage

2. In general, do defensively-minded teams perform better or worse in any statistically significant way compared to offensively-minded teams?
    * Defensive statistics:
        * Defensive Efficiency
        * Field goal percentage allowed
        * Turnover percentage committed
        * Defensive rebound rate
        * Free throw rate allowed
        * Adjusted tempo (at lower rates)
    * Offensive statistics:
        * Offensive Efficiency
        * Field goal percentage
        * Turnover percentage allowed
        * Offensive rebound rate
        * Free throw rate
        * Adjusted tempo (at higher rates)

3. What category of statistic, if any, has the strongest correlation to postseason performance?
    * Power rating
    * Offensive efficiency
    * Defensive efficiency
    * Combined efficiency
    * Field goal percentage rate
    * Combined rebound rate
    * Net turnover rate

4. Does a combination of possessions and field goal shooting percentage strongly, weakly, or not at all correlate to win rate and/or postseason success?
One specific point to investigate revolves around a seemingly obvious concept: the team who is able to score more points wins more often. The most points can simply come from having more possessions than the opponent AND scoring more efficiently (better shooting rate) than the opponent. Do teams that both create more possessions and convert more possessions into points tend to perform the best in the championship tournament?
    * Varibles related to possessions:
        * Rebound rate
        * Turnover rate
        * Tempo
    * Variables related to scoring efficiency:
        * Effective field goal percentage


### Other questions outside this analysis<a name="out_of_scope"></a>
This dataset, while robust, represents only a portion of the data surrounding each team. Further questions that would be interesting to investigate, provided more data, are:
1. How does a team's dependence on its starting five players correlate to postseason success?
The quick-succession championship tournament is famously exhausting for players, with teams playing in two out of three days on three successive weekends. Do teams that depend on a small number of players, and therefore may be more likely to see the effects of fatigue in such an intense tournament, show any more or less success in the tournament?
    * To answer this question would require data on minutes played per player per team.

2. How do injuries affect team performance in the championship tournament?
The loss of an important player due to injury could be a significant factor in predicting the success of a team at any time in the season. Does a team suffering such an injury immediately before or during the tournament, therefore having little to no time to practice with a different strategy, have any more or less success in the tournament?
    * To answer this question would require data on minutes played per player per team and whether a given player missed some or all of a game due to injury.

3. How does game-by-game 'momentum' play out in the postseason tournament?
Momentum is a popular concept in sports, wherein a team that is performing well in-game will continue to perform well. Similarly, a team may have game-by-game momentum, where a winning streak may be more likely to continue the longer it goes on (or at least, some folks may like to think so). Does a team that comes into the postseason riding a winning streak tend to perform better than one that does not have a notable active win streak?
    * To answer this question would require data on when wins and losses occurred for a team, and for further insight it would be helpful to have data on performance in the team's conference championship tournament.

## Notebooks<a name="notebooks"></a>

## Data<a name="data"></a>

### Content<a name="content"></a>
Data from the 2013, 2014, 2015, 2016, 2017, 2018, and 2019 Division I college basketball seasons.

### Variables<a name="variables"></a>
`TEAM`: The Division I college basketball school

`CONF`: The Athletic Conference in which the school participates  
    `A10` = Atlantic 10,  
    `ACC` = Atlantic Coast Conference,  
    `AE` = America East,  
    `Amer` = American,  
    `ASun` = ASUN,  
    `B10` = Big Ten,  
    `B12` = Big 12,  
    `BE` = Big East,  
    `BSky` = Big Sky,  
    `BSth` = Big South,  
    `BW` = Big West,  
    `CAA` = Colonial Athletic Association,  
    `CUSA` = Conference USA,  
    `Horz` = Horizon League,  
    `Ivy` = Ivy League,  
    `MAAC` = Metro Atlantic Athletic Conference,  
    `MAC` = Mid-American Conference,  
    `MEAC` = Mid-Eastern Athletic Conference,  
    `MVC` = Missouri Valley Conference,  
    `MWC` = Mountain West,  
    `NEC` = Northeast Conference,  
    `OVC` = Ohio Valley Conference,  
    `P12` = Pac-12,  
    `Pat` = Patriot League,  
    `SB` = Sun Belt,  
    `SC` = Southern Conference,  
    `SEC` = South Eastern Conference,  
    `Slnd` = Southland Conference,  
    `Sum` = Summit League,  
    `SWAC` = Southwestern Athletic Conference,  
    `WAC` = Western Athletic Conference,  
    `WCC` = West Coast Conference

`G`: Number of games played

`W`: Number of games won

`PRE_PC`: Percentage of games won prior to postseason tournament

`POST_PC`: Percentage of games won following postseason tournament

`ADJOE`: Adjusted Offensive Efficiency (An estimate of the offensive efficiency (points scored per 100 possessions) a team would have against the average Division I defense)

`ADJDE`: Adjusted Defensive Efficiency (An estimate of the defensive efficiency (points allowed per 100 possessions) a team would have against the average Division I offense)

`BARTHAG`: Power Rating (Chance of beating an average Division I team)

`EFG_O`: Effective Field Goal Percentage Shot

`EFG_D`: Effective Field Goal Percentage Allowed

`TOR`: Turnover Percentage Allowed (Turnover Rate)

`TORD`: Turnover Percentage Committed (Steal Rate)

`ORB`: Offensive Rebound Rate

`DRB`: Defensive Rebound Rate

`FTR`: Free Throw Rate (How often the given team shoots Free Throws)

`FTRD`: Free Throw Rate Allowed

`2P_O`: Two-Point Shooting Percentage

`2P_D`: Two-Point Shooting Percentage Allowed

`3P_O`: Three-Point Shooting Percentage

`3P_D`: Three-Point Shooting Percentage Allowed

`ADJ_T`: Adjusted Tempo (An estimate of the tempo (possessions per 40 minutes) a team would have against the team that wants to play at an average Division I tempo)

`WAB`: Wins Above Bubble (The bubble refers to the cut off between making the NCAA March Madness Tournament and not making it)

`POSTSEASON`: Round where the given team was eliminated or where their season ended  
    `R68` = First Four,  
    `R64` = Round of 64,  
    `R32` = Round of 32,  
    `S16` = Sweet Sixteen,  
    `E8` = Elite Eight,  
    `F4` = Final Four,  
    `2ND` = Runner-up,  
    `Champion` = Winner of the national championship game for that given year

`SEED`: Seed in the NCAA Men's Division I Basketball Tournament

`PFPC`: Performance Percentile (Percent of total teams that season whom the team outperformed, based on postseason finish, i.e. postseason champion bested all other teams, so it ranks 1.0, while a team finishing in the "Elite Eight" was better than all teams but eight, so it ranks roughly around 0.97

`YEAR`: Season

## Results<a name="results"></a>

The main findings of this project are explained in this [post].

## Liscensing, Authors, and Acknowledgements<a name="liscensing"></a>
### Acknowledgments<a name="acknowledgments"></a>
This dataset was borrowed from Kaggle.  
Name: College Basketball Dataset  
URL: https://www.kaggle.com/andrewsundberg/college-basketball-dataset  
Creator: Andrew Sundberg  
Creator URL: https://www.kaggle.com/andrewsundberg  
Accessed: April 2, 2021  

#### Adjustments<a name="adjustments"></a>
I made a these adjustments to the data to perform better analysis:
* Combined the season-by-season sets rather than use the pre-combined set, due to missing data in the `Postseason` column
* Added columns denoting win percentage both before and after postseason tournament
* Added column denoting performance percentile
* Inverted the column `DRB` (100 - value) to properly reflect Defensive Rebound Rate, instead of the original Offensive Rebound Rate Allowed
