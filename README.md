# Top N Recommender Systems

A machine learning algorithm for recommending the top N results for a multi-class target using XGBoost. The model is implemented in both [R](xgbmodeltest.Rmd) (with [html preview](http://htmlpreview.github.io/?https://github.com/madsenmj/ml-topn-recommender/blob/master/xgbmodeltest.html)) and [Python](XGBoost_TopNRecommender.ipynb). There is also a Python implementation of the same type of model [using Tensorflow](TensorFlow_TopNRecommender.ipynb).

This multi-class recommender system reads in a `.csv` file that has, on each row, a series of features and a prediction target. The sample data have independent 6 feature columns and two feature columns that contain the same feature as the target column. These last two columns represent user history and are prior views of the target item.

# Model

The recommender uses XGBoost to calculate the multi-class probabilities using a `multi:softprob` objective.

# Evaluation Metrics

A recommendation is considered valid if the target class is among the top N predictions.
