# Zero-Shot News Classification using Gliclass

This project applies a **zero-shot classification approach** to categorize news articles from the **AG News dataset** into predefined labels using a HuggingFace model.

---

##  Project Overview

The goal of this project is to classify news articles into four categories:

- World  
- Sports  
- Business  
- Science  

Instead of training a traditional machine learning model, a **zero-shot learning approach** was used with the `gliclass-modern-base-v3.0` model from HuggingFace.

---

## Dataset

- Dataset Name: AG News Classification Dataset  
- Source: Kaggle  
- Link: https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset  

The dataset contains labeled news articles already divided into the four classes above.

---

## Approach

### Zero-Shot Classification

### Why Zero-Shot?
- No need for model training
- Uses predefined labels directly
- Efficient for classification tasks with known categories
- Suitable for text classification benchmarking

---

## Model Used

- Model: gliclass-modern-base-v3.0  
- Provider: HuggingFace  
- Link: https://huggingface.co/knowledgator/gliclass-modern-base-v3.0  

---

## Implementation Steps

### 1. Data Loading
- Dataset downloaded from Kaggle
- Train file uploaded to Google Drive for easy access in Colab

### 2. Data Cleaning
The following preprocessing steps were applied:
- Convert text to lowercase  
- Remove URLs (http / https / www)  
- Remove mentions and hashtags (@, #)  
- Remove special characters and non-alphanumeric symbols  
- Remove numbers  
- Remove extra spaces  

---

### 3. Model Setup
- Installed `gliclass` library  
- Defined classification labels:

```python
labels = ['world', 'sports', 'business', 'science']
