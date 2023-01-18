# Neural_Network_Charity_Analysis

## Overview of the analysis: 

The purpose of the analysis is to identify and predict by evaluating potential applicants who would be successful if funding was presented to them. Deep learning models are applied to analyse the applicants by creating neural networks using TensorFlow platform.

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/Classification%20count.png)

## Results
•	**Data Preprocessing**

  - The target variable for your model is ‘Is_Successful’ column
  - ‘Application Type, Affiliation, Classification, Use Case, Organization, Status, Income Amount, Special Considerations, and Ask Amount’ are considered feature        variables for the model
  - Columns 'EIN' and 'Name' are neither targets nor features and should be removed from the input data.

•	**Compiling, Training, and Evaluating the Model**

  - In the original neural network model, there were 2 hidden with 80 neurons in the first layer and 30 neurons in the second layer. ‘Relu’ activation function was used for both the hidden layers as we were looking for positive values and ‘Sigmoid’ activation function was used for the output layer, as we were looking for probability between 0 and 1. The model was trained using 100 epochs.

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/org%20layers.JPG)

  - The model was able to get an accuracy of 73.07%.

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/Original.JPG)

Numerous efforts were made to optimize and improve model’s performance to 75% :

•	**Attempt 1 :** 

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/1-accuracy.JPG)

An accuracy rate of 72.51% was attained while trying for the first time to optimize accuracy to 75% or higher. Increased the number of hidden layers to 3 and having 80,40 & 20 in the respective layers while having the activation function ‘Relu’. The epoch was set at 100. Changed the training and testing dataset setting for random_state from zero value to 78.  

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/1-%20layers.JPG)

•	**Attempt 2 :** 

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/2-accuracy.JPG)

An accuracy rate of 71.83% was achieved on the second attempt which is lower than the earliest model. Removed more columns such as 'EIN','NAME' and "USE_CASE" and increased(4,000 instead of 500) the number of bins for application_type. The model’s weight was saved every 5 epochs. Keeping the hidden layers as 3, we used the activation function as ‘Relu’ for the hidden layers 1 & 2 and used ‘Tanh’ for the third hidden layer.

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/2-%20layers.JPG)

•	**Attempt 3 :** 

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/3-accuracy.JPG)

An accuracy rate of 72.41% was achieved on the third attempt which is lower than the original model. We increased the number of hidden layers to 4 instead of 2 and also the number of neurons (with the following number of neurons for each layer respectively from 1 to 4 : 80-60-40-30) keeping the activation function as ‘’relu’ for all the hidden layers. To add, we also increased the epochs to 200 from 100.

![This is an image]( https://github.com/Josna-Aykkara/Neural_Network_Charity_Analysis/blob/main/Image/3-%20layers.JPG)

Multiple attempts were made to optimize the model to achieve an accuracy of 75% or higher and unfortunately failed. 

## Summary

The neutral network model is 73.07% accurate, which is the best result so far. This is not ideal since we wanted a 75% accuracy at a minimum. Hence this simulation requires to have some additional modifications. 

Recommendation would be to increase the total epochs to the training regiments, increase the number neurons to the layers, or reducing the number of bins, as it would help to increase the accuracy rate for the model. Additionally, its better to use the ‘relu’ activation function as it would provide better results (based on the attempts made).
