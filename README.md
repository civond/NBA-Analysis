<h1>NBA Analysis Capstone Project</h1>
Our goal is to build a machine learning model that can (with reasonable accuracy) predict whether said player will make the NBA playoffs based a variety of factors such as: three point attempted vs made, experience level, etc (see image below). We picked this topic because we believe that it would be interesting if we can predict the success of a player within the NBA based off of their statistics.<br><br>

<img src=possible_workflow.png width=800px></img>
<ul>
    <li>Team Structure: Jack = presentation, Dorian = GitHub repository/machine learning , Ari - database creation.</li>
    <li>Communication protocol - we are communicating via Slack and have scheduled biweekly meetings during classtime.</li>
    <li>Data used: we are using three NBA datasets downloaded from Kaggle.</li>

</ul><br/>

<h2>Machine Learning Model Overview</h2>
<div><b>Preliminary Data Processing: </b>Originally, I had thought to merge all three datasets together. However, I realized that one dataset (advanced player stats) lacks a team category label, thus I am going to omit merging it with the other two until we figure out a way to label it correctly . I merged the player totals and teams datasets together (refer to Cleaned_Data_Alt.ipynb). <br/><br/>

<b>Feature Selection: </b>After merging the datasets, I decided to drop the season, player name, team name and games started because they have no effect on whether the individual makes it to the playoffs. <br/><br/>

<b>Split and Training: </b>I split the datasets into 70% for training, and the remaining 30% for evaluating our model. <br/><br/>

<b>Model Choice: </b>For the time being, I decided to test two ensemble learning classifiers (balanced random forest and easy ensemble adaboost). Overall, I only achieved an accuracy of ~61% and ~60%, which isn't ideal. I believe that we should try merging the third dataset before trying other methods. <br/><br/>
Balanced Random Forest:

    Pros - it can handle datasets with higher dimensionalities, and identify most significant variables.

    Cons - May overfit noisy datasets.

Easy Ensemble ADABoost:

    Pros - Not as prone to overfitting as balaced random forest.

    Cons - Requires a quality dataset (outliers/noisy data should be avoided)

</div>

<h2>Dashboard Concept</h2>
Demo Storyboard: <a>https://docs.google.com/presentation/d/1VQ8e_Y5QtRa-lqhXdS1Z7zf5Fnh6p61ZbZFkb3y1EK8/edit#slide=id.p</a>
