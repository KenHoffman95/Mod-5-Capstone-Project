# Mod-5-Capstone-Project

## Introduction
Whether they've finished in last place or just won the title, NBA teams are always looking to improve their rosters through the draft. Every June, NBA teams hope to find the missing player(s) that will bring them to the next level. Oftentimes, NBA teams wind up dissapointed with their picks and leave their fans wondering why a player was even drafted in the first place. 

## Objective
Create a a model that can accurately predict how rookies will perform as NBA players by classifying them into one of four categories: Bust, Role Player, Starter and All-Star. 

## Dataset
In order to create a model that can accurately predict how rookies will perform as NBA players, I webscraped NBA statistics, College statistics (final year) and additional information from https://www.basketball-reference.com/ and https://www.sports-reference.com/cbb/  for 1,013 NBA players dating back to 1980.

## Modeling
The Models I tested were:
* KNN
* Logistic Regression
* Decision Tree
* Random Forest
* Voting Classifier
* XGBoost

My best model was XGBoost which had an F1 (weighted) score of .872 and an Accuracy score of .881. These scores were significantly higher than the scores I got for the other models. 



