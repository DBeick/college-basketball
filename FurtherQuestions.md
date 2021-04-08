# Further Questions
These are questions both within the scope of the data set and outside the scope. Questions may have been sparked by reviewing the data available, reflecting on games I've seen, or conversations with other enthusiasts of the sport of college basketball.

### In Scope
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
        
### Out of Scope
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