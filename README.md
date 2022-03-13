# Neural_Network_Charity_Analysis

## Overview

  The current project was conducted for the non-profit organization Alphabet Soup. This organization raises and then donates money to organizations that work to protect the environment, improve peoples' well-being, and unify the world. The purpose of this project was to develop a neural network model that would accurately predict which organizations would be successful if funded by Alphabet Soup.

## Results

#### Data Preprocessing
Numeric features were scaled using the standard scalar, and categorical features were converted to numeric values using one-hot encoding. In additon, Application_Type and Classification were binned.

Target Variable: Is_Successful
Feature Variables: Application_Type, Affiliation, Classification, Use_Case, Organization, Status, Income_AMT, Ask_AMT
Removed Variables: EIN, Name, Special_Considerations


#### Compiling, Training, and Evaluating the Model
For all of the models: ReLU activation was used for the hidden layers as it is the most commonly used, and is less susceptible to vanishing gradients as with Sigmoid or Tanh. A Sigmoid activation function was used for the output as the goal of the model was binary classification.

#### Original Model:
Hidden Layers:
Layer 1: 80 neurons, ReLU activation
Layer 2: 30 neurons, ReLU activation
Output Layer: Sigmoid activation
80 Neurons were chosen for the first layer because that is approximately twice the number of features, then roughly half of that number of neurons were used for the second layer. NOTE: This original model still included the Special_Considerations feature.

## Summary
  Despite 3 attempts at optimization, the model accuracy never reached the 75% target accuracy. Another option to a neural network model is a random forest classifier model. For example, when this data was analyzed using a random forest classifier model, the resulting accuracy was 71%. This is comparable to the 72.7% accuracy of the neural network model, and the forest model ran in a fraction of the time that was required for the neural network model to run. In addition, the forest model required less code. Because of the faster performance and simplicity, I would recommend that Alphabet Soup use a random forest classifier model in the future.  
