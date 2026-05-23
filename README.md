# A10_OPIM5512_JRJ24004

# Assignment 10: Food Recall Severity Classification

## Project Overview

This project predicts the severity of food recalls using NLP classification methods.  
The target variable is `Event Classification`, which includes:

- Class I
- Class II
- Class III

The model uses two text inputs:

- `Product Description`
- `Reason for Recall`

These fields were combined into one text feature for modeling.

## Main Challenge

The dataset is highly imbalanced, with Class II dominating the recall records.  
Because of this, model performance was evaluated mainly using **weighted F1-score**, not accuracy alone.

## Workflow

1. Load and inspect the Food Recalls dataset
2. Perform EDA on class distribution and recall text
3. Clean text data:
   - lowercase text
   - remove symbols
   - remove stopwords
   - apply stemming
4. Prepare NLP features:
   - Bag of Words
   - TF-IDF
   - tokenized / padded sequences
5. Train and compare models:
   - Naive majority-class baseline
   - Bag of Words + Decision Tree
   - TF-IDF + Decision Tree
   - Hugging Face zero-shot classifier
6. Evaluate models using:
   - confusion matrices
   - classification reports
   - weighted F1-score
7. Add interpretability using permutation importance

## Key Findings

- Bag of Words + Decision Tree achieved the strongest overall performance.
- Traditional NLP models outperformed the naive majority baseline.
- Permutation importance showed that words like `salmonella`, `listeria`, and `contamin` were important predictors.

## Files

```text
A10_final.ipynb
data/FoodRecalls.xlsx
