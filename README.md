##Forecasting the 2015 All-NBA teams
Data mining techniques used to forecast who will be voted onto the 2015 All-NBA basketball teams.


##Intro:
At the end of every NBA season teams, players and coaches are recognized for the performance through the NBA season. 
Outside of the 12 annual awards given at the end of year, players' are anointed  to All pro teams(All NBA, All Rookie and All Defensive Teams) on the basis of their individual performance.
Its an honor bestowed to the "Best players in their respective positions. Three-five man teams are voted on by sportswriters and broadcasters across North America.

Player receive five points for the first team, three points for the second team, and one point for the third.
The five players with the highest total scores make the first team, then next five and so forth. 

To my knowledge, I don’t believe there is some methodology to the way voters vote for players to receive honors.
All the award is supposed to reflect the best players in their respective positions, this is not always true. Sometimes voters, vote on players by merit, not on individual performance or how one players performance helped their team. 

Notes: 
Ties are possible(but has only happen once)
From 1946 - 1955, players were selected without regard to position.  However starting in 1956, each team consisted of two forwards, one center and two guards. 

##Data Mining Meets Basketball:
###Problem

Given the availability of historical basketball data, can we predict which players will be voted into each team by the end of the 2014-15 season? 
	
Hypothesis statement:
		Null: there isn’t a relationship between the NBA statistics and whether or not an NBA player is voted onto the All-NBA team. 
		Alternative: There is a relationship between statistical performance and making the team.
	
### Data:
*Description of your data set and how it was obtained:

NBA Stats for every player who played in the NBA from 1950 - 2015

Each variable is the accumulated average for that particular stat in a given season.  

|column_name|name|legend_name|table_name|
| ----------|:-----:|:-------------:| -----:|
|player|Player|PLAYER|Per Game Player Stats|
|pos|Position|POS|Per Game Player Stats|
|age|Age|AGE|Per Game Player Stats
|bref_team_id|Team ID|BREF_TEAM_ID|Per Game Player Stats|	
|g|Games Played|G|Per Game Player Stats|
|gs|Games Started|GS|Per Game Player Stats|
|mp|Minutes Per Game|MP|Per Game Player Stats|
|fg|Field Goals Made Per Game|FG|Per Game Player Stats|
|fga|Field Goal Attempts Per Game|FGA|Per Game Player Stats|
|fg.|Field Goal %|FG%|Per Game Player Stats|
|x3p|3PT Shots Made Per Game|3PM|Per Game Player Stats|
|x3pa|3PT Shot Attempts Per Game|3PA|Per Game Player Stats|
|x3p.|3PT %|3P%|Per Game Player Stats|
|x2p|2PT Shots Made Per Game|2PM|Per Game Player Stats|
|x2pa|2PT Shot Attemps Per Game|2PA|Per Game Player Stats|
|x2p_|2PT Shot %|2P%|Per Game Player Stats|
|ft|Free Throws Made Per Game|FT|Per Game Player Stats|
|fta|Free Throw Attempts Per Game|FTA|Per Game Player Stats|
|ft_|Free Throw %|FT%|Per Game Player Stats|
|orb|Offensive Rebounds Per Game|ORB|Per Game Player Stats|
|drb|Defensive Rebounds Per Game|DRB|Per Game Player Stats|
|trb|Total Rebounds Per Game|TRB|Per Game Player Stats|
|ast|Assists Per Game|AST|Per Game Player Stats|
|stl|Steals Per Game|STL|Per Game Player Stats|
|blk|Blocks Per Game|BLK|Per Game Player Stats|
|tov|Turnovers Per Game|TOV|Per Game Player Stats|
|pf|Personal Fouls Per Game|PF|Per Game Player Stats|
|pts|Points Per Game|PPG|Per Game Player Stats|
|PER|Player Effiecieny Rating||Per Game Player Stats|
|TS%|True Shooting Percentage||Per Game Player Stats|
|3PAr|Three Point Attempt Rate||Per Game Player Stats|
|FTr|Free Throw Attempt Rate||Per Game Player Stats|
|TRB%|Offensive Rebound Percentage||Per Game Player Stats|
|AST%|Assist Percentage||Per Game Player Stats|
|STL%|Steal percentage||Per Game Player Stats|
|BLK%|Block Percentage||Per Game Player Stats|
|TOV%|Turnover Percentage||Per Game Player Stats|
|USG%|Usage Percentage||Per Game Player Stats|
|OWS|Offensive Win Shares||Per Game Player Stats|
|DWS|Defensive Wins Shares ||Per Game Player Stats|
|WS|Win Shares||Per Game Player Stats|
|WS/48|Wins per 48 mins||Per Game Player Stats|
|OBPM|Offensive Box Plus/Minus||Per Game Player Stats|
|DBPM|Defensive Box Plus/Minus||Per Game Player Stats|
|BPM|Box Plus/Minus||Per Game Player Stats|
|VORP|Value Over Replacement Player||Per Game Player Stats|

**Pulled data from here: https://github.com/abresler/abresler.github.io/tree/master/data/NBA/player_data/all_player_per_game

But data is originally scraped from: http://www.basketball-reference.com
