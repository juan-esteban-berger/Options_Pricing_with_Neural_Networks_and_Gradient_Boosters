# Options Pricing with Neural Networks and Gradient Boosters
This project compares Neural Networks and Gradient Boosted Decision Trees for pricing European Options. The Neural Network models were implemented using TensorFlow, and the Gradient Boosted Decision Tree models were implemented using XGBoost. Both the TensorFlow and the XGBoost models can outperform the Black-Scholes Model in terms of Mean Absolute Error and Mean Absolute Percentage Error. These results showcase the potential that using historical data from the underlying asset can have when pricing options, especially when using machine learning algorithms to learn complex features that traditional parametric models may not be able to detect.

The XGBoost algorithm has been regarded as the gold standard for machine shortly after its inception in 2014. On the other hand, Neural Networks have showcased incredible abilities in being able to learn extremely complicated functions with large numbers of variables. This study hopes to find out if deep learning algorithms are able to surpass the gold standard machine learning algorithm XGBoost in the problem of options pricing. This study will focus on pricing European Options from the IvyDB US dataset from Option Metrics. The data was split into training, validation, and testing datasets with approximates splits of 98\% of the data being used for training, 1\% of the data being used for validation, and 1\% being used for testing. Finally, the results of various Neural Network Models and various XGBoost models was be compared with the prices derived from the Black-Scholes Model, one of the classical parametric options pricing methodologies.

The results of this project show that Neural Networks seem to be far superior in estimating options prices than XGBoost. Both machine learning algorithms are able to outperform the Black-Scholes model, but it is clear that Feed-Forward Neural Networks are the superior model. It is also important to note that both the Neural Networks and the Gradient Boosted Decision Tree Models were not given implied volatility as a feature like the Black-Scholes model was, but learned all the necessary features on their own from the other feature variables and the past 20 lags of the underlying securities closing prices. With high volumes of data and computing resources becoming highly available, using machine learning and deep learning methods for options pricing becomes a viable option for pricing securities. It would be also be interesting to compare machine learning and deep learning methodologies with other option pricing methods such as Monte Carlo Simulations or the Binomial Asset Pricing Model in order to see if the Machine Learning models are able to surpass those models as well. Nevertheless, the results of this study seem to be consistent with the results of other related studies in that deep learning methods are able to outperform the Black-Scholes model, and in this case the gold standard in classification and regression problems, the XGBoost algorithm. 6 Different Options Pricing models were implemented in python for this project. The first model was the Black-Scholes model, the second was a 3-Layer Feed Forward Neural Network, the third was a 4-Layer Feed Forward Neural Network, the fourth was a 5-Layer Feed Forward Neural Network, the fifth was an XGBoost model with a max-depth of 5, and the sixth model was an XGBoost model with a max-depth of 10. The performances of the six models can be seen in the tables below.

| Model              | Call   | Put    | Total  |
| ------------------ | ------ | ------ | ------ |
| 5 Layer FFNN MAE   | 5.20   | 4.33   | 4.765  |
| 4 Layer FFNN MAE   | 5.30   | 4.46   | 4.880  |
| 3 Layer FFNN MAE   | 6.20   | 5.11   | 5.655  |
| XGBoost 10 MAE     | 10.13  | 4.55   | 7.340  |
| XGBoost 5 MAE      | 13.33  | 7.41   | 10.370 |
| Black-Scholes MAE  | 28.23  | 21.17  | 24.700 |

| Model               | Call    | Put     | Total   |
| ------------------- | ------- | ------- | ------- |
| 5 Layer FFNN MAPE   | 33.06   | 42.31   | 37.685  |
| 4 Layer FFNN MAPE   | 35.89   | 45.67   | 40.780  |
| 3 Layer FFNN MAPE   | 41.13   | 54.99   | 48.060  |
| XGBoost 10 MAPE     | 47.62   | 59.06   | 53.340  |
| Black-Scholes MAPE  | 57.18   | 70.22   | 63.700  |
| XGBoost 5 MAPE      | 193.39  | 264.49  | 228.940 |

This research project contains components for three graduate level courses at the University of Notre Dame, which are ACMS 80695 - Master's Research Project taught by Prof. Guosheng Fu, CSE 60868 - Neural Networks taught by Prof. Adam Czajka, and ACMS 60890 - Statistical Foundations of Data Science taught by Prof. Xiufan Yu. The Tensorflow Neural Networks were completed for CSE 60868, the XGBoost models were completed for ACMS 60890, and the research methodologies and big data applications in google cloud were performed as part of the ACMS 80695 project. A special thanks is given to all these professors for their teaching and support during the Spring Semester of 2023.
