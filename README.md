# PredictingFlightDelay
Feature extraction for predicting whether a flight will be delayed more than 15 minutes

For training the model to predict whether a flight will be delayed, the Airline On-Time Performance Data was used. Target variable, which is initially a continuous value of flight delays in minutes, was binarized so that delays exceeding 15 minutes would be represented by ones.  

For predictive model class, Random Forest Classifier was used due to its inherent feature importances attribute and robustness while handling of both categorical and numerical variables. Best performing RFC appeared to have no errors, therefore validating the model on an external set was necessary.  

Prior to feature selection, data preprocessing, numerical and categorical encoding, small scale feature engineering was performed. One of the engineered features, 'InHolidaySeason', appeared to be in the 6.25th percentile among the features that are returned by the tuned model.  

For the experiment, an external dataset and the highest ranking feature, arrival delay or 'ArrDelay', was used as the sole input for an untuned Random Forest Classifier. The predictions based solely on this feature measured to have a precision of 0.94, recall of 0.97, and F1-score of 0.95 for predicting an on-time flight. For delayed flights, the performance appeared to be weaker with a precision of 0.82, recall of 0.69, and F1-score of 0.75.  

This results revealed that, Arrival Delay is indeed a significant feature to predict flight delay, and there is room for improvement in reducing false negative detection.
