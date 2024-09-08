# League of Legends Early Game Jungle Analysis
 An analysis of League of Legends early-game jungle performance on overall team performance. This analysis was conducted as a final project for UCSD's Summer 2024 offering of DSC80.

## Introduction
## Data Cleaning and Exploratory Data Analysis
#### 1. Filtering out non-catcher/-enchanter support champions.
League of Legends has many classes for their champions, with the support role being especially diverse in both classes and playstyles for many characters. As a result, many other support characters exist outside the ones classified earlier as either a catcher or an enchanter (for example, burst mages and artillery supports exist). However, for the purposes of this exploration, I will be filtering out all rows that are not catchers or enchanters played in the support role.

This now means the following 5 dataframes will only contain data for esports players in the support role who picked either a catcher or an enchanter champion.

## Assessment of Missingness
While `firstblood` has many missing values, my analysis shows that its missingness can be explained by the column itself and another, which in this case is `position`. Rows where `position` is equal to `'team'` include the "missing" first blood statistic, indicating that first bloods are only recorded under the team that achieved them. As a result, I can conclude that the `firstblood` column is NMAR--not missing at random.

## Hypothesis Testing
## Framing a Prediction Problem
## Baseline Model
## Final Model
## Fairness Analysis
