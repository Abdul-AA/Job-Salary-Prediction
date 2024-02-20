# Job Salary Prediction Project

## Overview
This project aims to predict job salaries from job descriptions by classifying them into high and low salary categories. The dataset used for this project was sourced from [Kaggle's Job Salary Prediction competition](http://www.kaggle.com/c/job-salary-prediction).

For efficiency, a sample of 2,500 observations was extracted from the dataset. The original target variable was continuous, representing salaries. It was transformed into a categorical variable, with salaries in the >= 75th percentile categorized as high.

## Model Building Process

### Data Preprocessing
- The target variable was converted from continuous to categorical, with the cutoff for high salaries set at the 75th percentile.
- A subset of 2,500 observations was sampled to enhance the efficiency of the analysis.

### Model Selection
- Naive Bayes was chosen as the primary model for its simplicity and effectiveness in text classification tasks.

### Feature Engineering and Selection
- Both Count Vectorizer and TF-IDF techniques were evaluated to determine their effectiveness in processing text data.
- Count Vectorizer was found to be more effective, leading to higher accuracy in the predictive model.
- Variations of Count Vectorizer, including changes in n-grams, max features, and document frequency thresholds, were tested but did not yield significant improvements.
- Lemmatization was also experimented with; however, adjustments to hyperparameters did not result in better outcomes.

## Analysis of Words Indicative of Salary Levels

### High Salary Indicators
- A logistic regression model, trained on text data processed by Count Vectorizer, identified words with the highest positive coefficients as indicators of high salaries. These words include: director, senior, leadership, dentist, consumer, player, reputation, lead, successfully, and image.
  
### Low Salary Indicators
- Words with the lowest coefficients, suggesting a negative correlation with salary, were identified as indicators of low salaries. These words include: applicants, standard, basic, database, hours, depending, timely, selling, building, and stock.

## Conclusion
This project demonstrates the application of Naive Bayes and logistic regression models to classify job descriptions into high and low salary categories based on the text of the job descriptions. Through careful feature engineering and model selection, it was possible to identify key words associated with each salary category, providing insights into the factors that may influence salary levels in job postings.

