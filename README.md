<h1>NBA Analysis Capstone Project</h1>
Our goal is to build a machine learning model that can (with reasonable accuracy) predict whether said player will make the NBA playoffs based a variety of factors such as: three point attempted vs made, experience level, etc (see image below). We picked this topic because we believe that it would be interesting if we can predict the success of a player within the NBA based off of their statistics.<br><br>

<h2>Machine Learning Model Overview</h2>
<div><b>Preliminary Data Processing: </b>We merged three datasets together: advanced_player_stats, team_stats, and player_totals (all downloaded from Kaggle). <br/><br/>

<b>Feature Selection: </b>After merging the datasets, we dropped multiple columns such as: season, team, abbreviation, player_id, etc. because they have no effect on whether a player makes it to the NBA playoffs or not. Additionally, we filtered the dataset to only include the years 1984-2020.<br/><br/>

<b>Split and Training: </b>I split the datasets into 70% for training, and the remaining 30% for evaluating our model. <br/><br/>

<b>Model Choice: </b>I used two ensemble learning classifiers (balanced random forest and easy ensemble adaboost). Overall, I achieved an accuracy of ~77% for balanced random forest, and ~76% for the easy ensemble adaboost. Although our achieved accuracy score is not ideal, we believe that our model does a decent job for predicting our target. There are multiple factors outside of a players individual statistics that influence whether they make it to the playoffs or not. For example, how the team performed as a whole or which specific players were traded, and others.

<br/><br/>
Balanced Random Forest:

    Pros - it can handle datasets with higher dimensionalities, and identify most significant variables.

    Cons - May overfit noisy datasets.

Easy Ensemble ADABoost:

    Pros - Not as prone to overfitting as balaced random forest.

    Cons - Requires a quality dataset (outliers/noisy data should be avoided)

</div>

<h2><a href="https://public.tableau.com/app/profile/jack.hansley/viz/nba_stuff/Story1?publish=yes">Dashboard</a></h2>

 <ul>
 <li>The dashboard is focused around trends for different player stats and how they impact a player going to the playoffs</li>
 <li>Colors are used to distinguish whether a player goes to the playoffs</li>
 <li>The dashboard will be a mixture of machine learning analysis and relevant player stats</li>
 </ul>


<br/>

<h2>Project Structure</h2>
(Refer to image below for a visual of how our project was structured)
<ul>
    <li>Team Structure: Jack = Tableau visualizations/presentation, Dorian = GitHub repository management/machine learning model, Ari - database management/cleaning the datasets.</li>
    <li>Data used: we are using three NBA datasets downloaded from Kaggle.</li>
</ul>
<img src='Images/workflow.png' width=800px></img>
<br/>
