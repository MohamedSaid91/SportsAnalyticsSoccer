# SportsAnalyticsSoccer
Soccer Match Outcome Prediction

1.INTRODUCTION

1.1 Background
Football's widespread popularity and the complexity of match outcomes make predictions challenging yet crucial for strategic and entertainment purposes. The shift from traditional expert-based forecasts to data-driven approaches has emphasized the need for accurate, analytical predictions in sports. This project addresses this need by offering data-backed insights for strategic planning.

1.2 Problem Statement
The Football Match Prediction project focuses on developing a model to forecast football match outcomes and identify key statistical metrics influencing these outcomes. It involves analyzing historical data to find patterns crucial for predictions. This prediction includes identifying whether it will be a home win, away win, or a draw as well as highlight the most impactful game performance metrics (stats).

1.3 Objectives:
• To Predict the Outcome of a football Match
• To Get Key Statistical metrics which significantly determine the outcome of a match.

1.4 Significance:
The importance of the Football Match Prediction project in the context of machine learning (ML) and deep learning (DL) lies in its potential to showcase the capability of these technologies in accurately analyzing and predicting complex, real-world outcomes. It demonstrates how ML/DL can handle vast datasets to uncover hidden patterns and insights, contributing to strategic decision-making in sports. Although I employed one of the foundational methods to address the project goals, sports science is a rapidly growing field that will significantly contribute to advancements in ML/DL.

1.5 Impact:
Teams, coaches, analysts, and football fans will benefit from improved strategic decision-making and enhanced understanding of game dynamics through data-driven insights provided by this project's predictive modeling.

2. METHODOLOGY

2.1 Data Source:
Data for all English Premier League matches which was collected via web scraping from the official Premier League website and uploaded to Kaggle by P. FREITAS i. There are 4,070 matches, from 2010 to 2021, with 113 stats features for each match and team performance throughout the season at the time of each match.

2.2 Data Preprocessing:
I.   Analyzed and understood all the dataset columns. Selected 24 most common stats based on industry knowledge.
II.  Created target class [‘Result_Class’] from full time result score feature.
III. Checked for class imbalance.
IV.  Converted class label from string values to integer as ML deals with INT better.
V.   Used Pearson correlation analysis to select most impactful features on class label. 5 positive correlation (home team features) and 5 negative correlation (away team features).
VI.  Final features scaled using MinMaxScalar.
VII. Detected using IQR and dealt with outliers by removing them.
VIII. Dataset split: Training 80% and Testing 20%

2.3 Model Selection:
Logistic regression with One-vs-Rest (OvR) was chosen for its simplicity and efficacy in multiclass problems, like predicting football match outcomes. Additionally, research, notably the "Machine Learning Models Reveal Key Performance Metrics of Football Players to Win Matches in Qatar Stars League"ii paper, demonstrated logistic regression's superior performance in similar predictive tasks, further validating its selection for this project.
