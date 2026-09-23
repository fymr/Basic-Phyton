Human Activity Recognition Using Smartphone Sensor Data

This project uses the UCI Human Activity Recognition Using Smartphones Dataset, which contains sensor measurements collected from smartphones while participants performed different daily activities.

Dataset
The dataset contains six different activities:

* Walking
* Walking Upstairs
* Walking Downstairs
* Sitting
* Standing
* Laying

The training dataset contains 7,352 observations and 561 features from smartphone accelerometer and gyroscope signals in both time and frequency domains.

The dataset was first examined using Pandas and basic exploratory data analysis techniques:

* Dataset shape and feature inspection
* Missing value analysis
* Duplicate row analysis
* Activity distribution
* Feature histograms
* Box plots
* Scatter plots
* Feature importance analysis

No missing values or duplicate observations were found in the training data. Since the provided features were already processed and scaled, additional normalization was not applied.

The exploratory analysis also showed that some features can help distinguish different activities. For example, the combination of acceleration-related features showed a visible difference between activities such as Walking and Sitting.

Three classification algorithms were tested:

* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest

The models were trained using the training dataset and evaluated on the test dataset.

Model	Test Accuracy
KNN	97%
Decision Tree	94%
Random Forest	98%

Random Forest has the highest test accuracy among the three models.

The classification results also showed that Sitting and Standing were more difficult to distinguish than some of the other activities. Random Forest reduced the confusion between these two activities compared with KNN.


Feature importance was examined using the Random Forest model.

Some of the most important features included:
* tGravityAcc-min()-X
* angle(Y,gravityMean)
* tGravityAcc-max()-Y
* tGravityAcc-max()-X
* tGravityAcc-energy()-X

This analysis helped identify which sensor-derived features contributed more to the model’s classification decisions.

Limitations

The dataset has several limitations. It was collected from only 30 participants, so the results may not generalize to all users. It also contains only six predefined activities and was collected using a specific smartphone and sensor configuration.

Tools & Libraries
* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab
* GitHub

Project Goal

The main goal of this project was to understand the complete machine learning workflow, from dataset exploration and preprocessing to model training, evaluation, and feature importance analysis.
The project also provided practical experience with sensor data, classification algorithms, exploratory data analysis, and machine learning evaluation.
