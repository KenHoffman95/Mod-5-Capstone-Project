# Mod-5-Capstone-Project

## Introduction
Whether they've finished in last place or just won the title, NBA teams are always looking to improve their rosters through the draft. Every June, NBA teams hope to find the missing player(s) that will bring them to the next level. Oftentimes, NBA teams wind up dissapointed with their picks and leave their fans wondering why a player was even drafted in the first place. 

## Objective
Create a a model that can accurately predict how rookies will perform as NBA players by classifying them into one of four categories: Bust, Role Player, Starter and All-Star. 

## Dataset
In order to create a model that can accurately predict how rookies will perform as NBA players, I webscraped NBA statistics, College statistics (final year) and additional information from https://www.basketball-reference.com/ and https://www.sports-reference.com/cbb/  for 1,013 NBA players dating back to 1980. I used Number of All Star appearances, PER (Player Efficiency Rating) per Season and NBA Tenure in order to classify the players in the dataset into the one of four categories.  

## Modeling
The Models I tested were:
* KNN
* Logistic Regression
* Decision Tree
* Random Forest
* Voting Classifier
* XGBoost

My best model was XGBoost which had an F1 (weighted) score of .872 and an Accuracy score of .881. These scores were significantly higher than the scores I got with the other models. 

## Model Evaluation
In addition to observing a high F1 and Accuracy score, I wanted to evaluate the XGBoost model by using it to predict on a draft class. Since my dataset only had players that were drafted in 2017 and before, I used the 2018 NBA Draft class to evaluate my model.
All-Star - Trae Young, Shai Gilgeous-Alexander
Starter  - DeAndre Ayton,  

## Next Steps
* Apply model to 2020 Draft Class
* Include draft combine measurements in data
* Create model to predict how basketball players from foreign leagues will perform in the NBA



