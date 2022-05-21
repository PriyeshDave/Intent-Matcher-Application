# Intent-Matcher-Application
![image](https://user-images.githubusercontent.com/81012989/169656678-d27b878a-3133-473f-9919-f242bd8bb8e1.png)

## Introduction
Intent Matcher Application is a NLP based application which determines if to questions have same intent or not.

## 🧭 Problem Statement: 
This is a binary classification problem where we are predicting if the given two questions have same intent or not:
* Same => Both the questions have same intent.
* Different: If the intent is not same.
<img width="572" alt="image" src="https://user-images.githubusercontent.com/81012989/169664213-423764e0-c52f-402e-919f-7abde7d7b541.png">

## 🧾 Description: 
The dataset is based on actual data from Quora and will give anyone the opportunity to train and test models of semantic equivalence. There are over 400,000 lines of potential question duplicate pairs. Each line contains IDs for each question in the pair, the full text for each question, and a binary value that indicates whether the line truly contains a duplicate pair.
* Datasets: https://drive.google.com/file/d/1VFNjjD88XCxQK0KX8pSSw8zudjuy8TKe/view?usp=sharing

### :bar_chart: Exploratory Data Analysis:
* Exploratory Data Analysis is the first step of understanding your data and acquiring domain knowledge. 

### :hourglass: Data Preprocessing:
#### 1.) Data Cleaning:
* The given data was cleaned & preprocessed by first removing the unwanted special characters and numbers from text.
* Next I removed the stop words from the sentences.
* The preprocessed data is saved in **Cleaned-Data.csv** file.

#### 2.) Vectorization:
* I used **Avg Word2Vec** for vectorizing my text data.
* Each of the question is represented by a vector of length 500.
* The vectorized form of question1 and question2 is stored in **Q1_word2vec.csv** and **Q2_word2vec.csv** files respectively.

### ⚙ Model Training:
* The model is trained using **Sequential Model** with a 3 **BidirectionalLSTM layers** with 512, 256 and 128 neurons respectively.

<img width="630" alt="image" src="https://user-images.githubusercontent.com/81012989/169664655-b9f64d52-5d4c-4b88-aee5-42e59b6423af.png">
<img width="895" alt="image" src="https://user-images.githubusercontent.com/81012989/169664725-333863fe-d3d4-4946-bc0e-dd32b455f717.png">


* My trained model gives an accuracy of **80%** on train data while of **76%** on test data.
* As per the problem statement I used **F1 Score** as the evaluation metric for my model.
* Model: https://drive.google.com/file/d/1MvBdkfjrAC_A1I59qO_Vr0-QpZvOIqiN/view?usp=sharing

