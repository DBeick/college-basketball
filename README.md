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
This project makes use of the following python libraries:
- jupyter
- pandas
- numpy
- matplotlib

## Purpose<a name="purpose"></a>
Data analysis in sports has become commonplace in the 21st century, with people ranging from casual fans to franchise executives digging into numbers to better understand team performance. The goal of this analysis is to perform a rough look at offensive and defensive performance and their relation to team success in a personal favorite sport of mine, collegiate basketball.

### Questions<a name="questions"></a>
1. Which conferences produce the best offenses and the best defenses each year?
    1. Looking at year-by-year results, which conferences performed the best.
    2. Looking at cumulative results, which conferences performed the best.
2. Is a team with a better offense or a better defense more likely to have the most wins?
    1. Looking at season win totals, prior to postseason tournament.
    2. Looking at performance in the postseason tournament.
3. Is there a bias toward the "Major" conferences (ACC, Big East, Big Ten, Big 12, Pac-12, SEC) in how the postseason tournament is seeded?
    1. Looking at the average power ranking (`BARTHAG`) of major conference teams with a top seed (1-4), and comparing to the average power ranking of teams not in a major conference who earned a top seed.
    2. Comparing the non-major teams, if any, who had a better power ranking than any top-seeded P5 teams by seeing which team performed better in the postseason tournament.


## Notebooks<a name="notebooks"></a>
main.ipynb -- Primary notebook for this project. Reads in the dataset and presents data for analysis of all questions.  
create_dataset.ipynb -- Auxiliary notebook for building the dataset used in this project. It reads in seven independent datasets, makes appropriate changes to the data, such as correcting inconsistencies and creating additional columns, and saves the result in a single large csv.

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

The main findings of this project are explained in this [post](https://medium.com/@dbeickcodes/1e3f8c46a2).

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
* Fixed inconsistency in how teams without a conference affiliation were labeled in the dataset, specifically putting all such teams as being in conference 'Ind' to represent independence from a conference.