# Combating-Twitter-Hate-Speech-Using-ML-and-NLP
Using NLP and ML, make a model to identify hate speech (racist or sexist tweets) in Twitter. 
Problem Statement: Twitter is the biggest platform where anybody and everybody can have their views heard. Some of these voices spread hate and negativity. Twitter is wary of its platform being used as a medium  to spread hate.   You are a data scientist at Twitter, and you will help Twitter in identifying the tweets with hate speech and removing them from the platform. 
You will use NLP techniques, perform specific cleanup for tweets data, and make a robust model.  Domain: Social Media  Analysis to be done: Clean up tweets and build a classification model by using NLP techniques, cleanup specific for tweets data, regularization and hyperparameter tuning using stratified k-fold and cross validation to get the best model.  Content:   id: identifier number of the tweet  Label: 0 (non-hate) /1 (hate)  Tweet: the text in the tweet  
Tasks:       Load the tweets file using read_csv function from Pandas package.      
Get the tweets into a list for easy text cleanup and manipulation.      
To cleanup: Normalize the casing. Using regular expressions, remove user handles. These begin with '@’.         
Using regular expressions, remove URLs. Using TweetTokenizer from NLTK, tokenize the tweets into individual terms.          
Remove stop words. Remove redundant terms like ‘amp’, ‘rt’, etc.         
Remove ‘#’ symbols from the tweet while retaining the term.      
Extra cleanup by removing terms with a length of 1.      
Check out the top terms in the tweets:  
First, get all the tokenized terms into one large list. Use the counter and find the 10 most common terms.     

Data formatting for predictive modeling:  Join the tokens back to form strings. This will be required for the vectorizers. 
Assign x and y.  Perform train_test_split using sklearn. We’ll use TF-IDF values for the terms as a feature to get into a vector space model.         
Import TF-IDF  vectorizer from sklearn.          Instantiate with a maximum of 5000 terms in your vocabulary.          
Fit and apply on the train set. Apply on the test set.     
Model building: Ordinary Logistic Regression 
Instantiate Logistic Regression from sklearn with default parameters.         
Fit into  the train data.
Make predictions for the train and the test set. 
Model evaluation: Accuracy, recall, and f_1 score. 
Report the accuracy on the train set.  

Report the recall on the train set: decent, high, or low. Get the f1 score on the train set. Looks like you need to adjust the class imbalance, as the model seems to focus on the 0s.          Adjust the appropriate class in the LogisticRegression model. 
Train again with the adjustment and evaluate.          Train the model on the train set. 
Evaluate the predictions on the train set: accuracy, recall, and f_1 score. Regularization and Hyperparameter tuning:          
Import GridSearch and StratifiedKFold because of class imbalance.          Provide the parameter grid to choose for ‘C’ and ‘penalty’ parameters.Use a balanced class weight while instantiating the logistic regression.
Find the parameters with the best recall in cross validation. Choose ‘recall’ as the metric for scoring.          
Choose stratified 4 fold cross validation scheme. Fit into  the train set.      
What are the best parameters?      Predict and evaluate using the best estimator.         
Use the best estimator from the grid search to make predictions on the test set.          
What is the recall on the test set for the toxic comments?  What is the f_1 score?
