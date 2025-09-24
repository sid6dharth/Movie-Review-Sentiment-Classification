# IMDb Movie Review Sentiment Classification 

## Project Overview
This project classifies IMDb movie reviews as positive or negative using machine learning models.


## Approach
1. First, the data was preprocessed by making all the words present in the reviews into lowercase, removing any HTML tags, extra spaces and punctuations. Then, the labels - positive and negative were converted into 1 and 0 respectively.

2. The dataset was then broken into a 80 : 20 split training set vs test set and also stratified to ensure equal instances of sentiments were present in both.

3. The text was then converted into vectors by using Tfidf vectorizers which assigns high weightage to words which are frequent in a particular review but not common throughtout all the reviews, examples: great, good, boring, etc.

3. The best hyperparameter values for TfIdf (max features, ngram range) were found using GridSearchCV and then applied.

4. 3 Different models were then trained:
   - Logistic Regression
   - Support Vector Machine (SVM)
   - Random Forest

4. Different metrics like Accuracy (number of correct predictions), Precision (quality of positive predictions), Recall (coverage of positives identified), and F1-score (balance of precision & recall) were used to evaluate and compare the peformances of the 3 different models against each other.

5. The results were then visualised with confusion matrices for each model as well as plots showing the comparison between the different models based on different metrics.

##  Results

| Model               | Accuracy | Precision | Recall | F1-score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression | 0.8996   | 0.8937    | 0.9070 | 0.9003   |
| SVM                 | 0.8931   | 0.8891    | 0.8982 | 0.8936   |
| Random Forest       | 0.8403   | 0.8111    | 0.8872 | 0.8474   |

Logistic Regression performed the best with ~90% accuracy and ~ 90 F1-score followed by SVM achieving almost similarly with an accuracy of ~89%. The Random Forest model performed the worst out of all 3 but still achieved a decent 84% accuracy, ~89% recall and ~ 85% F1 - score but had a low precision 81%.


