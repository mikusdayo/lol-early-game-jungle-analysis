# League of Legends Early Game Jungle Analysis
 An analysis of League of Legends early-game jungle performance on overall team performance. This analysis was conducted as a final project for UCSD's Summer 2024 offering of DSC80.

## Introduction
#### What is League of Legends?
League of Legends (LoL) is a free-to-play, MOBA (multiplayer online battle arena) game in which two teams of 5 players fight to destroy their enemy's base. It is a dynamic game with several moving parts, and with games lasting up to 45 minutes, many elements can influence a team's victory or loss. In this project, I aim to explore several questions concerning aspects that may affect a game's outcome as an avid LoL player.
#### Quick Definitions
- **champion:** any playable character in LoL
- **lane:** a division of the LoL map where players earn gold and fight their respective opponent from the enemy team; corresponds to players' in-game roles; there are 3 lanes in a normal game of LoL
    - *laning* is the term corresponding to roles primarily played in the 3 lanes of the map, characterized by farming minion kills for gold and short solo battles against the enemy *laner*
    - a *laner* is any one of the 4/5 players in *roles* other than *jungle*, named after the lanes of the map they primarily play within
- **role:** any one of five available roles assumed by players in-game:
    - *top:* a solo, laning role played in the top-most lane of the map
    - *mid:* a solo, laning role played in the middle lane of the map
    - *bot:* a duo, laning role played in the bottom-most lane of the map; 1/2 of the pair played in this lane, their primary role is to earn as much gold and enemy kills as possible with the help of their support
    - *support*: a duo, support role played in the bottom-most lane of the map; 1/2 of the pair played in this lane, their primary role is to support their bot *laner* and help them earn gold and get enemy kills
    - *jungle:* a solo role played in the *jungle* regions of the map; their primary goal is to earn gold, claim objectives in the form of team-wide buffs, and assist their laners in getting enemy kills and map control
## Data Cleaning and Exploratory Data Analysis
### Brainstorming
Before beginning to conduct any analysis, I brainstormed a few possible questions to explore based on my own curiosities about the game.
##### Brainstorm questions:
1. Which side of the map (red or blue) is "easier" to play on?
2. Which ADC is the easiest to play over the last few seasons?
3. Are catcher supports or engage supports more likely to win a game?
##### Question picked to explore:
Are catcher supports or engage supports more likely to win a game?
### Prepping for analysis
To begin my analysis, I started by loading in my data from Oracle Elixir containing the last 5 years' worth of LoL Esports data and filtering out relevant columns.
#### Filtering out non-catcher/-enchanter support champions.
League of Legends has many classes for their champions, with the support role being especially diverse in both classes and playstyles for many characters. As a result, many other support characters exist outside the ones classified earlier as either a catcher or an enchanter (for example, burst mages and artillery supports exist). However, for the purposes of this exploration, I will be filtering out all rows that are not catchers or enchanters played in the support role.

This now means the following 5 dataframes will only contain data for esports players in the support role who picked either a catcher or an enchanter champion.
#### Filtering out irrelevant columns.
To save time in following data cleaning steps, I decided to only keep relevant columns, which were `year`, `patch`, `side`, `position`, `playername`, `teamname`, `champion`, `result`, `kills`, `deaths`, and `assists`, `visionscore`, `totalgold`, and `total cs`.
## Assessment of Missingness
While `firstblood` has many missing values, my analysis shows that its missingness can be explained by the column itself and another, which in this case is `position`. Rows where `position` is equal to `'team'` include the "missing" first blood statistic, indicating that first bloods are only recorded under the team that achieved them. As a result, I can conclude that the `firstblood` column is NMAR--not missing at random.

## Hypothesis Testing
## Framing a Prediction Problem
## Baseline Model
## Final Model
## Fairness Analysis
