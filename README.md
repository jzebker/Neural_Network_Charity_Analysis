# Neural_Network_Charity_Analysis
## Overview
Use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
## Results
**Data Preprocessing**

• the IS_SUCCESSFUL column is the ***target variable*** for the model

• APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are all ***features*** of the model

• I have ***removed*** EIN and NAME from the input data (and ASK_AMT in one version of the optimizations in deliverable 3)

**Compiling, Training, and Evaluating the Model**

• How many neurons, layers, and activation functions did you select for your neural network model, and why?

I chose a number of different neurons/layers/activation function combinations for the model largely because I was trying to figure out how it worked (see the included [folder](https://github.com/jzebker/Neural_Network_Charity_Analysis/tree/main/Deliverable%203%20Opt)).  My accuracy value hovered around 72-73% regardless of the numbers of neurons and hidden layers I picked.  I went with a relu function for the hidden layers and a sigmoid function for the output layer.  The specific numbers are pictured below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/84994321/138534800-7b8185a6-f8e1-4aa1-b09c-6b1945b6d5ad.png">
</p>

• Were you able to achieve the target model performance?

Nope.

• What steps did you take to try and increase model performance?
