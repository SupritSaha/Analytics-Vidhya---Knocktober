# Analytics-Vidhya---Knoctober
2nd place solution

### Approach:

Initially we generated numerous features but later realized that although some of them are performing very well in the train set but they are adding noise in the test set. In this competition we mainly focused on feature engineering rather than algorithm selection. 

We built different models like logistic regression, random forest, xgboost and GBM (in h2o package) using our initial set of features and observed that, there is a significant difference between cross validation score and public leaderboard score. We realized that some of the features in train set have different distribution in test set then we started our hunt for finding out the variables, which are adding noise in the test set.

To start with, we compared the distribution of variables across test and train and then we validated our results against public leaderboard score to find out noise variables.

After eliminating noise variables, we tried aforementioned models again and among those GBM was outperforming others. Using only GBM we reached 8th position in the public leaderboard after that we tried different ensemble methods but none of them increased the score in public leaderboard.

Key learning from this competition is that, feature engineering is one of the most important parts of modeling, probably much more than the choice of algorithm. This competition reminds us the famous quote by George Box “All models are wrong, but some are useful”. I think here the useful ones are the one with good set of features.

The major key for our success in this competition is elimination of noise variables and adding relevant features.

Some of the features, which helped us in pushing leaderboard score:

1)	*Recency* – How recent a patient is
2)	*Frequency* – How frequent a patient is
3)	*Age_Prob* – Probability for getting a favorable outcome of a patient belonging to age group
4)	*Difference between registration date and camp start date*
5)	*Difference between registration date and camp end date*
6)	*Difference between registration date and first interaction date*
7)	*Camp duration*


Tools used: R (Package: h2o)



