# Mental Health in Tech Treatment Analysis

## Background

### Mental health disorders consist of a wide range of mental conditions and issues that can negatively impact people’s thoughts, emotions, behaviors and even physical health. When not treated effectively, ongoing symptoms can lead to decline in their sense of well-being and ability to function in daily lives, leading to economic burden as they lose productivity in the workplace.  

### My project is built on OSMI’s survey results generated in 2019-2021, with the goal of trying to explore how these aspects about the respondents’ medical history and availability of care options from their workplace may motivate them to seek treatment for their mental health conditions. The results of this project will provide valuable insights to employers on how they can better support employees that may be struggling with such conditions, motivating them to seek treatment and improve daily function.

## Research Question

### What factors predict whether employees will seek mental health services?

## Dataset

### Open Sourcing Mental Health (“OSMI”) is a non-profit organization dedicated to raising awareness, educating, and providing resources to support mental wellness in the tech and open source communities. OSMI started conducting “Mental Health in Tech” surveys in 2014 with questions that try to understand a respondent’s personal history of mental health conditions and the types of support and resources they receive from their employers. 

### This dataset can be accessed on Kaggle and downloaded as csv files that will be imported into Google Colab notebook: 
- https://www.kaggle.com/datasets/osmihelp/osmh-2021-mental-health-in-tech-survey-results
- https://www.kaggle.com/datasets/osmihelp/osmi-2020-mental-health-in-tech-survey-results
- ttps://www.kaggle.com/datasets/osmihelp/osmi-mental-health-in-tech-survey-2019

## Feature Engineering

### I will derive my model inputs/features from survey questions that encompass aspects about the respondents and their workplace such as:
- Year the survey was taken as the pandemic may or may not impact a person’s willingness to seek treatment
- demographic info such as age and gender
- Personal history with mental health conditions
- Availability and awareness of mental health benefits offered through employer-based health insurance coverage
- Level of comfort in discussing mental health at work

### These factors will help us assess what impacts people's intention to seek treatment.

## Testing Methodology

### I will employ the clustering methodologies under unsupervised learning, specifically K-means and PCA, to determine where the survey provides insights to help distinguish employees between two clusters: 
1. **Those that seek mental health treatment**
2. **Those that do not seek treatment.**

### Two clustering methodologies selected:
- K-mode for categorical variables, as the answers for most survey questions are coded in Yes, No, Maybe responses. 
- K-means for numerical variables after converting the categorical variables to numerical variables using one-hot encoding.

### Both methodologies yield 2 as the optimal number of clusters. 

## Clustering Insights

### There are 2 distinct clusters. One of the clusters consists mostly of employees who seek treatment for mental health issues. Based on observations made in this cluster, employers could do more of the following in order to encourage employees to seek mental health treatment:
- Offer more comprehensive health care benefits that cover mental health care.
- Increase employees' awareness and knowledge of options for mental health care available under their employer-provided health coverage, i.e., through email communication, team forums or other wellness campaigns and publications.
- Encourage employees to pay more attention to their emotions, stress level and overall sense of well-being.
- Improve the ease to request medical leave to address mental health issues, while incorporating some eligibility criteria that motivate employees to start discussions with medical professionals and setting up treatment plans.











