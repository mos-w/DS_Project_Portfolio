# Fitbit Stress Score Prediction Analysis

## Background

### Stress is the physical or mental response to an external cause, either a short-term occurrence, or it can happen repeatedly over a long time. Anxiety is the body's reaction to stress and can occur even if there is no current threat (i.e., chronic stress). A person may be at risk for an anxiety disorder if it feels like he/she can’t manage the stress and if the symptoms of stress start to feel persistent and pervasive, interfere with daily life and cause the person to avoid doing things.  

### This project is built on biofeedback metrics collected through Fitbit devices as part of the European H2020 RAIS (Real-time Analytics for Internet of Sports) project. One of the metrics in this dataset is the Stress Score, which reflects the respondent’s level of stress. Understanding which factors can help predict this stress score will be beneficial to users and potentially guide them to make lifestyle changes to manage stress more effectively.

## Research Question

### This research will explore whether a selection of metrics tracked by Fitbit are statistically significant in their ability to explain variance in the Stress Score and to predict the Stress Score.

## Dataset

### Fitbit data tracked under the European H2020 RAIS (Real-time Analytics for Internet of Sports) project. The study involved 71 participants in the European region, and collected from mid-2021 to early-2022. Data is accessible via: https://www.kaggle.com/datasets/skywescar/lifesnaps-fitbit-dataset

## Feature Engineering

### Fitbit calculates the Stress Score from factors that cover 3 areas which will drive feature selection:
- Responsiveness: heart-rate data and electrodermal activity (EDA)
- Exertion balance: impact of physical activity on your stress level.
- Sleep patterns: effect of sleep duration and quality on your stress level.

### There are approximately 30 features spanning these 3 areas which will be incorporated to help us assess what impacts people's Stress Score.

## Testing Methodology

### OLS Regression model and Support Vector Machine Regression model are selected to evaluate whether the feature set is statistically significant in explaining the variance in the Target and predicting the Target. 

### 1) OLS Regression: 
- Adjusted R-squared value is 0.35 which means that the model only explains 37% of the variance in stress score, driven by nonlinearity in the dataset 

### 2) SVM Model: 
- RBF (radial basis function) kernel functions was use to predict the target variable.
- The SVM model score, similarly to R-squared, measures how well a statistical model predicts an outcome. In our RBF model, the feature set can explain approximately 70% of the variability in the Target which is statistically significant and better than the OLS Regression model.
- Three evaluation metrics (MAE 0.124, MSE 0.025, RMSE 0.158) are all calculated to be low, and lower values indicate better performance of the model. Specifically, stress score is measured along a range of 0-100 and the magnitude of errors calculated in our metrics are below 0.2, which is reasonably low compared to the average stress score of 76 in our dataset.


