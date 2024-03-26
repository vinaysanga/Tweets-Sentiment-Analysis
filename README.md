# Tweets Sentiment Analysis
Sentiment analysis, a vital aspect of natural language processing, assesses emotions, opinions, and attitudes within textual data. This project utilizes the Sentiment140 dataset, aiming to build and compare two machine learning models to analyze and predict sentiments expressed in tweets accurately.

<a target="_blank" href="https://colab.research.google.com/github/vinaysanga/Tweets-Sentiment-Analysis/blob/master/Experiment.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Data Preprocessing
The initial step involved loading the data into a DataFrame. The sentiment labels were encoded as 0 for negative and 4 for positive sentiments. The preprocessing phase included:

- **Text Normalization**: Converting all tweets to lowercase to maintain consistency.
- **Noise Removal**: Eliminating URLs, usernames, and special characters using regular expressions.
- **Tokenization**: Breaking down cleaned text into individual words or tokens.
- **Stopwords Removal**: Removing common English stopwords to focus on more meaningful words.
- **Lemmatization**: Converting words to their base form to simplify the analysis.

This processed text was then ready for vectorization, transforming it into a numerical format suitable for machine learning models.

## Modelling

### 3.1 Logistic Regression
Chosen for its simplicity and efficiency in binary classification, Logistic Regression was trained using TF-IDF vectorized input from the preprocessed tweets. Cross-validation with 5 folds was employed to ensure model reliability and applicability.

### 3.2 Linear Support Vector Classifier (Linear SVC)
The Linear SVC model, known for its high-dimensional space performance, was also trained on TF-IDF vectorized tweets, using cross-validation to evaluate its effectiveness.

## Model Evaluation
The models were evaluated on accuracy, precision, recall, and F1-score for both sentiment classes. The mean values of these metrics for both models were remarkably similar, indicating comparable performance in the sentiment analysis task.

- **Accuracy**: Both models achieved a mean accuracy of 74%.
- **F1-Score**: A balanced metric between precision and recall, stood at 0.76 for both models.
- **Precision and Recall**: Both models showed a precision and recall of 0.74 and 0.76, respectively.

ROC curves were plotted for both models, revealing:
- AUC for Logistic Regression at 0.84 and for Linear SVC at 0.83, demonstrating strong predictive capabilities

## Conclusion
Logistic Regression and Linear SVC exhibited similar performance metrics, the experience highlighted that no single model universally outperforms others, emphasizing the need for a tailored approach based on the specific task and data characteristics.

**For the entire info, please check [Project_Report](Project_Report.pdf)**
