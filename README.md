# Machine-Learning-with-Business-Metrics

QUEST FOR UPSTREAMS!

In this project business metrics are the decision tools.

An oil company, OilyGiant is in a quest of finding a new location for its new oil mining location.

A dataset of volume oil reserves, as well as three independent variables for each oil well as observed in the past are given.

The project is to find one location with to develop with prospect to meet company's business metrics:

1. Contribute to the company's positive profitability, with budgested cost of USD 100,000,000

2. Has a potential of risk not more than 2.5%

Steps in finding that are:

1. Gather the parameters to select wells in each location: oil quality and volume of reserves

2. Build and select a model that is able to predict the volume of oil reserve in a new well

3. Select wells with highest estimated volume

4. Select location with highest total profit for the selected wells

The datasets of three locations observed:

1. id — unique ID of wells

2. f0, f1, f2 — three features that are significant

3. product — volume of oil reserves in a well (thousands barrel)


The parameters of each well are known already. 
The target of this machine learing is to find prediction of volume, that is numerical, continuous.
Hence the model needed is the regression one.
One location with the highest margin will be found.
From those three location, wells are to be sampled using bootstrapping method.
And an analysis of profitability and potential risk is made.

Three models with three different algorithms: XGBoostRegressor, LinearRegression, and LightGBMRegressor, are built.
All three algorithms perform well for dataset of Location 2. 
Yet none work satisfactorily for datasets of Location 1 and Location 3. 
This is probably related to the three given predictors being weekly relevant to the volume of oil reserved. 
Without bootstrapping, Location 1 appears as the most promising contributor to profitability.
However with bootstrapping technique, it is discovered that the extremely high figure does not fall in the confidence interval of 95% of the distribution of mean of the samples.
Finally, it is found that Location 2 is solid and more likely to contribute the highest profit, with mean distribution of confidence interval of 95% : USD 1,050,097 - USD 9,635,649, and loss potential as low as 0.5%.
