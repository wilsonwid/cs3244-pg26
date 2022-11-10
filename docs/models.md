# Baseline models

We initially created a simple linear regression and polynomial regression model for our baseline as they are versatile and allow us to understand the data better. For these two models, the data was split into an 80% training and 20% test set, and from our results, linear regression doesn’t perform too well, with an MAPE of 27% and 16% respectively. We can see that a polynomial regression model with degree 2 performs slightly better, however the performance increase is only marginal at best. This led us to explore other types of models such as decision trees, neural networks, kNN regressor, and ensemble models, the designs of which we iterated based on their performance.

# More advanced models

As mentioned above, we decided to implement several types of models, namely decision tree regressors, kNN regressor, neural networks, and ensemble regressors. The first and last fall into the symbolist tribe, the second into the analogizer, and the third into the connectionist. With the exception of neural networks, we used a grid search algorithm on all our model types to automatically find the best hyperparameter(s) out of the possibilities we gave in the hyperparameter search space.

The best hyperparameters for all of the models we created are given in [this page](hyperparameters.md).

## Decision trees (and its ensembles)
We first made a basic decision tree model, after which we improved its features by adding on recursive feature elimination, as well as modified the learning algorithm itself by exploiting ensemble learning. The latter is done with adaptive boosting regressors (in AdaBoost) or by selecting random subsets of the data and fitting base regressors on them (as is the case in a bagging regressor). Both of these, however, are done with decision trees as the base regressor.


## Neural networks
We first created a network with a 54-1 dense architecture to act as a baseline for this model type. This is then enhanced into a 54-108-108-1 architecture, which immediately led to major overfitting problems. After some tweaking and fixing of the [lookahead bias](lookahead-bias.md), we eventually settled on a 57-20-1 architecture. This, however, had extremely inaccurate predictions on a level comparable to the simple linear regression we developed earlier.

## kNN regressor
In creating this model, we decided to grid search on a 10% sample of the original dataset to quicken our search of an optimal hyperparameter. This grid search includes finding the best distance metric, value of $k$, as well as whether the points are weighted uniformly or by the inverse of their distance.

## Ensemble regressors
These regressors are built on top of base regressors and extended either via "boosting" (as is the case with AdaBoost and XGBoost) or "bagging" (as is the case with bagging regressor). AdaBoost does so by fitting more weight-adjusted (based on the current error) copies of the regressor on top of the base, while the bagging regressor samples random subsets of the dataset and trains copies of the base regressor on it, before predicting via averaging each copy's predictions. XGBoost is similar to AdaBoost albeit  with an optimised version of gradient boosting instead of normal boosting.