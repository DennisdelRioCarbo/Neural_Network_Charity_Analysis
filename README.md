# Neural_Network_Charity_Analysis

## Overview
The purpose of this analysis is to help the  Alphabet Soup Charity foundation predict where to make successful investments.

From Alphabet Soup, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

Using machine learning and neural networks, we’ll use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results

- Data Preprocessing
  - What variable(s) are considered the target(s) for your model?
    - **IS_SUCCESSFUL** -Was the money used effectively
  
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
  For our first model (**nn model**) we selected *2 hidden layers* with **80** neurons in the first layer and **30** neurons in the second layer. We used the *relu* activation function as it seemed to work better when we have several inputs. For our *output layer* we used the *sigmoid* activation function with a single neuron. This first model served as exploratory and as a base line to see what level of accuracy we could get and try to increase model performance if necessary. 
  
  ![image](https://user-images.githubusercontent.com/104289098/189547613-a1f033bb-06a9-4b44-86ab-6183de62dca0.png)

  - Were you able to achieve the target model performance?
    No, despite several attempts to increase model performance the highest level of *accuracy* we were able to reach was 66%.
    
    **nn model**
    
    ![image](https://user-images.githubusercontent.com/104289098/189547488-86461833-e379-42f3-85d6-e090e651ab93.png)

  - What steps did you take to try and increase model performance?
  - The first step was trying to detect any outliers in the dataset, specifically in the *Funding amount requested* **ASK_AMT** where we noticed a big discrepancy between the mean and the third quartile. We adjusted and dropped some of the extreme values hoping that this would help training the model better. Once we did this we made three attemtps to increase the model perfomance.
  
  1. **nn1 model** We increased the number of neurons in the *first hidden layer* from **80** to **120** and in the *second hidden layer* from **30** to **80**. We kept 2 hidden layers with the *relu* activation, **50** *epochs*, and 1 *output layer* with *sigmoid* activation. There was no substantial increase in *accuracy*.
  
  ![image](https://user-images.githubusercontent.com/104289098/189546396-6b2f656c-59ba-495e-aca9-01cdd00c8185.png)
  
  ![image](https://user-images.githubusercontent.com/104289098/189547239-1665ed0f-aecf-4a14-a8f9-f2dde1c9d859.png)

  2. **nn2 model** We increased the number of *hidden layers* to 6, with *relu* activation,**50** *epochs* and 1 *output layer* with *sigmoid* activation. No increase in *accuracy*.
  
  ![image](https://user-images.githubusercontent.com/104289098/189546438-9fd507db-a162-4a65-a2d9-e0d4616ccd76.png)
  
  ![image](https://user-images.githubusercontent.com/104289098/189547264-1340d0b6-feea-4f5c-959f-48ff2c71ce4e.png)
 
  3. **nn3 model** We kept the 6 *hidden layers* with the same number of *neurons*, **50** *epochs* and 1 *output layer* with *sigmoid* activation. This time we changed the activation function in the *hidden layers* to *tanh*. Again no increase in *accuracy*

  ![image](https://user-images.githubusercontent.com/104289098/189546784-e953c406-0164-4dbd-af1c-24f6485d819d.png)

  ![image](https://user-images.githubusercontent.com/104289098/189546567-a970afeb-07cb-4b0a-a975-6e14b4313b65.png)
  
  ![image](https://user-images.githubusercontent.com/104289098/189547300-763a9d99-86de-4c35-b8ca-8af47061a115.png)


## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.


