## Overview
Logistic Regression is a supervised learning algorithm used for binary and multi-class classification problems. Unlike linear regression, it predicts the probability of a target variable belonging to a particular class using the logistic (or sigmoid) function.

## Key Concepts
- **Binary Classification**: Predicting two possible outcomes (e.g., spam or not spam).
- **Sigmoid Function**:
  - Converts raw outputs (logits) into probabilities between 0 and 1.
  - Formula: 
	$$
    \sigma(z) = \frac{1}{1 + e^{-z}}
    \
    $$
- Where:  $z = \beta_0 + \beta_1x_1 + \beta_2x_2 + \dots + \beta_nx_n$
- **Thresholding**: A probability threshold (e.g., 0.5) is used to classify the output.

---

## Applications
- **Healthcare**: Disease diagnosis (e.g., predicting diabetes).
- **Finance**: Loan approval, fraud detection.
- **Marketing**: Customer churn prediction.
- **Natural Language Processing (NLP)**: Sentiment analysis, spam detection.

---

## Steps in Logistic Regression Workflow
1. **Data Preparation**:
   - Ensure the dataset is labeled for classification.
   - Handle missing values, normalize features, and encode categorical variables.
2. **Model Training**:
   - Fit a logistic regression model using training data.
   - Learn parameters $(\beta_0, \beta_1, \dots, \beta_n)$ using maximum likelihood estimation.
3. **Evaluation**:
   - Use metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.
4. **Prediction**:
   - Use the model to predict probabilities and classify new data.

---

## Math Behind Logistic Regression
1. **Log-Odds Transformation**:
   - Logistic regression models the **log-odds** of the dependent variable as a linear combination of features:
     $$
     \text{log}\left(\frac{p}{1-p}\right) = \beta_0 + \beta_1x_1 + \dots + \beta_nx_n
     $$
     
     where \(p\) is the probability of the positive class.
2. **Cost Function**:
   - Logistic regression minimizes the **[[Log-Loss]]** function:
     $$
     J(\beta) = - \frac{1}{m} \sum_{i=1}^{m} \left[ y_i \log(\hat{y}_i) + (1-y_i) \log(1-\hat{y}_i) \right]
     $$
     where \(y_i\) is the true label, \(\hat{y}_i\) is the predicted probability, and \(m\) is the number of data points.
3. **Optimization**:
   - Parameters are optimized using [[Gradient Descent]] or similar methods.

---

## Variants of Logistic Regression
- **[[Binary Logistic Regression]]**: Two possible outcomes (e.g., 0 or 1).
- **[[Multinomial Logistic Regression]]**: Multiple classes without an inherent order (e.g., predicting the category of an item).
- **[[Ordinal Logistic Regression]]**: Multiple classes with a natural order (e.g., rating scales).

---

## Metrics for Evaluation
- **[[Confusion Matrix]]**: Summarizes model performance.
- **[[Precision]] and [[Recall]]**:
  - Precision: 
	$$
  \frac{\text{True Positives}}{\text{True Positives + False Positives}}
   $$
  - Recall: $$
  \frac{\text{True Positives}}{\text{True Positives + False Negatives}}
  $$
- **[[F1-Score]]**: Harmonic mean of precision and recall.
	$$
	\frac{2*\text{Precision}\times\text{Recall}}{\text{Precision}+\text{Recall}}
	$$
- **[[ROC AUC]]**: Measures the trade-off between true positive rate and false positive rate.

---

## Tools and Libraries
- **[[Python]] Libraries**:
  - [[Scikit-learn]]: `LogisticRegression` class for training and evaluation.
  - [[Statsmodels]]: Provides detailed statistical output for logistic regression models.
- **[[R]]**:
  - `glm()` function for logistic regression.

---

## Common Challenges
- **[[Multicollinearity]]**: Highly correlated features can lead to unstable coefficients. Address this with [[feature selection]] or [[regularization]].
- **[[Overfitting]]**: Use regularization techniques like L1 (Lasso) or L2 (Ridge) to avoid overfitting.
- **[[Class Imbalance]]**: If one class dominates, consider resampling methods or adjusting class weights.

---

## Resources
- *Introduction to Statistical Learning* by James, Witten, Hastie, and Tibshirani.
- *An Introduction to Logistic Regression Analysis* (Research Paper).
- Online courses:
  - *Andrew Ng’s Machine Learning* on Coursera (Logistic Regression section).
  - *Python Machine Learning* by Sebastian Raschka (Chapters on Logistic Regression).

---

## Related Topics
- [[Linear Regression]]: Foundation of logistic regression.
- [[Gradient Descent]]: Optimization technique used in logistic regression.
- [[Classification Metrics]]: Tools to evaluate model performance.
- [[Scikit-learn]]: Library for implementing logistic regression.

---

## Tags
#logisticregression #machinelearning #datascience #classification

## Links to Explore
- [[Scikit-learn]]: Implementation of logistic regression.
- [[Gradient Descent]]: Optimization for parameter learning.
- [[Confusion Matrix]]: Evaluating classification models.