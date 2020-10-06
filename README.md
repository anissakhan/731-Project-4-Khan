# Project 4 - Major Leagues

### Scope

The datasets used in this project (linked below) contain detailed NFL data ranging from 1920 to 2018 seasons. The purpose of this project is to use regression models to predict the target variable--Score of the game.

### Results

I used the Linear Regression and Random Forest models to predict the score of a team for a given game.  Since there are 2 score variables--score1 for team1 and score2 for team2--regressions are run separately where each score1 and score2 serve as the target variable. Since all the teams switch between being team1 and team2, the results for these regressions are similar. I used a correlation heatmap to determine the best predictors of score and then ran Linear and Random Forest regressions. The linear regression produced an R^2 of 0.48 meaning 48% of the variation in score (dependent variable) could be explained by the features (independent variables) I chose. The Random Forest regression visually appeared to explain more variation than the linear regression, which is expected because the random forest predictions are not required to follow a straight line.

Please see the Jupyter Notebook for more details and further discussion.

### Data
Datasets obtained from:
1. https://github.com/fivethirtyeight/nfl-elo-game
2. https://github.com/fivethirtyeight/data/tree/master/nfl-elo

### Variable descriptions

Most of the variables are variations on the Elo score, which is "a measure of strength based on head-to-head results and quality of opponent."

One of the important features in my model were the quarterback elo scores explained here: "Our quarterback-adjusted Elo model incorporates news reports to project likely starters for every upcoming game and uses our quarterback Elo ratings to adjust win probabilities for those games. A team’s current quarterback adjustment is based on possible starters in its next game and how much better or worse that QB is than the team’s top starter." (source: https://projects.fivethirtyeight.com/2019-nfl-predictions/)

Definition
date -	Date of game <br />
year -   Year of game <br />
month -  Month of game <br />
day -    Day of game <br />
season-	Year of season <br />
neutral -	Whether game was on a neutral site <br />
playoff -	Whether game was in playoffs, and the playoff round <br />
team1 -	Abbreviation for home team <br />
team2 -	Abbreviation for away team <br />
elo1_pre -	Home team's Elo rating before the game <br />
elo2_pre -	Away team's Elo rating before the game <br />
elo_prob1 -	Home team's probability of winning according to Elo ratings <br />
elo_prob2 -	Away team's probability of winning according to Elo ratings <br />
elo1_post -	Home team's Elo rating after the game <br />
elo2_post -	Away team's Elo rating after the game <br />
qbelo1_pre -	Home team's quarterback-adjusted base rating before the game <br />
qbelo2_pre -	Away team's quarterback-adjusted base rating before the game <br />
qb1 -	Name of home starting quarterback <br />
qb2 -	Name of away starting quarterback <br />
qb1_value_pre -	Home starting quarterbacks's raw Elo value before the game <br />
qb2_value_pre -	Away starting quarterbacks's raw Elo value before the game <br />
qb1_adj -	Home starting quarterbacks's Elo adjustment for the game <br />
qb2_adj -	Away starting quarterbacks's Elo adjustment for the game <br />
qbelo_prob1 -	Home team's probability of winning according to quarterback-adjusted Elo <br />
qbelo_prob2 -	Away team's probability of winning according to quarterback-adjusted Elo <br />
qb1_game_value -	Home quarterback's Elo value during this game <br />
qb2_game_value -	Away quarterback's Elo value during this game <br />
qb1_value_post -	Home starting quarterbacks's raw Elo value after the game <br />
qb2_value_post -	Away starting quarterbacks's raw Elo value after the game <br />
qbelo1_post -	Home team's quarterback-adjusted base rating after the game <br />
qbelo2_post -	Away team's quarterback-adjusted base rating after the game <br />
score1 -	Home team's score <br />
score2 -	Away team's score <br />
result1 - Whether or not team1 won the game (1=team1 won, 0=team2 won) <br />

### References
1. To implement linear regression:
     - https://www.geeksforgeeks.org/linear-regression-python-implementation/
     - https://medium.com/python-in-plain-english/ols-linear-regression-basics-with-pythons-scikit-learn-4ecfe88145b
2. To implement random forest regression:
    - https://towardsdatascience.com/random-forest-and-its-implementation-71824ced454f
