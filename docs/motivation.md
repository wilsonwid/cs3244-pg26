# Background 

Traditional property valuation methods are costly and manual in nature, requiring an appraiser to assess the property and make calculations based on comparable properties. With an automated model that makes price predictions given a set of property characteristics, we have a systematic and unbiased way of getting valuation estimates which are faster and cheaper. Such a model can also reduce fraud cases in valuations, given that the property features that serve as the model's inputs are not tampered with.

Appraisers can use this model to get a first-cut estimate on valuation of properties and supplement it with additional human knowledge of the uniqueness of each property. Furthermore, sellers can use the model to get an estimation of their existing property’s value to arrive at a competitive ask price, while buyers can be more informed to fairly assess their options. In essence, all parties are able to come towards a conclusive price point for a transaction to happen without under- or over-valuing the property.

# Main goals
With our motivation in mind, we wanted to do three things in this project:

1. ## Making an accurate price prediction model
First, we aim to create an ML model that can accurately make price predictions given property characteristics. Our plan was to try out different machine learning models that would be suitable for this task and dataset, and then evaluate their performance to determine the best models. 

1. ## Feature importance analysis
We also aim to identify the features most responsible for a property's resale price, to derive interesting observations from our model's performance on the dataset. This will be informative to home buyers on what are the most influential features that will affect a HDB flat’s value.  

3. ## Identify under- and over-valued properties using model predictions
Lastly, we also wanted to run a simulation to study how well our model would perform if we were to use its predictions to identify undervalued/overvalued properties on a rolling basis. This is to say, if someone were to use our model to purchase an identified undervalued property, would they see a good return on investment after 10 years?
