# Intent-Matcher-Application
![image](https://user-images.githubusercontent.com/81012989/169656678-d27b878a-3133-473f-9919-f242bd8bb8e1.png)

* Datasets : https://drive.google.com/file/d/1VFNjjD88XCxQK0KX8pSSw8zudjuy8TKe/view?usp=sharing
* Model : https://drive.google.com/file/d/1MvBdkfjrAC_A1I59qO_Vr0-QpZvOIqiN/view?usp=sharing

## Introduction
Intent Matcher Application is a NLP based application which determines if to questions have same intent or not.

## 🧭 Problem Statement: 
This is a binary classification problem where we are predicting if the given coment is toxic or not:
* Toxic => Contains text with hate speech, aggression, insults, and toxicity.
* Non Toxic 

## 🧾 Description: 
This dataset is a collection of datasets from different sources related to the automatic detection of cyber-bullying. The data is from different social media platforms like Kaggle, Twitter, Wikipedia Talk pages, and YouTube. The data contains text and are labeled as bullying or not. The data contains different types of cyber-bullying like hate speech, aggression, insults, and toxicity.

### :bar_chart: Exploratory Data Analysis:
* Exploratory Data Analysis is the first step of understanding your data and acquiring domain knowledge. 

### :hourglass: Data Preprocessing:
* The given data was cleaned & preprocessed by first removing the unwanted special characters and numbers from text.
* Next I removed the stop words from the sentences.
* Now I used **WordNetLemmatizer** for converting each of the tokens to their root words.
* Once the data is cleaned, I used **WordEmbedding** technique to convert words into vectors.

### ☁️ Word Cloud
![Toxic Word Cloud](https://user-images.githubusercontent.com/81012989/164935432-667a37e3-6035-4784-bd3b-ee5d26b1358c.png)

### ⚙ Model Training:
* The model is trained using **BidirectionalLSTM** with a vocabulary size of 16K and each word reprented by a vector of length 300.
* My trained model gives an accuracy of **91%** on train data while of **81%** on test data.
* As per the problem statement I used **F1 Score** as the evaluation metric for my model.

