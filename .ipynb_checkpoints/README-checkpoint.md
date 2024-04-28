# 21-deep-learning-challenge

Overview: The purpose of this analysis was to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

Results:

Data Preprocessing

What variable(s) are the target(s) for your model?
* IS_SUCCESSFUL
  
What variable(s) are the features for your model?
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* SPECIAL_CONSIDERATIONS
  
What variable(s) should be removed from the input data because they are neither targets nor features?
* INCOME_AMT
* ASK_AMT
  
Compiling, Training, and Evaluating the Model
 
How many neurons, layers, and activation functions did you select for your neural network model, and why?
* Neurons Layer 1 - 64; Layer 2 - 96; Output Layer - 1
I increased the number of neurons in each layer to allow the model to learn more complex patterns.
* Layers - 3
Increasing the number of layers to 4 did not improve the accuracy of the model, so I kept the layers to 3.
* Activation functions - relu and sigmoid
Relu - ReLU is a simple and effective activation function that introduces non-linearity to the network.
Sigmoid - Sigmoid is often used in the output layer of binary classification problems because it squashes the output values between 0 and 1, which can be interpreted as probabilities.

Were you able to achieve the target model performance?
* I was not able to achieve the target model performance even after removing a variable (SPECIAL_CONSIDERATIONS) and using the activation function tanh.

What steps did you take in your attempts to increase model performance?
* To increase model performance, I increased the number of neurons in each layer.
  
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Overall, the results of this model were less than satisfactory because the model did not meet the 75% accuracy goal. I would recommend combining this model with another model to solve the classification problem. For instance, this model could be combined with a logistic regression model. The models can be trained separately before combining the predictions with a simple voting scheme. If both models predict success, than the applicant is very likely to be successful if funded by Alphabet Soup. If both models predict fail, than the applicant is not likely to be successful. If the models don't agree, than there is a 50-50 chance the applicant will be successful. This new model might improve accuracy of the analysis.