# Neural_Network_Charity_Analysis

## Overview of the analysis: Explain the purpose of this analysis.
The purpose of this project is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by nonprofit foundation Alphabet Soup. This analysis will help to ensure that the foundation money being used properly and effectively. This neaural network ML algorithms are capable of interpreting large complex datasets. In our analysis, a CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Using this dataset, determine whether future charitable organisations will be successful if funded. For this analysis we need to clean and preprocess the data and decide what data is beneficial for the model accuracy.

## Resources
Dataset Charity_data.csv  
Jupyter notebook   
Python   
Scikit-learn  
TensorFlow  
Pandas  

## Result
### Data Preprocessing
#### What variable(s) are considered the target(s) for your model?
   Within the given dataset, the target data is "IS_SUCCESSFUL" column (1 for "YES" and 0 for "No")

#### What variable(s) are considered to be the features for your model?  
   Following are considered to be the features for the model,  
    APPLICATION_TYPE           
    AFFILIATION                  
    CLASSIFICATION              
    USE_CASE                    
    ORGANIZATION                
    STATUS                      
    INCOME_AMT                  
    SPECIAL_CONSIDERATIONS      
    ASK_AMT                   
    IS_SUCCESSFUL    

#### What variable(s) are neither targets nor features, and should be removed from the input data?  
   Identification number and the names of the organization were not helpful within our dataset so they were removed.


### Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
* Selected 200 neurons for the first layer and 90 neurons for the second layer(first layer should have atleast double the amount of input features).

* I used 2 layers, tried with 3rd layer which didn't contribute to the improvement of the ML model. Adding layers doesn't guarantee for the better performance. Adding more hidden layers will only increase the chance of overfitting the training data depending on the complexity of the input data. 

* Used "relu" activation function for the input features beacause relu is generally a good activation function for the complex dataset which has numerous inputs and "sigmoid" for the output layer.

#### Were you able to achieve the target model performance?
   Yes, after a few configurations I could achieve the target model performance.


|    Accuracy before optimization        |  Accuracy after optimization |
:--------------------------------------:|:---------------------------------------:
![](images/original_result.png?raw=true)|![](images/optimized_result.png?raw=true)

#### What steps did you take to try and increase model performance?
Tried following steps to increase the model performance but didn't get the considerable change in accurancy.
* Tried adding additional hidden layers and increasing the number of neurons to the neural network model. 
* Tried different the activation functions. 
* Changing the number of epochs in the training.

Finally tried following changes in the model to improve the performance.
* Added "NAME" column which was skipped in the prprocessing.
* Tried binning the NAME values.   
* Increased the number of neurons for the first layer from 80 to 200 and for the second layer from 30 to 90.

The model accuracy improved from 72.46% to 76.87% .

## Summary   
#### Summary of the result  
The model result shows how well the model does with the given dataset and how we build the model. So our model tells us the loss score is 52.47% and accuracy score is 76.87%. Though we increased the accuracy score more than 75%, the loss score is still high. 

#### Recommendations for further analysis   
I recommend using SVM or ensemble model as we are considering target data as binary results. We should also look for the outliers. 
 
