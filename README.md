# Neural Network Charity Analysis

## Overview 

The project is to analyse charity funding data of Alphabet Soup and train a model to predict for a given applicant that whether it will be a successful candidate or not. For this, Neural network model is used and tried to train the model on available data of 34000 different organization which have sought funding from Alphabet soup in past. 

## Purpose

The purpose of this analysis is to create a binary classification model to predict whether an applicant will be successful if funded by Alphabet Soup.


## Results

### Data Pre-processing

Variable considered target for the model:  **IS_SUCCESSFUL**

Variables considered to be features for the model: **All variables except IS_SUCCESSFUL & SPECIAL_CONSIDERATIONS_Y for optimization**

Variables are neither targets nor features, and removed from the input data: **EIN, NAME & SPECIAL_CONSIDERATIONS_Y **

### Compiling, Training, and Evaluating the Model: 

#### Initial Run:

Layers: 2 Hidden and 1 Output Layer

Layer #1: * Neurons: * 80 * Activation Function: * Relu (Computationally more effective)

Layer #2: * Neurons: * 30 * Activation Function: * Relu (Computationally more effective)

Output Layer: * Activation Function: * Sigmoid (Seeking classification output) 

![](Resources/images/ss1.png)

Model performance: Accuracy is at 73% and is below 75% the target model performance


Steps to increase model performance: 

3 Different model setting were tried, however failed to achieve the target performance

#### 1st Optimization Run:

Pre-processing change: Removed SPECIAL_CONSIDERATIONS_Y feature  as it seems to be redundant with SPECIAL_CONSIDERATIONS_N

Layers: 2 Hidden and 1 Output Layer

Layer #1: * Neurons: * 80 * Activation Function: * Relu (Computationally more effective)

Layer #2: * Neurons: * 30 * Activation Function: * Relu (Computationally more effective)

Output Layer: * Activation Function: * Sigmoid (Seeking classification output)

![](Resources/images/ss2.png)

Model performance: Accuracy is at 72.5% and is below 75% the target model performance


#### 2nd Optimization Run:

Pre-processing change: No change from previous run

Layers: 2 Hidden and 1 Output Layer * (No Change) *

Layer #1: * Neurons: * 90 * Activation Function: * Relu (Computationally more effective)

Layer #2: * Neurons: * 50 * Activation Function: * Relu (Computationally more effective)

Output Layer: * Activation Function: * Tanh (Ranges from -1 to 1, so negative inputs will be mapped strongly)

![](Resources/images/ss3.png)

Model performance: Accuracy is at 72% and is below 75% the target model performance. Performance is reduced as compared to previous runs.

#### 3rd Optimization Run:

Pre-processing change: No change from previous run

Layers: 3 Hidden and 1 Output Layer 

Layer #1: * Neurons: * 80 * Activation Function: * Relu (Computationally more effective)

Layer #2: * Neurons: * 30 * Activation Function: * Relu (Computationally more effective)

Layer #3: * Neurons: * 10 * Activation Function: * Relu (Computationally more effective)

Output Layer: * Activation Function: * Tanh (Ranges from -1 to 1, so negative inputs will be mapped strongly)

![](Resources/images/ss4.png)

Model performance: Accuracy is at 72.3% and is below 75% the target model performance. 


## Summary

The model achieved the highest accuracy of approximately 73%. However, it failed to cross the target model performance of 75%. On trying to optimize the model by adding more neurons or hidden layers, accuracy remained below the initial run.  We may need more data to train our neural network model more accurate or we may have to choose another technique. Random forest classification could also be could option with the available data, as it could have sufficient number of estimators and tree depth. It may assist in avoiding over fitting of model in case if make more data available to train neural network model.
