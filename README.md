![image](https://thomsonlab-webpage-files.s3.amazonaws.com/media/original_images/Banner-AI-2.jpg)

# Neural_Network_Charity_Analysis

## Background 

Alphabet Soup Foundation is a non-for-profit philanthropic foundation that invests in, and donates to, organizations which protect the environment, promote people's wellbeing and unify the world. The purpose of this challenge is to help the Foundation predict where to make investments using  machine learning and neural networks tehcniques. 

Using a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years, we will create a binary classifier using nerual network design that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. We will analyze the impact of each donation and vet potential recepients to ensure the foundation's money is being used effectively and in an impactful manner. 

The various steps involved in this exercise include:

* Preprocessing Data for a Neural Network Model
* Compile, Train, and Evaluate the Model
* Optimize the Model

## Results: 

### Data Preprocessing

**What variable(s) are considered the target(s) for your model?**

The target for the model is the "Is-Successful" column, reflecting if the funds were used effectively by the business. This is what Alphabet Soup is trying to predict using the model - whether potential recepients will be successful if funded. 

**What variable(s) are considered to be the features for your model?**

The features of this model are the NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT.

**What variable(s) are neither targets nor features, and should be removed from the input data?**

EIN (Employer identificaiton) and NAME were dropped because the numbers could confuse the system into thinking its significant. For the optimization exercise, I also dropped SPECIAL_CONSIDERATIONS because there is only a small percentage of cases that had any special consideration.

### Compiling, Training, and Evaluating the Model

**How many neurons, layers, and activation functions did you select for your neural network model, and why?**
For the initial model (deliverable 2), we used 2 hidden layers with 80 and 30 neurons respectively.
The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, we used the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
**These steps gave us an accuracy of 72.6%**

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt_summary.PNG)

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/attempt_accuracy.PNG)

**Were you able to achieve the target model performance?**

No

**What steps did you take to try and increase model performance?**

To improve model performance, I made the following adjustments:

**Attempt 1: Dropped 2 noisy variables "SPECIAL_CASE_Y and SPECIAL_CASE_N**

This did not improve accuracy, which was around 72.5%.

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_summary.PNG)

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt1_accuracy.PNG)

**Attempt 2: Dropped noisy variables as above, added a hidden layer and added more neurons to hidden layers**

Adding another hidden layer and adding more neurons to the hidden layers again did not improve the model accuracy, which was around 72.4%

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt2_summary.PNG)

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt2_accuracy.PNG)

**Attempt 3: Dropped noisy variables as above, added a hidden layer, added more neurons to hidden layers and used different activation functions for hidden layers**

In addition to the attempt 2, I used different activation functions in the hidden layer but again, the accuracy remained around 72.5%

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt3_summary.PNG)

![image](https://github.com/amberwnaushahi/Neural_Network_Charity_Analysis/blob/main/Images/Attempt3_accuracy.PNG)

## Summary: 

The deep learning neural network model did not reach the target of 75% accuracy despite attempts at optimization. We could further optimize our neural network by removing more features or adding more data to the dataset to increase accuracy.

We could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model. This is because random forest is a robust and accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks and can avoid the data from being overfitted.

