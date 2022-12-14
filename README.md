# Neural_Network_Charity_Analysis
To uncover success trends on applicants that are funded by Alphabet Soup using different machine learning strategies.

## Overview:
The purpose of this project was to review a large set of data for a charity and use a binary classification model to see if the features in the provided dataset to help Beks predict whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.  For the machine learning part, tensorflow will be utilized along with scikitlearn.

## Results
- What variable(s) are considered the target(s) for your model?

  - The target variable that forms the basis of our model is the IS_SUCCESSFUL category pulled from the charity.csv.  If the value = 1, the request was successful, and 0 if it was not.

- What variable(s) are considered to be the features for your model?
  - Initially the variables considered features for the model are application type, affilation, classification, use case, organization, income amount, special considerations, and asking amount, but for the optimization part I incoperated name and achieved results above 75%.  Categorical variables here were through OneHotEncoder which were transformed into useable data.
  
- What variable(s) are neither targets nor features, and should be removed from the input data? 
  - Initially, variables EIN and Name were removed from the data after importing the csv because they are neither features or targets for the model. Name was added in the optimization exercize, which drastically improved model performance.
  
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - For the original model I chose to go with a sigmoid activation with 100 units as the first hidden layer, a relu activation with 20 units for the 2nd hidden layer, and for the output a linear activation with 1 unit.  I chose 100 as the starting hidden layer because I wanted to rough have twice as many neurons as my input shape.  I chose sigmoid and relu because these are the activation functions typically used in binary classification models.
  
- Were you able to achieve the target model performance?
  - I was able to reach the target performance level after optimization after tweaking the model and making adjustments.
    - Initial run had an accuracy of 72.31%
    - The first optimization run had an accuracy of 77.81%.
    - The 2nd optimization run had an accuracy of 77.61%.
    - The final optimization attempt had an accuracy of 77.66%.

## Summary

In conclusion, I was unable to get results above 75% after making several tweaks to the model. I suggest experimenting with the entire dataset to see if there is improvements. It was helpful to look at online resources for which activation functions are the best for binary models and how many neurons to use for each layer.
