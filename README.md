### Predicting Housing Prices: Phase 1 - Classification

#### Objective:
In the first phase of the project, the goal is to create a model to predict whether a house is expensive or not. This is a binary classification task with two possible outcomes: “Expensive” and “Not expensive”.

#### Data:
The dataset contains various features related to housing, such as the type of dwelling, zoning classification, area, quality of various amenities, and many others. There are 81 columns in the dataset.

#### Preprocessing & Feature Engineering:
- Handled missing values:
  - Numerical columns: Used mean imputation.
  - Categorical columns: Used the most frequent value for imputation.
- One-hot encoded categorical features.
- Scaled numerical features using StandardScaler.

#### Model Building & Evaluation:
- Built pipelines using KNN (K-Nearest Neighbors) and Decision Tree classifiers.
- Evaluated the models based on accuracy:
  - KNN Classifier: \( \approx 93.84\% \)
  - Decision Tree Classifier: \( \approx 93.49\% \)
  
- Conducted hyperparameter tuning using Grid Search for both classifiers. The best hyperparameters were identified:
  - For KNN: Number of Neighbors (`n_neighbors`): 7, Power Parameter for Minkowski Distance (`p`): 1, Weight Function (`weights`): 'distance'.
  - For Decision Tree: Criterion (`criterion`): 'gini', Maximum Depth (`max_depth`): 10, Minimum Samples Split (`min_samples_split`): 10.

- Error Analysis:
  - Used the confusion matrix to understand the types of errors made by both KNN and Decision Tree models.

#### Additional Models:
- Experimented with other classifiers: Logistic Regression, Support Vector Machine (SVM), and Random Forest.
- Evaluated performance based on accuracy:
  - Logistic Regression: \( \approx 94.52\% \)
  - SVM: \( \approx 94.18\% \)
  - Random Forest: \( \approx 95.21\% \)

#### Conclusion:
Among all the models, the Random Forest classifier had the highest accuracy and was chosen as the best model for this classification task.
