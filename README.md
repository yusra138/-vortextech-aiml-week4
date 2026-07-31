# IMDB Movie Review Sentiment Analysis

## Project Overview

This project focuses on building a machine learning model that can classify movie reviews into two categories: **Positive** or **Negative**.

The goal of this project is to understand how Natural Language Processing (NLP) techniques can be used to process human-written text and convert it into meaningful numerical features that machine learning models can learn from.

For this task, the IMDB Movie Reviews dataset was used, which contains 50,000 movie reviews labeled with their sentiment. The project follows a complete NLP pipeline, starting from text preprocessing to model training and evaluation.

---

## Dataset

**Dataset Used:** IMDB Dataset of 50K Movie Reviews

**Source:** Kaggle  
https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

The dataset contains:

- 50,000 movie reviews
- Two sentiment classes:
  - Positive
  - Negative

The dataset is balanced, containing an equal number of positive and negative reviews, which helps in building a fair classification model.

## Technologies and Libraries Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Regular Expression (re)
- TF-IDF Vectorizer
- Logistic Regression
- Matplotlib
- Seaborn



## Project Workflow

### 1. Data Loading and Exploration

The dataset was loaded using Pandas and inspected to understand its structure.

Initial exploration included:

- Checking dataset size
- Viewing sample reviews
- Identifying text and label columns
- Checking sentiment distribution


### 2. Text Preprocessing

Raw text data usually contains unnecessary information such as punctuation, special characters, and inconsistent capitalization.

The reviews were cleaned by:

- Converting text into lowercase
- Removing punctuation and special characters
- Removing extra spaces

This step helps reduce noise and makes the text easier for the machine learning model to process.


### 3. Feature Extraction Using TF-IDF

Machine learning models cannot directly understand text, so the cleaned reviews were converted into numerical representations.

TF-IDF (Term Frequency-Inverse Document Frequency) was used to identify important words from the reviews and represent them as numerical features.

The model was trained using the 5,000 most important words from the dataset.


### 4. Model Training

The dataset was divided into:

- 80% Training data
- 20% Testing data

A Logistic Regression classifier was trained on the TF-IDF features to learn patterns between words and sentiment labels.


## Model Evaluation

The trained model was evaluated using:

### Accuracy Score

Measures the overall percentage of correctly classified reviews.

### F1 Score

Provides a balance between precision and recall and gives a better understanding of model performance.

### Confusion Matrix

Used to analyze correct and incorrect predictions for positive and negative reviews.


## Testing Custom Reviews

After training, the model was tested on manually created movie reviews to check whether it could predict sentiment on new unseen text.

Example:

**Input:**
> "This was the best movie I have ever watched"

**Prediction:**
> Positive


## Results

The Logistic Regression model performed well on the IMDB dataset, showing that traditional machine learning techniques combined with TF-IDF can effectively handle sentiment classification tasks.

The results demonstrate that important word patterns in movie reviews can provide enough information for accurate sentiment prediction.


## Limitations

Although the model performs well, it has some limitations:

- It does not understand the deeper meaning or context behind sentences.
- It may struggle with sarcasm or sentences containing mixed emotions.
- TF-IDF focuses mainly on word importance and does not capture relationships between words like advanced deep learning models.


## Future Improvements

Possible improvements for this project include:

- Using advanced NLP models such as LSTM, BERT, or other transformer-based models.
- Applying word embeddings like Word2Vec or GloVe.
- Improving preprocessing using techniques such as stemming or lemmatization.
- Comparing multiple machine learning algorithms.


## Conclusion

This project provided practical experience with the complete NLP workflow, including text preprocessing, feature extraction, model training, and evaluation.

The results show how machine learning can be applied to analyze large amounts of text data and automatically identify sentiment from user reviews.
