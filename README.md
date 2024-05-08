# Applied ML Assignments Overview

This repository contains my assignments for the course 'Applied Machine Learning'. 

## Assignment 1: Email Spam Detection using Machine Learning

- Implemented machine learning algorithms to classify emails as spam or non-spam
- Included data preprocessing, model training, and evaluation
- Used the `emails.csv` dataset containing email content and labels

## Assignment 2: DVC - Data Version Control

- Involved model training and experiment tracking using MLflow
- Built, tracked, and registered benchmark models (Logistic Regression, Support Vector Classifier, Random Forest, Stacking Classifier)
- Calculated and printed AUCPR (Area Under the Precision-Recall Curve) for each benchmark model

## Assignment 3: Testing & Model Serving

### Unit Testing
- Implemented a scoring function in `score.py` to predict spam/non-spam and propensity scores
- Wrote unit tests in `test.py` to validate the scoring function

### Flask Serving
- Created a Flask endpoint `/score` in `app.py` to receive text and return predictions and propensity scores
- Wrote an integration test in `test.py` to verify the Flask app behavior

## Assignment 4: Containerization & Continuous Integration

- Implemented a Flask web application for classifying text as spam or not spam using a trained SVM model
- Provided an API endpoint `/classify` to accept a sentence and return classification result and propensity score
- Included unit tests for the scoring function and Flask application
- Dockerized the application with a Dockerfile for containerization

## Assignment 5: Transfer Learning

### Image Data using Convolutional Neural Networks (CNN)
- Downloaded 100 images of ducks and 100 images of chickens
- Fine-tuned a pre-trained CNN model to classify duck vs. chicken images

### Text Data using Transformers
- Downloaded the sentiment analysis dataset from Kaggle
- Built a sentiment analysis classifier (positive, neutral, negative)
- Fine-tuned a pre-trained transformer model (BERT) for text classification
