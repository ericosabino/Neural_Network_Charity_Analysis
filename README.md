# Neural Network Charity Analysis

From Alphabet Soup’s business team, CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years was received. Within this dataset are a number of columns that capture metadata about each organization.

The goal of this project is to create a model to define whether organizations will be succesful in getting funded by Alphabet Soup, based on this data.

I'll use the features in the provided dataset to help to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup, with my knowledge of machine learning and neural networks.

# Results

## What variable(s) are considered the target(s) for your model?

The target for the model is the "Is-Successful" variable. This column shows whwther the funds were used effectively by each organization, and it's also what Alphabet Soup is trying to predict using the model, for other organization.

## What variable(s) are considered to be the features for your model?

- NAME
- APPLICATION
- TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- STATUS
- ASK_AMT

## What variable(s) are neither targets nor features, and should be removed from the input data?

Variables dropped as they serve only as identifiers:
- EIN (Employer identificaiton) 
- NAME

Variables dropped as they were only applicable to a small percentage of data:
- SPECIAL_CONSIDERATIONS

## Compiling, Training, and Evaluating the Model: How many neurons, layers, and activation functions did you select for your neural network model, and why? 

In the initial model I used 2 hidden layers with 80 and 30 neurons respectively and a ReLu activation function. The output layer is a binary classification and then, a Sigmoid function was used.

In 100 epochs, the model accuracy was evaluated in 72.40 % 

![](/Images/00_1.png)

![](/Images/00_2.png)

## Were you able to achieve the target model performance?

No.

## What steps did you take to try and increase model performance?

In the first attempt, I dropped two noisy variables, "SPECIAL_CASE_Y and SPECIAL_CASE_N, to try to increase the accuracy.

Using the same configuration as the initial model, it didn't improved the accuracy, which was 72.59%.

![](/Images/01_1.png)

![](/Images/01_2.png)

In the second attempt, by using the same dataframe with the variables above dropped, I added a hidden layer and added more neurons to all the hidden layers.

These changes didn't help the accuracy, which was 72.60%.

![](/Images/02_1.png)

![](/Images/02_2.png)


In the third and last attemp, I used again the dataframe with noisy variables dropped, added more neurons to the hidden layers and increased the number of epochs to 500. The accuracy was pratically the same, 72.53%.

![](/Images/03_1.png)

![](/Images/03_2.png)



# Summary:
This neural neural network model did not reach the target of 75% accuracy, even with the attempts to optimize it.

It seems like the neural network model is overfitted to this data, as even with different configurations the results were the same.

One alternative to the neural network cam be the Random Forest Classifier, as it is an accurate model due to their number of estimators and tree depth. They may also have faster performance than neural networks and avoid the data overfitting situation.