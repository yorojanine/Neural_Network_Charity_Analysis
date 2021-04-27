# Neural_Network_Charity_Analysis

## Purpose
The purpose of this challenge was to apply what we've learned about machine learning and **nueral networks**. Based on the features within the dataset, a binary classifier will be created in order to predict *whether applicants will be successful if funded by Alphabet Soup*. The goal is to use the skills learned from the module to help the foundation predict where to make investments.

## Analysis/Results
The provided dataset used in this analysis is a [CSV](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-online/module_19/charity_data.csv) "containing more than 34,000 organizations that have received funding from Alphabet Soup over the years." 

Stepping through the deliverables, the following tasks will be performed on the data:
1. Preprocessing the data for a Nueral Network Model
2. Compile, Train and Evaluate the Model
3. Optimize the Model

### Deliverable 1: Data Preprocessing
*What variable(s) are considered the target(s) for your model?*<br>
For this model, the **IS_SUCCESSFUL** column stands as the target variable. The column denotes whether the money was used effectively.

*What variable(s) are considered to be the features for your model?*<br>
The following variables have been considered as features for the model:<br>
* APPLICATION_TYPE—Alphabet Soup application type<br>
* AFFILIATION—Affiliated sector of industry<br>
* CLASSIFICATION—Government organization classification<br>
* USE_CASE—Use case for funding<br>
* ORGANIZATION—Organization type<br>
* STATUS—Active status<br>
* INCOME_AMT—Income classification<br>
* SPECIAL_CONSIDERATIONS—Special consideration for application<br>
* ASK_AMT—Funding amount requested<br>

*What variable(s) are neither targets nor features, and should be removed from the input data?*<br>
**EIN** and **NAME** were flagged as neither a target nor a feature and were essentially dropped from the input data. Both variables were identification columns for the dataset and marked as ineffectual in the model's prediction capability. 

### Deliverable 2: Compiling, Training, and Evaluating the Model
*How many neurons, layers, and activation functions did you select for your neural network model, and why?*<br>

In using the nine features listed above, the nueral network model has been set for two hidden layers.<br>
At the first hidden layer, 80 neurons were the selected input based on the provided code using the relu activation function.<br>
At the second hidden layer, also based on the provided code, 30 neurons were the selected input using the relu activation function. <br>
The relu activation was used as it handles non-linear data and simplifies output better than other activation functions.<br>
Finally at the output layer, 1 neuron was applied using the sigmoid activation function because sigmoid is set to produce a probability output.<br>

![](resources/dev2_inputs.PNG)

*Were you able to achieve the target model performance?*<br>
The model's target performance was to achieve an accuracy of higher than 75%. After running the initial input, the model was shy of roughly 2% and only achieved 72.61% accuracy. 

![](resources/originalAccuracy.PNG)

### Deliverable 3: Optimization
*What steps did you take to try and increase model performance?*

<show all 3 steps>

### Challenges

<file_size><unable to obtain optimization>

## Summary
*Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.*
