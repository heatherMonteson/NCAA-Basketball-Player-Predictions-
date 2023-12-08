## Predicting NBA draft picks of NCAA players through data mining 

**1. Data Collection:**
   - https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021
   - Includes player stats from 2009-2021

**2. Data Preprocessing:**
   1) Import and remove corrupt/inconsistant/unnecessary data
   
   2) Drop cols. with >60% missing data (nan values) 
   
   3) Remove highly corrilated features with corrilation above 70%
   
   4) Change target variable 'pick' to 1 if value is 1-60, else to 0
   
   5) Merge each individual player into 1 row/player
   
   6) Remove all players who still have >15% missing data 
   
   7) split into training and testing data
   
   8) Use KNN to fill in any remaining missing data/Nan values
   
   9) Feature selection with random forest classifier 

**3. Split training Data:**
   - Divide the dataset into training, validation.
   - Used 2 methods for finding the best methods for training on unbalanced data: k-fold and by simply balancing the data 

**4. Select a Prediction Target:**
   - Looking to predict if player was drafted or not, this is represented in our data set as 'pick'
     
**5. Model Selection:**
   - Used an ensemble with logistic regression, random forest, and support vector machine models 

**6. Model Training:**
   - k-fold and balanced data training, iterated with different feature selection 

## Still need to do 

**7. Model Evaluation:**
   - Use the validation set to tune hyperparameters and evaluate the model's performance. Common metrics for regression tasks include Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).

**9. Model Interpretation:**
    - Interpret the model's output to understand the factors that contribute to a player's performance prediction.

**10. Model Testing:**
    - Evaluate your model on the test set to ensure it generalizes well to unseen data.
