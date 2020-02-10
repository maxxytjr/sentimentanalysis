# sentiment_analysis

## Introduction
This repository includes code from the *Sentiment Analysis Project* of the *Udacity Machine Learning Engineer* Nanodegree program.

## Description
A neural network (RNN) is constructed using PyTorch to conduct sentiment analysis from blocks of texts.

The neural netowrk is trained and deployed in **Amazon SageMaker**.

**Text preprocessing** included:
  * Removing HTML formats
  * Lowercasing text and replaced all characters that are not alphabets nor digits with spaces using regex
  * Split each word of the text into a space-separated list
  * Removing stopwords ('english')
  * Stemming each word in the list (egs converting entitled/entitling --> entitl, builds/building--> build)
  

## File Descriptions
### train
This folder contains the code that will be necessary for training the model. 

  * `model.py` contains the structure of the PyTorch neural network. 

  * `train.py` contains the code that trains the RNN.

### serve
This folder contains the Python files that will be used in the deployed model. 

  * `predict.py` contains code that will be deployed in the Amazon SageMaker endpoint, which will perform the sentiment predictions based on the user's input.

### website

  * `index.html` contains a basic html script that interacts with the user and the SageMaker endpoint.
