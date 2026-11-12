# SMS Spam Detection using Multinomial Naive Bayes

A machine learning-based SMS classification application that identifies whether a text message is **Spam or Not Spam (Ham)** using Natural Language Processing (NLP) and the Multinomial Naive Bayes algorithm.

## Overview

This project implements an SMS Spam Detection system using supervised machine learning techniques. It applies NLP-based text preprocessing to clean and normalize incoming SMS messages before converting them into numerical representations for classification.

A trained **Multinomial Naive Bayes (MNB)** model predicts whether a given message is spam or legitimate (ham).

The application is deployed through a **Streamlit web interface**, allowing users to enter SMS messages and receive real-time classification results.

## Key Features

- **SMS Classification:** Identifies incoming text messages as Spam or Ham.
- **Natural Language Processing:** Applies text preprocessing techniques to prepare messages for classification.
- **Text Cleaning:** Performs lowercase conversion, punctuation handling, and tokenization.
- **Stopword Removal:** Removes common English stopwords to reduce irrelevant textual information.
- **Stemming:** Uses Porter Stemming to normalize words to their root forms.
- **Feature Extraction:** Uses a previously fitted text vectorizer to transform messages into numerical feature representations.
- **Machine Learning Classification:** Uses a trained Multinomial Naive Bayes classifier for spam detection.
- **Interactive Web Interface:** Provides a simple Streamlit application for real-time predictions.

## Machine Learning Workflow

The system follows a sequential NLP and machine learning pipeline:

1. **SMS Input:** Accepts a text message from the user.
2. **Text Preprocessing:** Converts text to lowercase and tokenizes the message.
3. **Text Cleaning:** Removes punctuation and irrelevant characters.
4. **Stopword Removal:** Filters out commonly occurring English words.
5. **Stemming:** Applies Porter Stemming to normalize words.
6. **Feature Extraction:** Transforms the processed text into numerical features using the trained vectorizer.
7. **Classification:** Passes the extracted features to the Multinomial Naive Bayes model.
8. **Prediction Output:** Displays the classification result as Spam or Ham.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Machine Learning | Scikit-learn |
| Classification Algorithm | Multinomial Naive Bayes |
| Domain | Natural Language Processing (NLP) |
| Text Preprocessing | NLTK |
| Feature Extraction | Text Vectorization |
| Data Processing | NumPy, Pandas |
| Model Serialization | Pickle |
| Web Application | Streamlit |

## Project Structure

```text
mnb-spam-model-2/
│
├── Streamlit Web App
│   └── Streamlit application deployment
│
├── m.pkl
│   └── Trained Multinomial Naive Bayes model
│
├── v.pkl
│   └── Fitted text vectorizer
│
├── prac.py
│   └── SMS preprocessing and classification application
│
├── requirements.txt
│   └── Project dependencies
│
└── README.md
```


The application will open in your default browser.

## Model & Classification

The project uses the **Multinomial Naive Bayes algorithm**, a probabilistic machine learning algorithm commonly used for text classification tasks.

The trained model and fitted vectorizer are stored as serialized pickle files:

- `m.pkl`: Contains the trained classification model.
- `v.pkl`: Contains the fitted text vectorizer used for feature extraction.

Both artifacts are loaded during application execution to perform predictions without retraining the model.

## Example Predictions

| Input SMS | Expected Classification |
|---|---|
| Congratulations! You have won a free prize. Claim now! | Spam |
| Hey, are we meeting tomorrow? | Ham |
| URGENT! You have been selected for a cash reward. | Spam |
| I'll call you when I get home. | Ham |

*Examples are illustrative and do not represent measured model performance.*

## Live Demo

[**SMS Spam Detection – Streamlit App**](https://av5gxny3bheqpr4grne5ic.streamlit.app/)

