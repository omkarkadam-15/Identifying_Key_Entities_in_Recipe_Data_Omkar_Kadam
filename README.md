# 🍲 Recipe Entity Extraction using CRF (NER)

## 📌 Project Overview

This project builds a Natural Language Processing (NLP) pipeline to extract key entities from recipe text using Named Entity Recognition (NER). It leverages Conditional Random Fields (CRF) to identify ingredients, quantities, and units from unstructured recipe data.

---

## 🎯 Objectives

* Extract structured information from recipe text
* Identify entities: ingredient, quantity, and unit
* Handle noisy and inconsistent text formats
* Build a high-accuracy sequence labeling model

---

## 📂 Dataset

* Source: JSON recipe dataset (ingredient_and_quantity.json)
* Records: ~280 samples
* Labels: ingredient, quantity, unit
* Cleaned invalid rows to ensure token-label alignment

---

## 🔍 Key Steps

### 1. Data Preprocessing

* Tokenized input text and labels
* Removed inconsistent and invalid rows
* Ensured equal length of tokens and labels

### 2. Exploratory Data Analysis

* Analyzed token distributions
* Identified frequent ingredients (e.g., salt, powder)
* Observed unit inconsistencies (cup/cups, teaspoon/teaspoons)

### 3. Feature Engineering

* Extracted token-level linguistic features
* Used regex for detecting quantities (fractions, decimals, numbers)
* Created contextual features using surrounding tokens

---

## 🤖 Model Used

* Conditional Random Fields (CRF)

  * Algorithm: lbfgs
  * L1 (c1): 0.5
  * L2 (c2): 1.0
  * Max iterations: 100

---

## 📊 Model Performance

* Accuracy: ~99.79%
* Very low error rates:

  * Quantity error ≈ 0.4%
  * Unit error ≈ 0.24%
* Confusion matrix shows near-perfect classification

---

## 🔑 Key Insights

* Strong performance due to contextual sequence modeling
* Most errors arise from linguistic ambiguity (e.g., "pinch", "cloves")
* Token proximity influences predictions (context-driven errors)

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* sklearn-crfsuite
* SpaCy, Regex

---

## 🚀 Future Improvements

* Phrase-level entity extraction
* Handle implicit quantities better
* Try transformer-based models (BERT, spaCy NER)

---

## 📎 Conclusion

This project demonstrates an effective NER pipeline using CRF for structured data extraction from recipe text. The model achieves high accuracy and is suitable for applications like recipe apps, dietary tracking, and food data platforms.

---

## 👤 Author

Omkar Kadam

