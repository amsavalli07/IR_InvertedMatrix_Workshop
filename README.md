#  NLP & IR Pipeline – Inverted Index + Vector Space Similarity

This repository contains our team’s submission for the **PROG8245 90-minute NLP Workshop**, where we built a complete natural language processing pipeline from scratch. The project demonstrates foundational NLP concepts such as tokenization, stemming, stop word removal, inverted indexing, and vector space modeling using cosine similarity.

---

##  Dataset Description

We used the `20 Newsgroups` dataset provided by `scikit-learn`, which contains real-world documents from various topics such as religion, space, computers, and politics. We selected a subset of **20 documents** from the training set.

- Source: `sklearn.datasets.fetch_20newsgroups`
- Preprocessing: Removed headers, footers, and quotes
- Number of documents: 20 (doc_0 to doc_19)
- License: Open dataset for educational use

---

##  NLP Pipeline Overview

The pipeline implements the following six foundational NLP concepts:

| Step | Concept                       | Description |
|------|-------------------------------|-------------|
|  1 | **Document Collection**        | Loaded 20 newsgroup documents |
|  2 | **Tokenization**              | Custom tokenizer to split text into words |
|  3 | **Normalization**             | Lowercasing, punctuation removal |
|  4 | **Stop Word Removal**         | Removed common non-informative words using NLTK |
|  5 | **Stemming**                  | Used PorterStemmer to reduce words to root form |
|  6 | **Vectorization + Cosine Similarity** | Transformed documents using TF-IDF and ranked similarity to phrase queries |

---

##  Repository Contents

| File Name                           | Description                                  |
|------------------------------------|----------------------------------------------|
| `IR_InvertedMatrix_Workshop.ipynb` | Final Jupyter Notebook with all steps, queries, and talking points |
| `README.md`                        | This file with full project documentation |

---

## 🔍 Functionality Implemented

-  Custom `tokenize()` and `normalize()` functions
-  `PorterStemmer`-based stemming pipeline
-  Inverted index using normalized tokens
-  Phrase query handling using **AND** and **OR** logic
-  TF-IDF vectorization using `TfidfVectorizer`
-  Cosine similarity calculation between query and document vectors
-  Ranked document retrieval for phrase queries

---

##  Example Phrase Query Tests

### Inverted Index Queries
- **Query**: `"space mission"` → Retrieved `doc_13`  
- **Query**: `"computer science"` → Returned `[]` due to token mismatch

### TF-IDF + Cosine Similarity
- **Query**: `"floppy disk"`  
- **Result**: Ranked docs based on cosine score (e.g., `doc_13`: 0.42, `doc_5`: 0.17, etc.)

---

##  Team Members

- **Name 1** – Student ID:   

---

##  Submission Info

**Course:**    
**Repo Name:**   
**Submitted On:** 
**Instructor:** 

##  How to Run

1. Open `IR_InvertedMatrix_Workshop.ipynb` in Jupyter Notebook.
2. Run all cells step-by-step to:
   - Build the inverted index
   - Query documents
   - Apply TF-IDF and check cosine similarity
3. Review talking points and phrase query results.
