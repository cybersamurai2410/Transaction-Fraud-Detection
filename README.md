# Credit Card Fraud Detection using Autoencoders
This project aims to detect fraudulent transactions in a credit card dataset using autoencoders for anomaly detection and feature extraction, followed by classifiers for binary classification. The project demonstrates an effective approach to handling imbalanced datasets in a semi-supervised learning framework.

## Dataset
The dataset used in this project is a publicly available credit card transactions dataset, which contains transactions labeled as fraudulent (Class = 1) or non-fraudulent (Class = 0). The dataset is highly imbalanced, with fraudulent transactions being a very small fraction of the total. The feautures V1 through V28 are principle components from PCA applied to the original transaction data reducing dimensionaltiy and preserving privacy. 

## Preprocessing
*  Normalizing and scaling the features using a combination of Normalizer and MinMaxScaler.
*  Splitting the data into training, validation, and test sets.
*  Handling class imbalance by undersampling the majority class (non-fraudulent transactions).

## Autoencoder for Anomaly Detection
An autoencoder was implemented to learn the patterns of non-fraudulent transactions. The autoencoder was trained on the non-fraudulent data, and the reconstruction loss was used to identify potential anomalies. Transactions with high reconstruction loss were flagged as possible frauds.
<br><br>
![download](https://github.com/user-attachments/assets/74e6d4f0-e702-472e-8f98-e288a3ba6286)
<img width="511" alt="image" src="https://github.com/user-attachments/assets/aef82e1c-cb42-40eb-8f96-78d93325f6e3">

## Feature Extraction with Autoencoder
After training the autoencoder, the encoder part of the network was used to extract latent features from the transactions. These features were then used to train binary classifiers. 
<br><br>
![download](https://github.com/user-attachments/assets/28010349-7edb-4968-9dc8-581e3dd5e60c)

## Classification
The extracted features were used to train and evaluate different classifiers:
*  Logistic Regression
*  Support Vector Machine (SVM)
The performance of these classifiers was compared using metrics such as accuracy, precision, recall, and AUC-ROC curves.

## Results
The autoencoder effectively reduced the dimensionality of the data while preserving important patterns for classification. The Logistic Regression and SVM models showed competitive performance, with the SVM model achieving a higher AUC-ROC score.
<br><br>
![download](https://github.com/user-attachments/assets/f93c8c0d-ff7a-4c23-a80e-8513f1d63840)
