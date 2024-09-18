# Sentiment_Analysis_Bike_Reviews

Summary:
Pre-processed dataset and implemented Logistic Regression, SVM, and Decision Tree models to predict 
sentiment of reviews in the testing dataset. 

Problem Statement:
A dataset of bike reviews with various features including text reviews and ratings. Your objective is to build a sentiment analysis model that classifies each review into one of three sentiment categories: Positive, Average, or Negative. You will preprocess the data, train a machine learning model, and evaluate its performance.

Steps:
1. Load the Dataset:
   The dataset is loaded from a CSV file (Bike_Reviews.csv). The dataset is initially inspected to understand its structure and contents.

2. Data Cleaning:
   Remove Unnecessary Columns: Columns that are not needed for the analysis (Avg_Stars and Review title) are removed.
   Handle Missing Values: Any rows with missing values are removed from the dataset.
   Remove Duplicates: Duplicate rows are identified and removed to ensure the data's uniqueness.

3. EDA:
   Visualize Ratings: The distribution of ratings is visualized using a count plot to understand the distribution of sentiments.
   Sentiment Classification: Ratings are converted into sentiment categories based on their value:
      Positive: Rating > 3
      Average: Rating = 3
      Negative: Rating < 3
   Visualize Sentiments: The distribution of sentiments is visualized to understand how many reviews fall into each sentiment category.

4. Preprocessing:
   Text reviews are cleaned by:
      Removing stop words and punctuation.
      Tokenizing the text.
      Lemmatizing the tokens (reducing words to their base form).

5. Feature extraction:
   The cleaned text is transformed into numerical features using TfidfVectorizer, which converts the text data into a matrix of TF-IDF features.

6. Model Training:
   Prepare Data for Modeling: The dataset is split into training and testing sets.
   Build Models: Two classifiers are used:
      Logistic Regression: A linear model for classification.
      Decision Tree: A model that splits data into subsets based on feature values.
   Combine Models: These models are combined using a VotingClassifier with hard voting, which aggregates the predictions of the individual models to make a final prediction.

7. Model Evaluation:
   Predict on Test Set: The combined model is used to make predictions on the test set.
   Evaluate Performance: The model's performance is evaluated using:
      Accuracy: The proportion of correctly classified reviews.
      Classification Report: Includes precision, recall, and F1-score for each sentiment category.
      Confusion Matrix: A matrix is visualized to show the true vs. predicted classifications.

Thank You!!!
