# Mod-5-Capstone-Project

## Introduction
Whether they've finished in last place or just won the title, NBA teams are always looking to improve their rosters through the draft. Every June, NBA teams hope to find the missing player(s) that will bring them to the next level. Oftentimes, NBA teams wind up dissapointed with their picks and leave their fans wondering why a player was even drafted in the first place. 

## Objective
Create a a model that can accurately predict how rookies will perform as NBA players by classifying them into one of four categories: Bust, Role Player, Starter and All-Star. 

## Dataset
In order to create a model that can accurately predict how rookies will perform as NBA players, I webscraped NBA statistics, College statistics (final year) and additional information from https://www.basketball-reference.com/ and https://www.sports-reference.com/cbb/  for 1,013 NBA players dating back to 1980. I used Number of All Star appearances, PER (Player Efficiency Rating) per Season and NBA Tenure in order to classify the players in the dataset into the one of four categories. As a result, there were 304 players classified as "Bust", 375 classified as "Role Player", 254 classified as "Starter" and 80 classified as "All-Star". 

## Process & Repository Contents
* ***Webscraping:*** webscraping data from www.basketball-reference.com and www.sports-reference.com/cbb 
  * [NBA and NCAA Stats Scraping.ipynb](https://github.com/KenHoffman95/Mod-5-Capstone-Project/blob/master/NBA%20and%20NCAA%20Stats%20Scraping.ipynb)
* ***Data Cleanning and Feature Engineering:*** cleaning data and engineering new features in preparation for modeling
  * [Data Cleaning and Feature Engineering.ipynb](https://github.com/KenHoffman95/Mod-5-Capstone-Project/blob/master/Data%20Cleaning%20and%20Feature%20Engineering.ipynb)
* ***EDA, Modeling and Evaluation:*** Analysis of the data through visualizaitons to gain better understanding. Building models and determining which one is the best. 
  * [EDA and Modeling.ipynb](https://github.com/KenHoffman95/Mod-5-Capstone-Project/blob/master/EDA%20and%20Modeling.ipynb)

## Modeling
The Models I tested were:
* KNN
* Logistic Regression
* Decision Tree
* Random Forest
* Voting Classifier
* XGBoost

Because I had to account for class imbalance and wanted to minimize the amount of false positives that my model outputs, I used F1 (weighted) score and Precision score respectively to evaluate my models. My best model was XGBoost which had an F1 (weighted) score of .902 and a Precision Score of .914. These scores were significantly higher than the scores I got with the other models. The most important features in the model were 'Years in College', 'Undersized', and 'FG%'. The model favored players that spent fewer years in college, were not undersized and had a higher FG%.

## Model Evaluation
In addition to observing a high F1 and Precision score, I wanted to evaluate the XGBoost model by using it to predict on a draft class. Since my dataset only had players that were drafted in 2017 and before, I used the 2018 NBA Draft class to evaluate my model.

* All-Star - Trae Young and Shai Gilgeous-Alexander
* Starter  - DeAndre Ayton, Mo Bamba, Jalen Brunson, Aaron Holiday and Gary Trent Jr. 
* Role Player - Mikal Bridges, Keita Bates-Diop, Kevin Huerter, Bruce Brown, Tony Brown, Devonte' Graham, Kevin Knox, Donte DiVincenzo, Jevon Carter, Jerome Robinson, Josh Okogie, Zhaire Smith, Mo Wagner, Omari Spellman, Lonnie Walker, Khyri Thomas, Sviatoslav Mykhailiuk, Chimezie Metu, De'Anthony Melton, Chandler Hutchison, Thomas Welsh and Robert Williams
* Bust - Grayson Allen, Miles Bridges, Kostas Antetokounmpo, Landry Shamet, Collin Sexton, Jaron Blossomgame, Vince Edwards, Hamidou Diallo, Jacob Evans, Alize Johnson, Frank Jackson, Melvin Frazier, George King, Jarred Vanderbilt and Jonah Bolden 

I was satisfied with the predictions that my model produced for the 2018 NBA Draft class. Although it usually takes at least three seasons for NBA players to reach their full potential, I thought that the majority of classifications given to the players were accurate based on the levels that they're currently playing. The only predictions that were noticeably inaccurate were the classifications of Landry Shamet and Collin Sexton as Busts. Based on their first two seasons in the NBA, my model would've ideally classified them as Starters. 

## 2020 Draft Class Projections

* All-Star - None
* Starter - James Wiseman, Onyeka Okongwu, Obi Toppin, Tyrese Haliburton, Kira Lewis Jr., Precious Achiuwa, Zeke Nnaji, Payton Pritchard, Vernon Carey Jr., Daniel Otoru, Xavier Tillman, Tyler Bey, Saben Lee, Nick Richards and Cassius Winston
* Role Player - Anthony Edwards, Jalen Smith, Devin Vassell, Cole Anthony, Isaiah Stewart, Josh Green, Saddiq Bey, Udoka Azubuike, Jaden McDaniels, Desmond Bane, Elijah Hughes, Robert Woodard, Tre Jones, CJ Elleby, Skylar Mays, Cassius Stanley, Grant Riller, Reggie Perry, Paul Reed, Jalen Harris and Sam Merrill 
* Bust - Patrick Williams, Isaac Okoro, Aaron Nesmith, Tyrese Maxey, Immanuel Quickley, Malachi Flynn, Tyrell Terry, Jahmi'us Ramsey, Jordan Nwora, Nico Mannion, Isaiah Joe and Justinian Jessup 

## Next Steps
* Include draft combine measurements in data
* Create model to predict how basketball players from foreign leagues will perform in the NBA

## Presentation
https://docs.google.com/presentation/d/1KQHi55iG6syKPLgX_9aHa_oR1w6M07tKeVrQ-Zmvpjc/edit#slide=id.p



