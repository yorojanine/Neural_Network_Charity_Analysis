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
Finally at the output layer, 1 neuron was applied using the sigmoid activation function to produce a probability output.<br>

![](resources/dev2_inputs.PNG)

*Were you able to achieve the target model performance?*<br>
The model's target performance was to achieve an accuracy of higher than 75%. After running the initial input, the model was shy of roughly 2.5% and only achieved **72.54%** accuracy.

![](resources/originalAccuracy.PNG)

### Deliverable 3: Optimization
*What steps did you take to try and increase model performance?*<br>
Since the original model missed its mark of achieving the desired 75% accuaracy target, three different approaches were taken in order to optimize the model.

1) **Adding an additional hidden layer and setting the hidden nodes to 20.** - At the chance the model may be underfitting, I felt adding an additional layer would be able to address that issue. Unfortunately, this attempt showed minimal improvements. In fact, it lowered the accuracy of the model to **72.40%**.<br>
![](resources/attempt1.PNG)

2) **Add more nuerons to the original two layers.** - Since adding the additional layer lowered the model's accuracy, I decided to remove the added hidden layer and continue with the original two layers. Because the number of nuerons can also be a factor in over/underfitting, I decided to increase the preset nuerons. By increasing the first hidden layer from 80 to 100 nuerons and the second hidden layer from 30 to 60, the goal was to again try and address any form of underfitting. Unfortunately, I came up still a little short from both the target goal and the original accuracy. While this model performed better than my first optimization attempt with **72.43%** accuracy, it still wasn't enough.
![](resources/attempt2.PNG)

3) **Changing the activation function of all hidden layers**. - Finally, with the last attempt at optimization, I decided to keep the number of nuerons from the second attempt since it did have some marked improvements. In addition, I wanted to see if changing the activation function would make any difference to the model performance. Hence, all the activation functions at all layers (first, second, and output) were changed from "relu" to "sigmoid". Based on the results, changing activation functions made no improvements to the accuracy score and stayed at **72.43%**.<br>
![](resources/attempt3.PNG)

Furthermore, as we can see from the results, all attempts to optimize the model failed without any marked improvements to the original model.

### Challenges

Working with the dataset, I ran into a few challenges. (1) Unable to achieve optimization. In addition, I noticed a slight difference when I copied the `AlphaetSoupCharity.ipynb` and built upon the code with `AlphaetSoupCharity_Optimization.ipynb`. With the optimization code, I added all my attempts for enhancement. However, when I ran the whole notebook through as one swoop, I noticed that the accuracy of the "initial" model showed slight improvement from 72.54% to 72.61% . 
![](resources/accuracyChallenge.PNG)
<br> To me, it was interesting to see that shift as there is no difference between the two notebook codes.


## Summary
*Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.*
