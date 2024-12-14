# Credit-Card-Fraud-Detection-using-Autoencoders-in-Keras

# Overview
This project explores the implementation of a Deep Autoencoder, built with Keras, to identify fraudulent credit card transactions. The model is trained exclusively on normal (non-fraudulent) transactions, learning to reconstruct their patterns. Transactions with high reconstruction errors are flagged as potential fraud.

# Features
•	Comprehensive preprocessing of credit card transaction data.

•	Visualization of data distributions to gain insights.

•	Application of a Deep Autoencoder for anomaly detection.

•	Model evaluation using metrics such as ROC-AUC and Precision-Recall.

•	Graphical analysis of results, including confusion matrices, ROC curves, and reconstruction errors.

# Requirements
To run this project, you will need the following Python libraries:

•	pandas

•	numpy

•	matplotlib

•	seaborn

•	sklearn

•	tensorflow

•	keras

•	scipy

# Dataset
The dataset utilized is a credit card transaction dataset available in Data folder in main branch.

# Dataset Columns
•	Time: Time elapsed since the first transaction.

•	Amount: The transaction amount.

•	Class: Labels denoting normal (0) or fraudulent (1) transactions.

# Workflow
1.	Import Libraries
    o	Import necessary libraries and set visualization preferences.
2.	Load and Explore Dataset
    o	Load the dataset using pandas.
    o	Check for missing values and analyze the distribution of the Class column.
3.	Data Visualization
    o	Visualize the distribution of transaction classes. 
    o	Create histograms for transaction amounts and scatter plots for time vs. amount, categorized by class.
4.	Data Preprocessing
    o	Normalize the Amount column using StandardScaler.
    o	Exclude the Time column.
    o	Split the dataset into training (normal transactions) and testing datasets.
5.	Model Implementation
    o	Design the Autoencoder with encoding and decoding layers.
    o	Use mean squared error as the loss function.
    o	Save the best model using ModelCheckpoint.
6.	Training
    o	Train the Autoencoder on normal transactions and validate its performance on the test set.
7.	Evaluation
    o	Identify fraudulent transactions by analyzing reconstruction errors.
    o	Plot the ROC curve, Precision-Recall curve, and reconstruction error distributions.
    o	Calculate the confusion matrix and derive performance metrics.
# Results
•	Model Performance: The Autoencoder effectively identified fraudulent transactions by detecting anomalies in reconstruction patterns.
•	Visual Outputs:
    o	Distribution of transaction classes.
    o	Reconstruction error distributions.
    o	ROC curve and Precision-Recall curve.
    o	Confusion matrix.
# Key Files
•	Model Checkpoints: model.keras
•	Generated Visualizations:
    o	transaction_class_distribution.png
    o	Amount_per_transaction_by_class.png
    o	Time_vs_Amount_by_class.png
    o	ROC_Curve.png
    o	Precision_vs_Recall.png
    o	Confusion_Matrix.png
# Conclusion
This project demonstrates the feasibility of detecting fraudulent transactions by leveraging Autoencoders to model patterns in normal transactions. While this implementation is a foundational demonstration, further tuning and advanced methods can improve its accuracy and applicability.
# Acknowledgments
The project draws inspiration from the principles of anomaly detection using Autoencoders. Special thanks to the dataset providers for making this exploration possible.
# How to Run
1.	Clone this repository.
2.	Install the necessary Python libraries.
3.	Update the dataset file path in the script.
4.	Execute the script to train the model and generate results.
# License
This project is licensed under the MIT License.

