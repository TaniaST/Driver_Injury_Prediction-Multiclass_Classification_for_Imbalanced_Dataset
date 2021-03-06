# Driver's Injury Prediction Project
The purpose of the study is to predict driver’s injury level in a car crash using machine learning techniques. The data used for the analysis are the records of bodily injury accidents occurred between two cars in Metropolitan France in 2005-2017. The outcome variable is severity of the accident represented by four levels of injury: “no injury”, “light injury”, “hospitalised” and “killed”. Exploratory data analysis (see EDA Jupyter Notebook for details) shows that the dataset is highly imbalanced, and most independent features are highly fractioned categorical variables. To avoid overfitting in the tree-based models, we aggregate these features and then apply one-hot encoding to make it possible to include them in the models. Based on correlation check and Cramer’s V strength of association test results, the following features are relevant to be included in the models: legal speed limit, hour of accident, driver’s age, built-up area (whether the crash took place in or out of a built-up area), gender, road shape, lighting conditions and shock point. In our study, we use two scaling techniques: normalisation and standardisation. We train Random Forest, XGBoost, Support Vector Machines and K-nearest Neighbours models on normalised, standardised, and unscaled data to see if scaling improves the performance of the models (see Models Jupyter Notebook for details). We also create two Convolutional Neural Networks models and train them on standardised data. One of the CNN models is directly created for our multiclass classification task. The other CNN model is built using transfer learning technique by saving the weights of a CNN model trained on the same dataset but with a two-class outcome (see CNN Google Colab file).

To evaluate the models, we choose macro-averaged F-1 score, precision, and recall, as well as Matthews Correlation Coefficient, as these metrics allow to consider
the imbalance between classes when comparing the predictive performance. 

The conclusions can be summarised, as follows:

• Support Vector Machines give better results if data is normalised or standardised. Random Forest, XGBoost and K-Nearest Neighbours algorithms, on the contrary, do not show considerable changes in performance depending on whether data have been scaled or not.

• CNN model created using transfer learning technique performs significantly better than the one directly built for four-class outcome.

• Random forest and XGBoost models outperform the other algorithms, giving the highest overall macro-averaged F-1 score at 0.37 for both models. XGBoost has higher precision at 0.44 vs. 0.39 for Random Forest but lower recall at 0.37 vs. 0.47. Matthews Correlation Coefficient is also the highest for these two models with 0.23 result for XGBoost and 0.22 for Random Forest.

• Despite an almost equal overall performance, Random Forest and XGBoost behave differently in predicting minority classes. Random Forest gives the best F-1 score overall for the most underrepresented class “killed” at 0.13, whereas XGBoost model only achieves 0.03.

• Overall performance of the models is relatively low, due to the lack of the most impactful features and high imbalance present in the dataset.
