# Phishing URL detection Using Classification models
## **Introduction**
Machine learning algorithms can be trained to detect phishing URLs by analyzing their characteristics and comparing them to known phishing websites. These algorithms can identify patterns in URL structures, domain names, and other features that are indicative of malicious websites. By learning from a dataset of phishing and legitimate URLs, these models can accurately classify new, unseen URLs as either phishing or legitimate.  

## **Data Collection and Preprocessing:**
  - A dataset is created containing both phishing and legitimate URLs. 
  - Features are extracted from each URL, such as its length, the presence of specific keywords, and the domain name. 
  - Data preprocessing techniques may be applied to clean and prepare the data for machine learning models.
  
In this work I used the dataset "PhiUSIIL Phishing URL" from UCI Machine Learning Repository.PhiUSIIL Phishing URL Dataset is a substantial dataset comprising 134,850 legitimate and 100,945 phishing URLs. Most of the URLs we analyzed, while constructing the dataset, are the latest URLs. Features are extracted from the source code of the webpage and URL. Features such as CharContinuationRate, URLTitleMatchScore, URLCharProb, and TLDLegitimateProb are derived from existing features.To download dataset go to link : https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset.
As for preprocessing, there are no missing values or duplicate values in this dataset.We need to handle the categoral features and the outliers in the dataset.

## **Machine Learning Model Training:**
Before stating the ML model training, the data is split into 80-20 i.e., 8000 training samples & 2000 testing samples. From the dataset, it is clear that this is a supervised machine learning task. There are two major types of supervised machine learning problems, called classification and regression.

This data set comes under classification problem.Various machine learning algorithms can be used, including:
    - Logistic Regression: A linear model that predicts the probability of a URL being phishing.
    - K-Nearest Neighbour:Algorithm determines the most frequent class label among the 'k' nearest neighbors and assigns it to the new data point. 
    - Decision Trees: Models that use a tree-like structure to classify URLs. 
    - Random Forests: An ensemble of decision trees that improve accuracy and robustness. 
    - Support Vector Machines (SVM): A model that finds the optimal hyperplane to separate phishing and legitimate URLs.  
The models are trained on the prepared dataset to learn the patterns that differentiate phishing URLs from legitimate ones.
 
## **Model Evaluation and Fine-tuning:**
  - The trained models are evaluated using metrics like accuracy, precision, recall, and F1-score.
  - The models can be further fine-tuned to improve their performance by adjusting hyperparameters or using different feature selection techniques. 

## **End Results**
From the obtained results of the above models, Random Forest Classifier has highest model performance of 99%. So the model is saved to the file 'Phishing_.pkl'.
