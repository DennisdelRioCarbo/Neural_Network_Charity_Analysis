# Neural_Network_Charity_Analysis

## Overview
The purpose of this analysis is to help the  Alphabet Soup Charity foundation predict where to make successful investments.

From Alphabet Soup, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Using machine learning and neural networks, we’ll use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results

- Data Preprocessing
  - What variable(s) are considered the target(s) for your model?
    - **IS_SUCCESSFUL** is our target variable
  
  - What variable(s) are considered to be the features for your model?
      - **APPLICATION_TYPE**—Alphabet Soup application type
      - **AFFILIATION**—Affiliated sector of industry
      - **CLASSIFICATION**—Government organization classification
      - **USE_CASE**—Use case for funding
      - **ORGANIZATION**—Organization type
      - **STATUS**—Active status
      - **INCOME_AMT**—Income classification
      - **SPECIAL_CONSIDERATIONS**—Special consideration for application
      - **ASK_AMT**—Funding amount requested
  
  - What variable(s) are neither targets nor features, and should be removed from the input data?
    - **EIN and NAME**—Identification columns
  
- Compiling, Training, and Evaluating the Model
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?
  
  
  - Were you able to achieve the target model performance?
    No, despite several attempts to increase model performance the highest level of *accuracy* we were able to reach was 50%.
    
    ![image](https://user-images.githubusercontent.com/104289098/189546239-c924231e-2638-4033-b460-ff17b7cb6bd3.png)

    
  - What steps did you take to try and increase model performance?
  1. We increased the number of neurons in the *first hidden layer* from **80** to **120** and in the *second hidden layer* from **30** to **80**. We kept 2 hidden layers with the *relu* activation and **50** *epochs*.
  
  ![image](https://user-images.githubusercontent.com/104289098/189546396-6b2f656c-59ba-495e-aca9-01cdd00c8185.png)

  2. We increased the number of *hidden layers* to 6, with *relu* activation and **50** *epochs*
  
  ![image](https://user-images.githubusercontent.com/104289098/189546438-9fd507db-a162-4a65-a2d9-e0d4616ccd76.png)
  
  3. We kept the 6 *hidden layers* with the same number of *neurons* and **50** *epochs*. This time changed the activation function to *tanh*.

  ![image](https://user-images.githubusercontent.com/104289098/189546784-e953c406-0164-4dbd-af1c-24f6485d819d.png)

  ![image](https://user-images.githubusercontent.com/104289098/189546567-a970afeb-07cb-4b0a-a975-6e14b4313b65.png)


## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
