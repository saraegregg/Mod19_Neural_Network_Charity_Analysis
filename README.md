# Module 19 Challenge

---
## Alphabet Soup Charity Analysis 
---

## Project Overview
Build and analyse a deep neural network machine learning model using information from more than 34,000 organizations that have received funding from Alphabet Soup over the years. The goal is to create a binary classifier that is capable of predicting with 75% accuracy whether applicants will be successful if funded by Alphabet Soup, which will guide the foundation about where to make investments.

## Challenge Objectives
Produce the following:
- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model
- Deliverable 4: A Written Report on the Neural Network Model (README.md)

## Resources
**Data Sources:** 
- charity_data.csv

**Software:**
- Python 3.9.7
- Visual Studio Code 1.67.1 
- Anaconda Navigator 1.9.0
- Jupyter Notebook 6.4.5


## Results 

### Data Preprocessing
**What variable(s) are considered the target(s) for your model?**
The target is the "is_successful" column in the dataframe, where a 1 denotes success and a 0 represents failure.

**What variable(s) are considered to be the features for your model?**
The variables that are features in the model include:
     - **Application Type**- the type of application submitted to Alphabet Soup
     - **Affiliation**- the affiliated sector of industry
     - **Classification**- the government organization classification
     - **Use Case**- the planned use case for funding
     - **Organization**- the type of organization receiving the funding
     - **Status**- the status of the project, active or inactive
     - **Income Amount**- the income classification of the applicant
     - **Special Considerations**- if there are special considerations attached to the application
     - **Ask Amount**- the funding amount requested

**What variable(s) are neither targets nor features, and should be removed from the input data?**
The dataframe also included two columns that were not used as features or targets: **EIN** and **Name**, the identification number and name columns.

### Compiling, Training, and Evaluating the Model
**How many neurons, layers, and activation functions did you select for your neural network model, and why?**

The initial model included two hidden layers, the first with 30 neurons and the second with 20 neurons. 30 neurons were chosen based on the idea of using roughly 3 times the number of input values, the second hidden layer was given 2/3 the number of neurons as the first layer, and ReLU was chosen because there are no negative values in the dataset and it does a better job with nonlinear data. 

**Were you able to achieve the target model performance?**
None of the models ach
No, none of the models achieved the target model performance level of 75% accuracy.

**What steps did you take to try and increase model performance?**
In an attempt to reach the 75% accuracy threshold, firstly I attempted to find and remove "noisy" variables by binning the applications by the ask amount. Then I built three additional models adjusting the number of neurons, the number of hidden layers, the activation functions. 

## Summary
After all the optimization attempts, none of the deep-learning neural network models achieved the desired accuracy rating of 75%. This might be from insufficient data preprocessing, not using the optimum activation funcion or not using the best amount of layers and neurons. I would recommend researching a script that searches for and applies the optimum hyperparameters, which would be much faster than manually adjusting the hyperparameters. Another option would be when fitting the model to add the argument to select the best weights found in an optimization attempt (instead of keeping whichever weights were generated on the 100th epoch) in the hopes that they would also improve performance on the test set. Should the model still not be performing adequately, looking at a SVN or random forest model might further improve the performance of the model.
