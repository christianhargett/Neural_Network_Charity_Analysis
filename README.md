# Neural_Network_Charity_Analysis

## Overview

In this project we are attempting to create a binary classifier that is capable of predicting whether applicants will be successful if they receive funding from our client, Alphabet Soup. Our goal is to build a neural network that will take a dataset containing the applicants (provided by Alphabet Soup) which will make predictions based off of certain data points. 

## Results

### Data Processing
- Our target variable is the "IS_SUCESSFUL" column in our dataset. This column contains a value of either "0" or "1"; a score of "0" means that the company used the funding effectively while a "1" score means the company DID use their funds effectively.
- The datapoints that our neural network uses to determine if an applicant will be successful or not are called "features" Our feature variables are as follows: "APPLICATION_TYPE", "CLASSIFICATION", "AFFILIATION", "USE_CASE", "ORGANIZATION", "SPECIAL_CONSIDERATIONS", "INCOME_AMT".
- Variables that are neither targets nor features are as follows: "EIN" and "NAME". These are the first two columns in our dataset. These datapoints are purely unique identifiers for each applicant and bare no weight in our neural network model when determining successful applicants. These columns can be removed from our dataset.

### Compiling, Training, and Evaluating the Model
- In the neural network we used two hidden layers, the first with 60 neurons and the second with 20. I used the Rectified Linear Unit (ReLU) function in the hidden layers because it is the most used activation function in neural networks due to its simplifying output. Additionally, I used the sigmoid function for the output layer because our neural network needs to determine one of two outcomes (if an applicant will be successful or not).
- After several experiments, I was unfortunately unable to achieve the target model performance of 75%.
- In my attempts to optimize my model's performance, I adjusted the binning for appplication type and classification values so that more datapoints were included in the "Other" bin. I also increased the number of neurons in my model to 80 for the first layer and 40 for the second layer. Lastly, I doubled the number of epochs from 100 to 200. None of my attempts made a sufficient impact on making the model more optimal.
