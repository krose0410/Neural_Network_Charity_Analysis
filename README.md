# Neural_Network_Charity_Analysis
## Overview
The purpose of this analysis is to use machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. This was accomplished using SKLearn and TensorFlow.

## Results
### Data Preprocessing
The following steps were taken to preprocess the data for the neural network model:
- Target variable was identified as IS_SUCCESSFUL
- Features were identified as all columns except IS_SUCCESSFUL and EIN
- The following columns were removed from the features:
  * EIN
  * NAME

### Compiling, Training, and Evaluating the Model
The following steps were taken to compile, train, and evaluate the model:

- The neural network model was created using the following parameters:
  * 2 hidden layers
  * 80 nodes in the first hidden layer
  * 30 nodes in the second hidden layer
  * relu activation function
  * 100 epochs

<img width="716" alt="Fig1a" src="https://user-images.githubusercontent.com/109715441/216853268-a3c48b2a-8e5d-458e-acc9-ee085578b8d5.png">
<img width="890" alt="Fig1b" src="https://user-images.githubusercontent.com/109715441/216853294-776e58c3-9243-482b-b054-9a27949ed8df.png">
<img width="804" alt="Fig2a" src="https://user-images.githubusercontent.com/109715441/216853302-64bbdacd-2324-44fa-a81e-1b362ab048ed.png">
<img width="893" alt="Fig2b" src="https://user-images.githubusercontent.com/109715441/216853311-0dc077d2-1158-4bef-ad65-0f4a21e35586.png">

- The target accuracy of 75% was not achieved, the final accuracy score was 72.3%. All of the following steps taken to improve the model resulted in accuracy scores within less than 1% of each other
- Steps taken to improve the model consisted of variations of the following:
  * Adding a third and fourth hidden layer
  * Increasing the number of nodes in the first and second hidden layers to 150 and 75 respectively
  * Changing the activation function to leaky_relu and elu
  * Changing the number of epochs to 120
  * Changing the number of applications and classification counts from 500 to 1000 and 2000   to 4000 respectively
  
<img width="1072" alt="Fig3" src="https://user-images.githubusercontent.com/109715441/216853401-ba429441-27f4-4f14-b454-1f044fe22f55.png">
<img width="932" alt="Fig4a" src="https://user-images.githubusercontent.com/109715441/216853451-ec88e82a-d717-437d-8fdc-fa1859f8265d.png">

  <img width="619" alt="Fig4b" src="https://user-images.githubusercontent.com/109715441/216853458-3654c666-4f0e-492a-a536-68c645b04a40.png">

## Summary
The accuracy of the model was 72.3%, meaning that the model was able to predict the success of the applicants 72.3% of the time. This model was not able to meet the target accuracy of 75%. As this is a binary classification problem, it is possible that with sufficient data, a supervised machine learning model could be created that would be able to predict the success of the applicants with greater accuracy. It is also possible that the numerical difference between different applicants income and ask, which range from thousands to millions, is too large even with the scaling of the data.
