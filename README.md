<h1>NBA Analysis Capstone Project</h1>
Our goal is to build a machine learning model that can (with reasonable accuracy) predict whether said player will make the NBA playoffs based a variety of factors such as: three point attempted vs made, experience level, etc (see image below). We picked this topic because we believe that it would be interesting if we can predict the success of a player within the NBA based off of their statistics.<br><br>

<img src=possible_workflow.png width=800px></img>
<ul>
    <li>Team Structure: Jack = presentation, Dorian = GitHub repository/machine learning , Ari - database creation.</li>
    <li>Communication protocol - we are communicating via Slack and have scheduled biweekly meetings during classtime.</li>
    <li>Data used: we are using three NBA datasets downloaded from Kaggle.</li>

</ul><br/>

<h2>Machine Learning Model Overview</h2>
<div><b>Preliminary Data Processing: </b>Originally, I had thought to merge all three datasets together. However, I realized that one dataset (advanced player stats) lacks a team category label, thus I am going to omit merging it with the other two until we figure out a way to label it correctly . I merged the player totals and teams datasets together. <br/><br/>

<b>Feature Selection: </b>After merging the datasets, I decided to drop the season, player name, team name and games started because they have no effect on whether the individual makes it to the playoffs. <br/><br/>

<b>Split and Training: </b>Originally, I had thought to merge all three datasets together. However, I realized that one dataset (advanced player stats) lacks a team category label, thus I am going to omit merging it with the other two until we figure out a way to label it correctly . I merged the player totals and teams datasets together. <br/><br/>

<b>Model Choice: </b>For the time being, I decided to test out logistic regression, and two ensemble learning classifiers (balanced random forest and easy ensemble adaboost). The reason for this choice is that<br/><br/>
</div>