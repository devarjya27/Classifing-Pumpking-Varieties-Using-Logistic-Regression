# Pumpkin Classification Model

This repository contains a logistic regression model that classifies pumpkins into two classes: **Ürgüp Sivrisi** and **Çerçevelik**. The model is trained and tested using datasets consisting of pumpkin features, including physical characteristics such as area, perimeter, and eccentricity.

## Dataset
* **Training Dataset:** `Gotem_Pumpkins.csv` contains labeled data for training the model.
* **Testing Dataset:** `Freyja_Pumpkins.csv` contains unlabeled data for testing the model.

Both datasets consist of the following features:

* Area
* Perimeter
* Major_Axis_Length
* Minor_Axis_Length
* Convex_Area
* Equiv_Diameter
* Eccentricity
* Solidity
* Extent
* Roundness
* Aspect_Ratio
* Compactness

The **Class** column denotes the type of pumpkin (Ürgüp Sivrisi or Çerçevelik) in the training dataset, while the test dataset only includes the features for prediction.

## Steps

### Data Preprocessing:
* The Unnamed: 0 column is dropped from both the training and testing datasets.
* Missing values are removed from the datasets.
* The Class column in the datasets is encoded to binary values: Ürgüp Sivrisi as 0 and Çerçevelik as 1.
* Z-score normalization is applied to the numerical features for both training and testing datasets to standardize the features to have a mean of 0 and a standard deviation of 1.

### Model Implementation:
* A logistic regression model is implemented from scratch using a custom sigmoid function and gradient descent optimization.
* The model is trained for `5000` iterations with a learning rate of `0.006`.

### Prediction:
* Predictions are made on the training and testing datasets using the learned weights and bias from the logistic regression model.

### Evaluation:
* Accuracy is calculated for both the training and testing datasets by comparing the predicted classes with the actual classes.
* A confusion matrix is generated and visualized using a heatmap to assess the model's performance in distinguishing between the two classes.
