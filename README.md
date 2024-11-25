# Fake News Detection

This project implements a **Fake News Detection System** using **Natural Language Processing (NLP)** techniques. The system classifies news articles as **real** or **fake** based on the content using machine learning models like **Logistic Regression** and **TF-IDF** for text vectorization.

## Project Overview

With the rise of misinformation and fake news, detecting the authenticity of news articles has become crucial. This project uses NLP techniques to automatically detect whether a given news article is real or fake. The classification model is trained on a labeled dataset and utilizes **TF-IDF** vectorization for transforming text data into numerical features.

## Features

- **Data Preprocessing**: 
  - Text data is cleaned and preprocessed to ensure that the model can effectively analyze and learn from it. This step involves several processes:
    - **Removing Noise**: Irrelevant words such as stopwords (e.g., "the", "and", "is") and special characters (e.g., punctuation marks) are removed.
    - **Tokenization**: The text is split into smaller units like words or phrases (tokens). This allows the model to analyze each word individually.
    - **Lowercasing**: All text is converted to lowercase to avoid treating the same word (e.g., "Fake" and "fake") as different entities.
    - **Lemmatization/Stemming**: Words are reduced to their base form. For instance, "running" becomes "run", which helps the model generalize better.
  
- **Text Vectorization (TF-IDF)**:
  - **TF-IDF** (Term Frequency-Inverse Document Frequency) is used to convert the text data into a numerical format, allowing machine learning models to process the information. It works in two ways:
    - **Term Frequency (TF)**: Measures how frequently a term (word) appears in a document. A higher frequency means that word is more important to the document.
    - **Inverse Document Frequency (IDF)**: Measures how rare or unique a term is across the entire dataset. Words that appear in fewer documents have a higher IDF, and thus more weight.
  - The combination of these two (TF × IDF) gives each word a score that indicates its importance in a document and across the dataset. Words that are common in fake news articles will have a higher score, making them more significant in the classification process.

- **Modeling (Logistic Regression)**:
  - The model used for classification is **Logistic Regression**, a popular machine learning algorithm for binary classification problems like this one (real vs. fake news).
  - Logistic Regression uses the weighted features from the TF-IDF vectorization to learn the relationship between the words in the news articles and their corresponding labels (fake or real).
  - Once trained, the model can predict the probability of a new article being fake or real based on the patterns it has learned. Logistic Regression is a simple yet effective algorithm for this task and works well with text classification problems.

- **Accuracy**:
  - The accuracy of the model is calculated as the percentage of correct predictions made by the model compared to the total number of predictions. It is a key performance metric for evaluating the effectiveness of the model.
  - The model is trained on the **Fake News Dataset**, and the accuracy achieved on the test data indicates how well it can distinguish between fake and real news articles.
  - The accuracy metric provides a quick overview of how well the model is performing. For example, if the model predicts the correct label (fake or real) 85 times out of 100, the accuracy is **85%**. Higher accuracy means better performance.


