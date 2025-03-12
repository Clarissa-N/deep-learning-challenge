# deep-learning-challenge

## Repository Structure

**Analysis:**
  - **Analysis_Code:** File with code for the neural network.
  - **AlphabetSoupCharity.h5:** Results


## Overview

  The purpose of this analysis is to creat a model using machine learning, specifically deep learning, to predict whether an organization's application will be successful.The dataset contains records from organizations that recieved funding from Alphabet Soup, with features that also provide metadata about each organization.The target variable `IS_SUCCESSFUL` indicated whether the funding was used effectively (successful) or not (unsuccessful). The goal was to use all this information to train a neural network that can predict the success of future applications.

## Results

**Data Preprocessing:**

  - **Target Variable:**
    - The target variable for the model is `IS_SUCCESSFUL`, which is a binary variable that indicates whether the application for funding was successful(1) or not(0).

  - **Feature Variables:**
    - The inputs used by the model include columns such as APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, among others. These features capture metadata about each organization and their application.

  - **Variables to Remove:**
    - EIN and NAME were removed from the input data as they are identification columns that do not provide predictive value for the classification task.

**Compiling, Training, and Evaluating the Model**

- **Neurons, Layers, and Activation Functions:**

  - **Neurons and Layers:** There are 3 hidden layers. The first has 25 neurons and the second and third both have 16 neurons.

  - **Activation Functions:** The ReLU activation function was used in the hidden layers which allows the model to learn non-linear patterns in the data. The output layer uses a sigmoid activation functionc, which is great for binary classification as it outputs a probability score between 0 and 1.

  - **Justification:** After working through various optimations, this model of three hidden layers with 25 and 16 neurons was able to provide the best results. These specific activation funcitons were also chosen to help provide faster training and to reduce the likelihood of vanishing gradients.
 
**Model Performance:**
  - **Loss:** 0.56
  - **Accuracy:** 73.13%
  - **Target Performance:** While the target was to exceed 75%, the other requirement was to make at least three optimization attempts and I made around eight attempts before deciding to go with these final results.

**Steps Taken to Optimize the Model:**

  1. **Increased Hidden layers:** The starter code started with two hidden layers and after going though a couple trials of adding and taking away layers, I finalized adding a third layer in order to increase its capacity to capture complex relationships between features.
  2. **Neurons:** I went through several trials of increasing and decreasing neurons as well and finally landed on using 25 and 16.
  3. **Use of Dropout:** I did include droupout layers for a couple trials, but it tended to result in slightly lower accuracy so I went without them.


## Summary

  Overall, the deep learning model achieved and accuracy of 73.13%, which is a solid performance despite it falling slightly short of the target performance. A recommendation might be to use a more advanced model such as XGBoost or Random Forest as they are also well-known for their usefullness and effectiveness in classification tasks revolving around structured data. Another recommendation would be to simply continue optimizing the current model. There could continue to be more hyperparamater fine-tuning as well as maybe using cross-validation to reduce variance. With further refinement this model has the potential to meet the target of 75% accuracy and improve the Alphabet Soup nonprofit foundation's ability to predict successful applicants for funding.

