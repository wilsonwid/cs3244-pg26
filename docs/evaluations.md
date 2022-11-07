# General description
The following evaluation metrics are options that we have considered. However, to judge the efficacy of our models, we have decided on primarily using the mean absolute percentage error (MAPE) and median absolute percentage error (MdAPE). These evaluation metrics are best suited for our particular dataset due to property prices having a wider range of values, i.e. a percentage error indicates a similar proportion of impact be it for a $100,000 or a $10,000,000 property. This is crucial as the resale price has a heavy right-tailed distribution (see the figure below; also available in the EDA report) due to some properties having very high transaction prices. Furthermore, both the MAPE and the MdAPE are more easily understandable metrics as they are described in terms of percentages.

## Price histogram
Below is a histogram of resale property prices, which indicates a heavy right-tailed distribution.

![price-freq-hist.jpg](price-freq-hist.jpg)

# Primary model evaluations
In this section, we shall detail the performance metrics of the models that our team has created. Note that since this is only a primary stage of evaluation, we only compare the different models based on the five metrics that we have chosen, without any accompanying data visualisations.

## Biased model results
Please visit [this page]() to view the performance metrics of our models that have been trained using an arbitrary train-test split, i.e., the results of models tainted with lookahead bias. 

A notable result is that of kNN regressor, where the MAPE was close to 0%, indicating that there must be some serious issue either with overfitting or with the training data.

## Unbiased model results
Please visit [this page]() to view the performance metrics of our models trained after fixing the lookahead bias.


# Extended model evaluations
In this section, we shall detail the three models that we have selected, namely rolling bagging regressor, rolling kNN regressor, and rolling XGBoost regressor in more depth through the use of data visualisations on the models' predictions.

## Rolling bagging regressor

## Rolling kNN regressor

## Rolling XGBoost regressor
* [xgboost-lat-lon-fig.html](rolling-xgboost/xgboost-lat-lon-fig.html)