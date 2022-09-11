# AWS-SageMaker-on-Detecting-Payment-Card-Fraud

## Labeled Data
The payment fraud data set (Dal Pozzolo et al. 2015) was downloaded from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). This has features and labels for thousands of credit card transactions, each of which is labeled as fraudulent or valid. In this notebook, we'd like to train a model based on the features of these transactions so that we can predict risky or fraudulent transactions in the future.

## Binary Classification
Since we have true labels to aim for, we'll take a supervised learning approach and train a binary classifier to sort data into one of our two transaction classes: fraudulent or valid. We'll train a model on training data and see how well it generalizes on some test data.

The notebook will be broken down into a few steps:

- Loading and exploring the data
- Splitting the data into train/test sets
- Defining and training a LinearLearner, binary classifier
- Making improvements on the model
- Evaluating and comparing model test performance

## Making Improvements
A lot of this notebook will focus on making improvements, as discussed in this [SageMaker blog post](https://aws.amazon.com/cn/blogs/machine-learning/train-faster-more-flexible-models-with-amazon-sagemaker-linear-learner/). Specifically, we'll address techniques for:

- Tuning a model's hyperparameters and aiming for a specific metric, such as high recall or precision.
- Managing class imbalance, which is when we have many more training examples in one class than another (in this case, many more valid transactions than fraudulent).
