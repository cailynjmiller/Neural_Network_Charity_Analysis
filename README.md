# Neural_Network_Charity_Analysis
## Overview of the Analysis
The purpose of this project is to create a deep neural network to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
## Results
### Data preprocessing
- The target variable for this analysis is "IS_SUCCESSFUL".
- The input variables are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT               .
- The variables EIN and NAME were removed as they were not relevant to the analysis.
### Compiling, Training, and Evaluating the Model
- I used 2 hidden layers with 80 neurons for the first hidden layer and 30 neurons for the second. I also used the relu activation function for the hidden layers and the sigmond activation function was used for the output layer.
- No, the model was unsuccessful in reaching the 75% model performance. It only achieved a .7257(72.57%) accuracy score.
![orginal scores](https://github.com/cailynjmiller/Neural_Network_Charity_Analysis/blob/main/photos/original%20scores.png)
- Steps taken to increase model performance
  - Making the "other" bucked have a smaller threshold for APPLICATION_TYPE. I changed it for values that had counts over 100 instead of 500.
  - Making the "other" bucked have a smaller threshold for CLASSIFICATION. I changed it for values that had counts over 100 instead of 1800.
  - Creating a third hidden layer with 80 neurons.
  - I was unable to achieve the target performace after making these changes. In fact, the accuracy score went down slightly to .7250(72.5%).
 ![optim scores](https://github.com/cailynjmiller/Neural_Network_Charity_Analysis/blob/main/photos/optimization%20scores.png)
## Summary
For both models, they predicted "IS_SUCCESSFUL" correct around 72.5% of the time with a loss score of .57. I recommend using the Tahn function to take into account negative values that the dataset could contain that would be made 0 with the Relu activation function.
