# Sentiment Analysis Project

This project is a sentiment analysis project developed as part of the course "NLP - Natural Language Processing with Python" on Udemy, taught by Jose Portilla. The goal of the project is to classify movie reviews as either positive or negative based on their text content.

## Project Overview

The project uses a dataset of movie reviews, stored in the file `moviereviews.tsv`. The dataset contains two columns: `label` (indicating the sentiment of the review, either "pos" for positive or "neg" for negative) and `review` (containing the text of the review).

The project follows the following steps:

1. Data preprocessing:
   - Dropping null records: Any rows with missing values are removed from the dataset.
   - Dropping empty strings: Rows with empty string reviews are removed from the dataset.

2. Sentiment analysis using VADER:
   - The VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool is utilized.
   - The `SentimentIntensityAnalyzer` from the NLTK library is used to assign sentiment scores to each review.
   - A compound score is computed, representing the overall sentiment of the review.
   - Based on the compound score, a predicted label ("pos" or "neg") is assigned to each review.

3. Evaluation and results:
   - The accuracy of the sentiment analysis model is computed by comparing the predicted labels to the actual labels in the dataset.
   - Classification metrics (precision, recall, f1-score) are calculated and displayed.
   - A confusion matrix is generated to visualize the performance of the model.

## Results and Limitations

The sentiment analysis model using VADER achieves an accuracy of approximately 63.67%. However, it is important to note that VADER may struggle with sarcasm and the detection of dichotomy in reviews, which can lead to lower precision and recall scores.

To improve the classification of positive and negative sentiment, the project suggests using the TF-IDF (Term Frequency-Inverse Document Frequency) technique. TF-IDF can help create better classification models, providing more accurate results for sentiment analysis tasks.

## Repository Information

The code for this sentiment analysis project can be found in the `sentiment_analysis_project.ipynb` file. It is a Jupyter Notebook file containing the code and explanations for each step of the project.
