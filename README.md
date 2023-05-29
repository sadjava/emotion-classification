# Emotion Classification using Neural Network 
Classify facial images in [fer2013](https://www.kaggle.com/datasets/deadskull7/fer2013) dataset using custom built convolutional neural network

## Features
⚡Multi Label Image Classification  
⚡Cutsom Convolutional Network  
⚡Fine-tuned ResNet18

## Table of Contents
- [Objective](#objective)
- [Dataset](#dataset)
- [Evaluation Criteria](#evaluation-criteria)
- [Solution Approach](#solution-approach)

## Objective
I'll build a neural network using PyTorch. The goal here is to build a system to identify the emotion on a given facial image.

## Dataset
- Dataset consists of 32,000 training images and 3,000 testing images.
- Every image in the dataset will belong to one of the seven classes...

| Label	| Description |
|--- | ---|
|0|	Anger|
|1|	Disgust|
|2|	Fear|
|3|	Happy|
|4|	Neutral|
|5|	Sadness|
|6|	Surprise|

- Each image in the dataset is a 48x48 pixel grayscale image.


## Evaluation Criteria

### Loss Function  
Cross Entropy Loss is used as the loss function during model training and validation 

### Performance Metric
`accuracy` is used as the model's performance metric on the test-set 

<img src="https://github.com/sssingh/fashion-mnist-classification/blob/master/assets/accuracy.png?raw=true">

## Solution Approach
- Training dataset along with testing dataset are downloaded from [kaggle](https://www.kaggle.com/datasets/deadskull7/fer2013).
- Training dataset is then further split into training (29,000 samples) and validation (3,000) samples sets
- The training, validation, and testing datasets are then wrapped in PyTorch `Datamodule` object so that we can iterate through them with ease. A `batch_size` can be configured.

