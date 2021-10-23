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

I chose a number of different neurons/layers/activation function combinations for the model following various rules of thumb (see the included [folder](https://github.com/jzebker/Neural_Network_Charity_Analysis/tree/main/Deliverable%203%20Opt)).  My accuracy value hovered around 72-73% regardless of the numbers of neurons and hidden layers I picked.  I went with a relu function for the hidden layers and a sigmoid function for the output layer.  The specific numbers are pictured below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/84994321/138534800-7b8185a6-f8e1-4aa1-b09c-6b1945b6d5ad.png">
</p>

• Were you able to achieve the target model performance?

Nope.

• What steps did you take to try and increase model performance?

Different attempts included the following - one at a time was altered to see how it affected performance but changes seemed to either lower performance or make no appreciable difference:

1) Re-binning the [ASK_AMT](https://github.com/jzebker/Neural_Network_Charity_Analysis/blob/main/Deliverable%203%20Opt/D3Pics/ASK_AMT_bucket.png) and [INCOME_AMT](https://github.com/jzebker/Neural_Network_Charity_Analysis/blob/main/Deliverable%203%20Opt/D3Pics/INCOME_AMT_bucket.png) columns (each separately and [together](https://github.com/jzebker/Neural_Network_Charity_Analysis/blob/main/Deliverable%203%20Opt/AlphabetSoupCharity_Optimization_ASK_AMT_INC_AMT_Bucket.ipynb))

2) Dropping the ASK_AMT column

        # Drop the non-beneficial ID columns, 'EIN' and 'NAME' and 'ASK_AMT'.
        application_df = application_df.drop(['EIN', 'NAME', 'ASK_AMT'], axis=1)

3) Adding different numbers of neurons (tried different rules of thumb ranging from 1/2 number of input features to greater than the number of input features)

<p align="center">
  <img src="https://github.com/jzebker/Neural_Network_Charity_Analysis/blob/main/Deliverable%203%20Opt/D3Pics/Add_Neurons.png?raw=true" width=500>
</p>

4) Adding hidden layers

<p align="center">
  <img src="https://github.com/jzebker/Neural_Network_Charity_Analysis/blob/main/Deliverable%203%20Opt/D3Pics/Add_Hidden_Layer.png?raw=true" width=500>
</p>

5) Changing activation functions

<p align="center">
  <img src="https://github.com/jzebker/Neural_Network_Charity_Analysis/blob/main/Deliverable%203%20Opt/D3Pics/Change_Activation.png?raw=true" width=500>
</p>

## Summary
I was unable to get the accuracy of the model above ~73%.  It should be noted that there is a static amount of data with relatively few features and we were looking at whether or not a charitable donation was successful or not.  I would recommend an unsupervised model that would hopefully show associations between different values or use clustering instead of taking into account the binary IS_SUCCESSFUL values in the data set.
