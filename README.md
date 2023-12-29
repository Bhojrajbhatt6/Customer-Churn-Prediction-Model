# Customer Churn Prediction Model

This repository contains a Python script for building and training a customer churn prediction model using a neural network. The model is implemented using TensorFlow and Keras. The dataset used for training and testing is loaded from a CSV file named "Customer-Churn-Records.csv."

## Dataset Overview

The initial dataset contains the following columns:

- **CreditScore**: Credit score of the customer.
- **Geography**: Country of residence.
- **Gender**: Gender of the customer.
- **Age**: Age of the customer.
- **Tenure**: Number of years the customer has been with the bank.
- **Balance**: Current account balance.
- **NumOfProducts**: Number of bank products the customer uses.
- **HasCrCard**: Whether the customer has a credit card (1 for yes, 0 for no).
- **IsActiveMember**: Whether the customer is an active bank member (1 for yes, 0 for no).
- **EstimatedSalary**: Estimated salary of the customer.
- **Exited**: Whether the customer exited the bank (1 for yes, 0 for no).

## Data Preprocessing

1. **Handling Missing Values**: No missing values were found in the dataset.
2. **Handling Duplicate Values**: No duplicate rows were found in the dataset.
3. **Feature Selection**: Unnecessary columns such as 'RowNumber', 'CustomerId', 'Surname', 'Complain', 'Point Earned', 'Card Type', 'Satisfaction Score' were removed.

## Exploratory Data Analysis (EDA)

1. **Data Distribution**: The distribution of customers who stayed and exited the bank was visualized using a histogram.
2. **Correlation Heatmap**: A heatmap was created to visualize the correlation between different features in the dataset.

## Data Transformation

1. **Categorical Data Encoding**: The categorical columns ('Geography' and 'Gender') were one-hot encoded.

## Model Building

1. **Data Splitting**: The dataset was split into training and testing sets using a 80-20 split.
2. **Feature Scaling**: Standard scaling was applied to the numerical features.

## Neural Network Architecture

The neural network model was built using the following architecture:

- Input Layer: 11 neurons (corresponding to the number of features)
- Hidden Layer 1: 64 neurons, Sigmoid activation function
- Hidden Layer 2: 32 neurons, Sigmoid activation function
- Output Layer: 1 neuron, Sigmoid activation function

## Model Compilation and Training

The model was compiled using binary crossentropy loss and the Adam optimizer. It was trained for 10 epochs with a validation split of 20%.

## Model Evaluation

1. **Accuracy**: The model achieved an accuracy of 79.25% on the test set.
2. **Loss Reduction**: The training and validation loss reduction was visualized.

## Prediction and Thresholding

The trained model was used to make predictions on the test set, and a threshold of 0.5 was applied to convert the output into binary predictions.

## Conclusion

The customer churn prediction model demonstrates reasonable accuracy in identifying potential churners. Further optimization and fine-tuning of hyperparameters may enhance the model's performance.

