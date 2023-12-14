# LeagueWinPredictor

by: Edward New

## The Problem

When there are millions of dollars on the line in professional Esports, winning is the only thing that matters. Being able to predict which team wins or loses after seeing the data of an entire game is important since it reveals a lot of the key factors that affect a game's outcome. But doesn't that feel a little like cheating? Of course the team with a 5k gold lead and almost every objective won the game.

Let's see if we can improve on this prediction idea. We want to build a model that can predict which team will win or lose while the game is still going.

To do this, we'll start by looking at the game data at the 15 mintute mark to make our predictions.

The model we are trying to build is specifically a classifictaion model since instead of predicting some continuous numerical value, the model needs to make a binary decision on the outcome of the game it is looking at: Win or Lose.

The metric that we will use to measure the performance of our model is just the accuracy of the model. There is no real reason to use fancy performance metrics in this particlar case since our data is very symmetrical and there is not really a preferance for preventing against a particular type of error (False Positives or False Negatives).

Since we've made it a point to want to predict the outcome of a game while it is still going, we will only focus on data that is availiable at the 15 minute mark, which is on generally the half way mark through a game of League.

In particular we will look at:

-   kills at 15
-   cs at 15
-   gold at 15
-   xp at 15
-   turret plates (turret plates are only attainable in the first 14 minuites of any game)

## Baseline Model
