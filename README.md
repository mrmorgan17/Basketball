# Basketball

This repository includes exploratory analysis and predictive modeling for the Kobe Bryant Shot Selection Kaggle competition (https://www.kaggle.com/c/kobe-bryant-shot-selection). All code was done using the R programming language.

The .Rmd file `ShotAnalysis.Rmd` includes the code and output for the methodology of feature selection, model building, and model tuning for the competiton.

The .Rmd file `EDA.Rmd` includes many graphs and visualizations that were created while looking at the variables included in the competition dataset.

A notebook was created on Kaggle for this competition as well and can be found [here](https://www.kaggle.com/matt4byu/kobe-bryant-shot-selection-analysis-with-xgboost).

The goal of this competition was to use 20 years of data on Kobe's makes and misses to predict which shots he would make or miss? This competition is well suited for practicing classification basics, feature engineering, and time series analysis. The dataset for this comeptition (`data.csv`) included data on 30,697 of Kobe's shots as well as data about shot distance, shot location, opponent, time left in the game, game date, etc. 5,000 of Kobe's shots had the indication of whether he made it or not removed (replaced with NAs) and these 5,000 shots formed the testing set of the data while the remaining 25,697 shots formed the training set. 

The best model that was fit to the data was an xgboost model. Models were fit using the [xgboost](https://www.rdocumentation.org/packages/xgboost/versions/1.1.1.1) R package. This competiton used logloss as the defining metric to compare submissions to each other. While the competition closed approximately 4 years ago, privately, the best logloss score achieved from an xgboost model was .60101 which would place 76th out of 1117 teams on the Kaggle leaderboard for this competition. Using the same code in a Kaggle notebook has currently achieved a best score of .60125 which would place 94th out of 1117 teams. Both of these scores place in the 90th percentile on the Kaggle leaderboard with the private score placing in the 93rd percentile. 

Additional improvements could be made in the areas of feature selection, model tuning, and avoiding leakage better.

