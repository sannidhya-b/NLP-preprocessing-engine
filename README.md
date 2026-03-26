# NLP Preprocessing Engine

A robust, modular Natural Language Processing (NLP) preprocessing pipeline built as part of the **Data Science Internship – February 2026** assignment.

---

## 📌 Overview

Raw text data in the real world is noisy, inconsistent, and unstructured. This project implements a production-quality NLP preprocessing engine capable of handling emojis, URLs, slang, repeated characters, mixed case, and more — transforming raw text into clean, structured tokens ready for machine learning models.

---

## 📂 File Structure

```
📦 nlp-preprocessing-engine
 ┣ 📓 nlp_preprocessing_engine.ipynb   ← Main notebook (all tasks)
 ┗ 📄 README.md                        ← This file
```

---

## 🧠 Tasks Covered

| Task | Description |
|------|-------------|
| Task 1 | Conceptual understanding — stopwords, stemming, lemmatization |
| Task 2 | `preprocess_text()` — advanced preprocessing function |
| Task 3 | Stress testing on 10 diverse real-world sentences |
| Task 4 | Token analytics — total, unique, average token length |
| Task 5 | Frequency analysis using `collections.Counter` |
| Task 6 | `full_pipeline()` — end-to-end pipeline for a list of texts |
| Task 7 | Error handling — empty strings, emojis-only, numbers-only |

---

## ⚙️ Preprocessing Steps

The `preprocess_text()` function applies the following steps in order:

1. Remove URLs and email-like patterns
2. Remove emojis and non-ASCII characters
3. Convert text to lowercase
4. Collapse repeated characters (`soooo` → `so`)
5. Remove punctuation and special characters
6. Remove standalone numbers
7. Tokenize
8. Remove stopwords (preserving negations like `not`, `no`)
9. Remove very short tokens (length ≤ 2), with exceptions
10. Strip extra whitespace

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com)
2. Click **File → Upload notebook**
3. Upload `nlp_preprocessing_engine.ipynb`
4. Click **Runtime → Run all**

### Option 2 — Jupyter Notebook (Local)
```bash
pip install nltk jupyter
jupyter notebook nlp_preprocessing_engine.ipynb
```

---

## 📦 Dependencies

| Library | Purpose |
|---------|---------|
| `re` | Regex-based text cleaning |
| `string` | Punctuation handling |
| `collections.Counter` | Frequency analysis |
| `nltk` | Stopwords corpus |

All libraries are part of the Python standard library except `nltk`, which is auto-installed in the notebook.

---

## 📊 Sample Output

**Input:**
```
"I absolutely looooved this product 😍😍"
```

**Output:**
```
Tokens   : ['absolutely', 'loved', 'product']
Cleaned  : absolutely loved product
```

---

## 👤 Author

**Sannidhya Bahulekar**  
Agentic AI Intern – February 2026  
