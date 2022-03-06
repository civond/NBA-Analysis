# NBA-Analysis  
## Overview  
The goal of this project was to analyze a set of metrics for NBA players for each season between 1979 and 2021 and to construct a model that could predict with reasonable accuracy whether a player would make the playoffs. Player metrics were evaluated independent of player name and which team they played for - therefore allowing a focus on the metrics themselves. We obtained three datasets obtained from https://www.kaggle.com/sumitrodatta/nba-aba-baa-stats containing individual and team data beginning in 1947.   

### Overall project schematic:  

![nba](https://user-images.githubusercontent.com/60231630/156903252-00ebdc1c-0317-4872-9d59-5300b981b4e7.png)   

### Preliminary Data Processing:  

We utilized three datasets included in the resources folder:   

advanced.csv   
player_totals.csv  
team_summaries.csv  
team_totals.csv  

The advanced and player_totals datasets contain a large set of individual player metrics (features) sorted by player and season with features such as the team they played on, age, experience, and a variety of cumulative stats for each season.  Given our goal was to see whether features for players could be used to predict whether a player makes the playoffs on any given season, it was important to evaluate our data independent of team and player name.  After cleaning the said datasets to focus on  the years 1979-2021 and focus on most complete and relevant features, we obtained three datsets (all files are available in the resources folder):   

advanced_stats_filtered.csv  
player_totals_filtered.csv  
team_summary_filtered.csv  


###  Data joining  

Cleaned datasets were uploaded to a remote relational database and merged to create a large dataset of player metrics resulting in the file: initial_merged_nba_data.csv.  
A final dataset was then created by merging this file to team_summary data which indicates whether the associated team made it to the playoffs for the season in question. The final dataset: final_nba_player_dataset.csv was then used for generating graphical/storytelling data and served as the data source for our Machine learning models.  An Entity Relationship diagram (nba_entity_relationship_diagram.png) showing the relational features for the datasets (Entities) is also included.  The included ipynb jupyter notebook: nba_players_teams.ipynb contains all code for this process including the merging of files.  Files were uploaded to the indicated relational database and can also be merged using  SQL methods.   

### Machine learning and storyboard  

Feature Selection: 
The following features were dropped: season, player name, team name and games started.  This allows the model to focus mainly on player metrics.  
<b>Split and Training: </b>I split the datasets into 70% for training, and the remaining 30% for evaluating our model. <br/><br/>

<b>Model Choice: </b>We tested two ensemble learning classifiers (balanced random forest and easy ensemble adaboost). Overall,  an accuracy of ~77%  was obtained.   

Balanced Random Forest:

    Pros - it can handle datasets with higher dimensionalities, and identify most significant variables.

    Cons - May overfit noisy datasets.

Easy Ensemble ADABoost:

    Pros - Not as prone to overfitting as balaced random forest.

    Cons - Requires a quality dataset (outliers/noisy data should be avoided)

</div>

