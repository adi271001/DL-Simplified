
# LLM Prompt Recovery Dataset

This repository contains the dataset for the "LLM Prompt Recovery" competition hosted on
Kaggle. The objective of this competition is to develop models that can recover prompts given to
large language models (LLMs).

## Table of Contents

1. Dataset Description
2. Files
3. Usage
4. Evaluation
5. Baseline Models
6. References

## Dataset Description

The dataset provided for this competition includes a collection of prompts and the
corresponding responses generated by a large language model (LLM). Participants are tasked
with recovering the original prompts from the provided responses.

The dataset is divided into three main parts:

```
Training Set : A set of response-prompt pairs for model training.
Validation Set : A set of response-prompt pairs for model validation.
Test Set : A set of responses for which participants need to predict the original prompts.
```
## Files

The dataset includes the following files:

```
train.csv : Contains the training data with columns response and prompt.
valid.csv : Contains the validation data with columns response and prompt.
test.csv : Contains the test data with the column response only.
```
### File Format

Each CSV file has the following structure:


```
train.csv and valid.csv :
response : The text generated by the LLM.
prompt : The original prompt given to the LLM.
```
```
test.csv :
response : The text generated by the LLM for which the prompt needs to be recovered.
```
## Usage

To use the dataset, follow these steps:

1. **Download the dataset** : Ensure you have the Kaggle API installed and set up, then download
    the dataset using the Kaggle API or through the Kaggle website.
2. **Load the data** : Use pandas or any other data processing library to load the CSV files into
    your environment.

```
import pandas as pd train_df = pd.read_csv('train.csv') valid_df =
pd.read_csv('valid.csv') test_df = pd.read_csv('test.csv')
```
3. **Preprocess the data** : Perform any necessary preprocessing steps, such as tokenization,
    normalization, etc., depending on the requirements of your model.
4. **Train your model** : Use the training and validation data to train your prompt recovery model.
5. **Make predictions** : Generate predictions on the test data and submit them to the
    competition.

## Evaluation

The evaluation metric for this competition is the BLEU score which measures the similarity
between the predicted prompts and the actual prompts.

To evaluate your model's performance, compare the predicted prompts with the true prompts in
the validation set using the BLEU score.

## Baseline Models

Participants are encouraged to develop their own models for prompt recovery. However,
baseline models are provided to help you get started. These models include:

```
Simple Heuristic Models : Basic models using string matching or simple heuristics.
Machine Learning Models : Traditional ML models such as logistic regression, SVM, etc.
Deep Learning Models : Advanced models such as transformers, seq2seq models, etc.
```
```
python Copy code
```

Refer to the **baseline_models** directory for implementations and usage instructions.

## References

For more information on the competition, datasets, and evaluation criteria, please refer to the
Kaggle competition page.