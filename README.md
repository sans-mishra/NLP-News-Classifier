# NLP-News-Classifier
# Introduction
The main idea behind the News Classification project is to create a robust machine learning model that can classify news articles into their respective categories. It comprises of a dataset of news article statistics, focusing on predicting the correct category of each article based on its content using Natural Language Processing (NLP) techniques and a Support Vector Machine (SVM) classifier.

# Features
* Text preprocessing techniques like stopword removal, tokenization, stemming, and TF-IDF vectorization.
* Support Vector Machine (SVM) classifier implementation with hyperparameter tuning.
* Use of RandomizedSearchCV for optimizing hyperparameters.
* Evaluation metrics like accuracy, F1-score, and confusion matrix for performance analysis.
* Configurable parameters for model training.
# Dataset
The dataset used in this project contains news articles with the following columns:

 * ID: Unique identifier for each article.
 * News_Title: The title of the news article.
 * News_Headline: The headline or summary of the article.
 * Category: The target label/category for classification.
 The categories are:

    * Arts (0)
    * Business (1)
    * Humor (2)
    * Politics (3)
    * Sports (4)
    * Tech (5)
    * Data Preprocessing
To prepare the dataset for training, the following preprocessing steps are applied:

* Text Cleaning: Removing special characters, punctuation, and non-alphabetic characters.
* Tokenization: Splitting the text into individual words.
* Stopword Removal: Removing common words that do not add much value (e.g., "the", "is").
* Stemming: Reducing words to their base form (e.g., "running" to "run").
* TF-IDF Vectorization: Converting the processed text into numerical features using Term Frequency-Inverse Document Frequency (TF-IDF).
# Model Overview
Support Vector Machine (SVM)
   * The SVM is a supervised learning model used for classification tasks. It aims to find the optimal hyperplane that maximizes the margin between different categories in the dataset. For this project:
   * A linear SVM was used for text classification.
   * The TF-IDF vectors served as input features for the SVM.

Hyperparameter Tuning
   * Hyperparameters for the SVM were optimized using RandomizedSearchCV, which performs random sampling of hyperparameters over a specified parameter grid.
   * The key hyperparameters tuned in this project are:
     * C (Regularization parameter)
     * Kernel (Type of kernel function, e.g., 'linear', 'rbf')
     * Gamma (Kernel coefficient)
     * Class Weight (Balancing the class weights)
