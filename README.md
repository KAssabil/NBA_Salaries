# NBA Salaries Prediction Model

## Introduction & Questions
For this project, I wanted to explore to what extent would I be able to predict the salary of the NBA players based on several player attributes. I first selected a set of relevant features and analyzed their impact in the player salary separatedly. Then, I built a predictive model with those features that have a larger influence on the player salary.
Since for each player I have a wide range of statistics at disposal, I considered for this analysis only some relevant ones, to avoid multicollinearity in our predictors. I took into account the minutes per game (MPG), the points per game (POINTS) and the offensive/defensive real plus-minus values (ORPM and DRPM). 

## Data Cleaning
Missing values and outliers I knew would make the modelling process very difficult. I used imputation method to fill in any missing values. I chose the median number of the whole column to fill in the missing variables because a median value will not be influened by outliers.

## Descriptive Stats
To understand the data, descriptive statistics can be used to understand of the dataset. The methods included mean, median, mode, standard deviation, interquatile range. 

## EDA
![](Screen%20Shot%202020-12-23%20at%2012.33.34%20PM.png)
![](Screen%20Shot%202020-12-23%20at%2012.33.52%20PM.png)
![](Screen%20Shot%202020-12-23%20at%2012.34.12%20PM.png)

## Modeling Analysis
I began running different linear models to try and grasp the variables I'll need for my final model. For every independent variable I ran against the dependent varibale(salary) I calculated the R-Squared, RMSE, and pearson correlation coefficient. I use these values to gage what effect the independent variable has on the dependent variable on it's own. I ran into a problem with trying to see the effect of position on salary; this was an easy fix because since there are 5 positions I changed all the positions to numerical values and did my analysis.
After grasping how the independent variables effect salary indivdually I split the data into training and testing sets and built my final model on the training set to compare to the predictions on testing set
I included the age variable because of the curve relationship between age and salary. I also included offensive stats since they seem to make salary go up; I aslo added AST and FG% since those can be catogrized as offensive stats.
My final model yielded an R-Squared of 0.59 and an RMSE value of 4.43; this model was the best R-Squared I got from all my regression models. This model still shows significant bias even though it performs better than all the other variables that were considered independently. With this model on average we're about 4.43 million dollars off per player for their salary.

## Conclusion and Improvement
With this model I would say it can predict the salary of an NBA player to a certain degree but it's also not the most accurate. To improve this model I believe I would have to other variables both numerical and categorical that influence salary indirectly such as likeliness,tenure with the team, team capspace and if the player has been an allstar in the past or not. Predicitng NBA salaries can also be improved by using other types of analysis besides linear model regression which is more limited in it's abilities.


