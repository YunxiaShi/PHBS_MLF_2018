# Outcome of NFL games based on the QB's performance
## PHBS_MLF_2018

ID# OscarHemmingsen - 1802010265 
ID# ThanhVuongng - 1802010228

## Description

This project will use the statistics from different Quarterback (hereafter QB) performances over time dating back to 2002. Furthermore, we have collected the actual outcome of those game, so that we are able to match statistics from the QB's performance to the actual outcome. Hence, we will try to build a model that will be able to predict the outcome of an NFL-game based on the QB's performance.

## Data & Preprocessing

Our dataset was found on Kaggle in which all different quarterback performances from the late 90's up until 2016 was included. Here, various statistics such as attempts, completions, touchdowns etc. were included. However, we needed to find out whether the team actually lost or won that actual game. This statistic was not included in the dataset. Therefore, we found via NFL.com's database the actual outcome of that particular game in which we matched the year and the quarterback to the actual game.

Since the dataset was for ALL QBs that had played a game, it also included backup statistics e.g. when the team is leading by a lot and the team decides to rest the starting players. Therefore, we made a threshold in which all QBs had to at least make 15 attempts in the game. We felt this would give the indication that the QB had at least started the game and probably played at least half of the game.

Below is a snapshot of how our data is presented:

![data overview](https://user-images.githubusercontent.com/42951299/48195285-2aed8000-e38a-11e8-8c3d-7226dd9789d2.jpg)

First, we wanted to get visuals of the data, so we made some simple graphs and tables so we could maybe get some pre-indications for our model.

![mean win-loss stats](https://user-images.githubusercontent.com/42951299/48195951-fd093b00-e38b-11e8-84a8-b884dd0690b0.jpg)

Above is a mean computation of a winning and losing QB. It is interesting to see that a winning QB on average throws fewer times than a losing QB. We would assume based on the current state of the NFL and how the game is played now that the roles would have been switched. Other than that we conclude that the data is fairly logical in which the QB throws more touchdowns and less interceptions (when the opposing team catches the ball) when the team is winning.

Below are two simple versus tables for win or losses compared to touchdowns and interceptions.

![statistik over sejre 2](https://user-images.githubusercontent.com/42951299/48198984-a43ea000-e395-11e8-90bb-a098fd576f1e.png)

![statistik over sejre](https://user-images.githubusercontent.com/42951299/48198823-14005b00-e395-11e8-91d0-c8c96b123ec3.png)




## Models & Graphs

### Logistis regression

First, we stated trying to build a logistic regression model. This was mainly due to its simplicity and the fact we have a binary output

<img width="590" alt="logistic regression" src="https://user-images.githubusercontent.com/42951188/48195643-2d9ca500-e38b-11e8-96e2-2a8f1cfa2dbc.png">

### Decision tree

We build two decision tree models. One, where we decide via the gini and the second with the information gain

Gini index

<img width="697" alt="gini index" src="https://user-images.githubusercontent.com/42951188/48195642-2d040e80-e38b-11e8-9753-3827cd9a254c.png">

Information gain 

<img width="748" alt="information gain" src="https://user-images.githubusercontent.com/42951188/48195645-2d9ca500-e38b-11e8-91e1-cc638a9bcfe1.png">

### KNN with K=8

![knn](https://user-images.githubusercontent.com/42951299/48198815-0b0f8980-e395-11e8-8d42-1a70e8c5c7e1.jpg)


### Confusion matrix and ratios 

Below is our confusion matrix and the following ratios

![confusion matrix](https://user-images.githubusercontent.com/42951188/48194979-74899b00-e389-11e8-9a3a-2a005d4da274.png)

Accuracy, Prediction and Recall

<img width="254" alt="accuracy_prediction_recall" src="https://user-images.githubusercontent.com/42951188/48195644-2d9ca500-e38b-11e8-9bf8-cea2e7d7de16.png">

Cross-validated score

![cross-validation](https://user-images.githubusercontent.com/42951299/48198812-077c0280-e395-11e8-80c7-df11f8bdd19a.jpg)




# Goal of the project

The goals of this project are the following:
- Ability to predict the outcome of an NFL-game based on the Quarterbacks (QB) performance.
- Group performances "together" and quantify a "bad", "medium" and "good" performance.
- Being able to show the changes in the game over time based on data from the early 2000's.


